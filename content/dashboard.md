---
title: "Dashboard"
description: "Game state at a glance. Threat clocks, quest log, and boon ledger."
layout: "page"
slug: "dashboard"
menu:
  main:
    weight: 4
    params:
      icon: "dots"
---

<style>
/* === CLOCKS === */
.clock-grid { display: grid; grid-template-columns: 1fr; gap: 1.5rem; margin: 1.5rem 0; }
.clock-card { border: 2px solid #d4d4d4; border-radius: 12px; padding: 1.5rem; background: #fafafa; font-size: 16px !important; }
.clock-card * { font-size: inherit; }
.clock-card.critical { border-color: #dc2626; border-width: 3px; background: #fef2f2; }
.clock-card.keyed { border-color: #d97706; border-width: 3px; background: #fffbeb; }
.clock-card.closed { border-color: #a8a29e; background: #f5f5f4; opacity: 0.5; }
.clock-card.complete { border-color: #16a34a; border-width: 3px; background: #f0fdf4; }
.clock-name { font-weight: 700 !important; font-size: 20px !important; margin-bottom: 0.4rem; }
.clock-pips { font-size: 48px !important; letter-spacing: 0.3rem; margin: 0.5rem 0; font-family: monospace; line-height: 1.2; }
.pip-filled { color: #dc2626 !important; }
.pip-empty { color: #d4d4d4 !important; }
.pip-filled.green { color: #16a34a !important; }
.pip-filled.amber { color: #d97706 !important; }
.pip-filled.blue { color: #2563eb !important; }
.clock-status { font-size: 14px !important; color: #57534e !important; margin-top: 0.4rem; line-height: 1.5; }
.clock-status strong { color: #1c1917 !important; }
.clock-badge { display: inline-block; font-size: 11px !important; font-weight: 700; text-transform: uppercase; padding: 0.2rem 0.5rem; border-radius: 4px; margin-left: 0.5rem; vertical-align: middle; }
.badge-critical { background: #dc2626; color: white !important; }
.badge-keyed { background: #d97706; color: white !important; }
.badge-closed { background: #a8a29e; color: white !important; }
.badge-complete { background: #16a34a; color: white !important; }

/* === QUESTS === */
.quest-card { border-left: 4px solid #d4d4d4; padding: 1rem 1.25rem; margin-bottom: 1rem; background: #fafafa; border-radius: 0 6px 6px 0; }
.quest-card.active { border-left-color: #eab308; }
.quest-card.side-active { border-left-color: #3b82f6; }
.quest-card.optional-active { border-left-color: #a78bfa; }
.quest-card.done { border-left-color: #16a34a; background: #f0fdf4; opacity: 0.7; }
.quest-card.critical { border-left-color: #dc2626; border-left-width: 5px; background: #fef2f2; }
.quest-header { display: flex; align-items: center; gap: 0.6rem; flex-wrap: wrap; }
.quest-name { font-weight: 700; font-size: 16px !important; color: #1c1917; }
.quest-pc { font-size: 11px !important; font-weight: 700; text-transform: uppercase; padding: 0.1rem 0.4rem; border-radius: 3px; }
.pc-darius { background: #dbeafe; color: #1e40af; }
.pc-sable { background: #fce7f3; color: #9d174d; }
.pc-both { background: #ede9fe; color: #5b21b6; }
.quest-status { font-size: 11px !important; font-weight: 700; text-transform: uppercase; padding: 0.1rem 0.4rem; border-radius: 3px; }
.status-active { background: #fef3c7; color: #92400e; }
.status-done { background: #dcfce7; color: #166534; }
.status-locked { background: #e7e5e4; color: #57534e; }
.status-critical { background: #fecaca; color: #991b1b; }
.status-advancing { background: #dbeafe; color: #1e40af; }
.quest-desc { font-size: 14px !important; color: #57534e; margin-top: 0.4rem; line-height: 1.5; }
.quest-objective { font-size: 13px !important; color: #78716c; margin-top: 0.3rem; padding-left: 0.75rem; border-left: 2px solid #e7e5e4; }

/* === BOONS === */
.boon-card { border-left: 4px solid #d4d4d4; padding: 0.75rem 1rem; margin-bottom: 0.75rem; background: #fafafa; border-radius: 0 6px 6px 0; }
.boon-card.debt { border-left-color: #dc2626; }
.boon-card.credit { border-left-color: #16a34a; background: #f0fdf4; }
.boon-card.even { border-left-color: #78716c; background: #f5f5f4; opacity: 0.7; }
.boon-card.feudal { border-left-color: #d97706; background: #fffbeb; }
.boon-card.npc-debt { border-left-color: #a78bfa; background: #faf5ff; }
.boon-header { display: flex; align-items: center; gap: 0.6rem; flex-wrap: wrap; }
.boon-parties { font-weight: 700; font-size: 15px !important; color: #1c1917; }
.boon-level { font-size: 11px !important; font-weight: 700; text-transform: uppercase; padding: 0.1rem 0.4rem; border-radius: 3px; }
.level-minor { background: #dbeafe; color: #1e40af; }
.level-moderate { background: #fef3c7; color: #92400e; }
.level-life { background: #292524; color: #fbbf24; }
.level-fealty { background: #451a03; color: #fbbf24; }
.level-even { background: #d6d3d1; color: #57534e; }
.boon-desc { font-size: 13px !important; color: #57534e; margin-top: 0.3rem; line-height: 1.5; }

/* === SHARED === */
.dash-section { font-size: 14px !important; text-transform: uppercase; letter-spacing: 0.1rem; color: #78716c; font-weight: 700; margin: 2.5rem 0 0.75rem; padding-bottom: 0.4rem; border-bottom: 2px solid #e7e5e4; }
.dash-section.gold { color: #92400e; border-color: #eab308; }
.dash-section.blue { color: #1e40af; border-color: #3b82f6; }
.dash-section.green { color: #166534; border-color: #16a34a; }
.dash-section.red { color: #991b1b; border-color: #dc2626; }
.dash-section.purple { color: #5b21b6; border-color: #a78bfa; }
</style>

*Gary, Indiana. Updated: **July 20, 1990.** See also: [Territory Map](/map/) | [Relationship Maps](/relationships/)*

---

## Threat Clocks

*All clocks /6. At 4/6, local heat spills into Masquerade. At 6/6, active crisis.*

<div class="dash-section red">Critical</div>
<div class="clock-grid">

<div class="clock-card">
<div class="clock-name">Modius Leash — Sable</div>
<div class="clock-pips"><span class="pip-filled">&#9632;&#9632;&#9632;&#9632;</span><span class="pip-empty">&#9632;&#9632;</span></div>
<div class="clock-status"><strong>4/6</strong> — EASED. Competent FBI report. Chicago scrutiny revealed. "More useful than I expected." Still a leash, but longer.</div>
</div>

<div class="clock-card critical">
<div class="clock-name">Torch / Rack Heat <span class="clock-badge badge-critical">CRITICAL</span></div>
<div class="clock-pips"><span class="pip-filled">&#9632;&#9632;&#9632;&#9632;&#9632;</span><span class="pip-empty">&#9632;</span></div>
<div class="clock-status"><strong>5/6</strong> — FBI physically visited. Shepard has Warren Birch name. One more tick = the Torch becomes a trap.</div>
</div>

</div>

<div class="dash-section">Active</div>
<div class="clock-grid">

<div class="clock-card keyed">
<div class="clock-name">Dock Pipeline Exposure <span class="clock-badge badge-keyed">KEYED</span></div>
<div class="clock-pips"><span class="pip-filled amber">&#9632;&#9632;&#9632;</span><span class="pip-empty">&#9632;&#9632;&#9632;</span></div>
<div class="clock-status"><strong>3/6</strong> — Pipeline ACTIVE. Eddie Fells Dominated. <strong>Lucian makes friendly contact soon.</strong></div>
</div>

<div class="clock-card">
<div class="clock-name">Cover Story Exposure</div>
<div class="clock-pips"><span class="pip-filled amber">&#9632;&#9632;&#9632;</span><span class="pip-empty">&#9632;&#9632;&#9632;</span></div>
<div class="clock-status"><strong>3/6</strong> — Two elders holding questions. Chuc Luc building replacement identity.</div>
</div>

<div class="clock-card">
<div class="clock-name">Dane Identifies Darius</div>
<div class="clock-pips"><span class="pip-filled amber">&#9632;&#9632;</span><span class="pip-empty">&#9632;&#9632;&#9632;&#9632;</span></div>
<div class="clock-status"><strong>2/6</strong> — Patient, thorough, nine months of data. At 3/6: Dane appears in 1d4 scenes.</div>
</div>

<div class="clock-card">
<div class="clock-name">Gregory + Shepard Convergence</div>
<div class="clock-pips"><span class="pip-filled amber">&#9632;&#9632;</span><span class="pip-empty">&#9632;&#9632;&#9632;&#9632;</span></div>
<div class="clock-status"><strong>2/6</strong> — At 4/6: they share intelligence.</div>
</div>

<div class="clock-card">
<div class="clock-name">Docks Heat</div>
<div class="clock-pips"><span class="pip-filled amber">&#9632;&#9632;</span><span class="pip-empty">&#9632;&#9632;&#9632;&#9632;</span></div>
<div class="clock-status"><strong>2/6</strong> — Dockworkers guarding words.</div>
</div>

<div class="clock-card">
<div class="clock-name">Modius Leash — Darius</div>
<div class="clock-pips"><span class="pip-filled blue">&#9632;</span><span class="pip-empty">&#9632;&#9632;&#9632;&#9632;&#9632;</span></div>
<div class="clock-status"><strong>1/6</strong> — The handshake. Prince trusts Darius.</div>
</div>

<div class="clock-card">
<div class="clock-name">Sharon's Vendetta</div>
<div class="clock-pips"><span class="pip-filled">&#9632;</span><span class="pip-empty">&#9632;&#9632;&#9632;&#9632;&#9632;</span></div>
<div class="clock-status"><strong>1/6</strong> — Letter sent to Denise. At 2/6: proxy arrives.</div>
</div>

<div class="clock-card">
<div class="clock-name">Masquerade Heat</div>
<div class="clock-pips"><span class="pip-filled">&#9632;</span><span class="pip-empty">&#9632;&#9632;&#9632;&#9632;&#9632;</span></div>
<div class="clock-status"><strong>1/6</strong> — Fragile but not burning.</div>
</div>

<div class="clock-card">
<div class="clock-name">Wasteland Heat</div>
<div class="clock-pips"><span class="pip-filled">&#9632;</span><span class="pip-empty">&#9632;&#9632;&#9632;&#9632;&#9632;</span></div>
<div class="clock-status"><strong>1/6</strong> — Gangs, anarchs, bodies.</div>
</div>

</div>

---

## Quest Log

<div class="dash-section gold">Main Quests</div>

<div class="quest-card active">
<div class="quest-header">
<span class="quest-name">Build the Pipeline</span>
<span class="quest-pc pc-darius">Darius</span>
<span class="quest-status status-active">Active</span>
</div>
<div class="quest-desc">Smuggling pipeline through Gary's docks for Chuc Luc. Pipeline OPERATIONAL — first shipment next week.</div>
</div>

<div class="quest-card active">
<div class="quest-header">
<span class="quest-name">Maintain the Cover</span>
<span class="quest-pc pc-darius">Darius</span>
<span class="quest-status status-active">3/6</span>
</div>
<div class="quest-desc">10th gen pretending to be 12th. Warren Birch proxy planned. Danov's forger working (4-6 weeks).</div>
</div>

<div class="quest-card critical">
<div class="quest-header">
<span class="quest-name">Navigate the Modius Leash</span>
<span class="quest-pc pc-sable">Sable</span>
<span class="quest-status status-critical">Critical — 5/6</span>
</div>
<div class="quest-desc">Blood sharing violation undiscovered. One discovery = crisis. Break free, submit, or find leverage.</div>
</div>

<div class="dash-section blue">Side Quests</div>

<div class="quest-card side-active">
<div class="quest-header"><span class="quest-name">The FBI Problem</span><span class="quest-pc pc-darius">Darius</span><span class="quest-status status-advancing">Plan Forming</span></div>
<div class="quest-desc">Shepard investigating Torch. Proxy + Danov forger. Juggler partnered.</div>
</div>

<div class="quest-card side-active">
<div class="quest-header"><span class="quest-name">Handle Marcus Webb</span><span class="quest-pc pc-darius">Darius</span><span class="quest-status status-critical">Urgent</span></div>
<div class="quest-desc">Chuc Luc: "You will solve it or I will." Dominate, distance, or death.</div>
</div>

<div class="quest-card side-active">
<div class="quest-header"><span class="quest-name">Protect Allicia</span><span class="quest-pc pc-sable">Sable</span><span class="quest-status status-active">Active</span></div>
<div class="quest-desc">Alliance 6/6. Blood Bond Step 1. Modius starving her. Drawing room surveillance.</div>
</div>

<div class="quest-card side-active">
<div class="quest-header"><span class="quest-name">Sullivan Dane</span><span class="quest-pc pc-darius">Darius</span><span class="quest-status status-active">2/6</span></div>
<div class="quest-desc">True Faith 5. Nine months of data. At 3/6: appears in 1d4 scenes.</div>
</div>

<div class="quest-card side-active">
<div class="quest-header"><span class="quest-name">Sharon's Vendetta</span><span class="quest-pc pc-sable">Sable</span><span class="quest-status status-active">1/6</span></div>
<div class="quest-desc">Presence 5. Sixty years of rage. Letter to Denise Price. She's coming.</div>
</div>

<div class="quest-card side-active">
<div class="quest-header"><span class="quest-name">Sal Cantone</span><span class="quest-pc pc-darius">Darius</span><span class="quest-status status-advancing">Managed</span></div>
<div class="quest-desc">Stolen drug pipeline. First watcher memory-rewritten. Cantone will escalate.</div>
</div>

<div class="quest-card side-active">
<div class="quest-header"><span class="quest-name">Denise Price</span><span class="quest-pc pc-sable">Sable</span><span class="quest-status status-active">Active</span></div>
<div class="quest-desc">Mother found the studio number. Phone unplugged. Problem isn't.</div>
</div>

<div class="quest-card side-active">
<div class="quest-header"><span class="quest-name">Deliver Lucian's Feeding Rights</span><span class="quest-pc pc-darius">Darius</span><span class="quest-status status-active">Pending</span></div>
<div class="quest-desc">Modius's order. Still undelivered. Lucian keyed contact may overlap.</div>
</div>

<div class="quest-card side-active">
<div class="quest-header"><span class="quest-name">Find Michael Payne</span><span class="quest-pc pc-sable">Sable</span><span class="quest-status status-active">Escalated</span></div>
<div class="quest-desc">Sable's sire. Missing. Called to Primogen by Sharon.</div>
</div>

<div class="dash-section purple">Optional</div>

<div class="quest-card optional-active">
<div class="quest-header"><span class="quest-name">Mr. White</span><span class="quest-pc pc-darius">Darius</span><span class="quest-status status-locked">October</span></div>
<div class="quest-desc">Milwaukee buyer. Possible Kindred. Notebook has the schedule.</div>
</div>

<div class="quest-card optional-active">
<div class="quest-header"><span class="quest-name">Church Disposal</span><span class="quest-pc pc-darius">Darius</span><span class="quest-status status-advancing">In Progress</span></div>
<div class="quest-desc">Ray burns Polk & 13th. Destroy the trafficking evidence.</div>
</div>

<div class="quest-card done">
<div class="quest-header"><span class="quest-name">Big Six</span><span class="quest-pc pc-sable">Sable</span><span class="quest-status status-done">Resolved</span></div>
<div class="quest-desc">Drained to death at Kendrick's Auto. Crew ghouled. Haven secured. The predator became the prey.</div>
</div>

<div class="quest-card optional-active">
<div class="quest-header"><span class="quest-name">Keisha and Amy</span><span class="quest-pc pc-sable">Sable</span><span class="quest-status status-active">Background</span></div>
<div class="quest-desc">Rescued. At Fifth Avenue studio. Need placement.</div>
</div>

<div class="dash-section green">Completed</div>

<div class="quest-card done">
<div class="quest-header"><span class="quest-name">Blood at Dawn</span><span class="quest-pc pc-both">Both</span><span class="quest-status status-done">Complete</span></div>
<div class="quest-desc">Spirit destroyed. Falcon delivered. Wierus exits.</div>
</div>

<div class="quest-card done">
<div class="quest-header"><span class="quest-name">Torch Auction</span><span class="quest-pc pc-darius">Darius</span><span class="quest-status status-done">Complete</span></div>
<div class="quest-desc">Mortgage assumed. $800/mo. Warren Birch owns the building.</div>
</div>

<div class="quest-card done">
<div class="quest-header"><span class="quest-name">Williams Slave Auction</span><span class="quest-pc pc-both">Both</span><span class="quest-status status-done">Complete</span></div>
<div class="quest-desc">Williams destroyed. Keisha + Amy rescued. 43 entries in a dead man's notebook.</div>
</div>

<div class="quest-card done">
<div class="quest-header"><span class="quest-name">Allicia Alliance</span><span class="quest-pc pc-sable">Sable</span><span class="quest-status status-done">6/6</span></div>
<div class="quest-desc">Blood Bond Step 1. Seven words counted.</div>
</div>

<div class="quest-card done">
<div class="quest-header"><span class="quest-name">Feeding Rights</span><span class="quest-pc pc-darius">Darius</span><span class="quest-status status-done">Complete</span></div>
<div class="quest-desc">Annual, renewable. Lucian accepted.</div>
</div>

<div class="quest-card done">
<div class="quest-header"><span class="quest-name">Secure The Torch</span><span class="quest-pc pc-darius">Darius</span><span class="quest-status status-done">Complete</span></div>
<div class="quest-desc">Fisk mesmerized. Juggler partnership. Three-layer ownership.</div>
</div>

<div class="quest-card done">
<div class="quest-header"><span class="quest-name">Warehouse + Customs Gap</span><span class="quest-pc pc-darius">Darius</span><span class="quest-status status-done">Complete</span></div>
<div class="quest-desc">Eddie Fells Dominated. Pipeline stolen from Sal Cantone.</div>
</div>

---

## Boon Ledger

*No harpies in Gary. Debts tracked by memory, reputation, and what Danov's archive records.*

<div class="dash-section red">PCs Owe</div>

<div class="boon-card debt">
<div class="boon-header"><span class="boon-parties">Sable → Juggler</span><span class="boon-level level-minor">Minor</span></div>
<div class="boon-desc">Gloria Serrano house call for Amy. "You owe me for this, Price." Explicit.</div>
</div>

<div class="boon-card feudal">
<div class="boon-header"><span class="boon-parties">Sable → Modius</span><span class="boon-level level-fealty">Fealty</span></div>
<div class="boon-desc">Studio + spy assignment. Feudal service, not discrete boon. Leash 5/6.</div>
</div>

<div class="boon-card debt">
<div class="boon-header"><span class="boon-parties">Darius → Juggler</span><span class="boon-level level-minor">Minor</span></div>
<div class="boon-desc">Danov intro + FBI counsel. Implicit. Torch partnership may settle it.</div>
</div>

<div class="boon-card feudal">
<div class="boon-header"><span class="boon-parties">Darius → Modius</span><span class="boon-level level-fealty">Fealty</span></div>
<div class="boon-desc">Handshake, domain, Torch approval. Princely grant or princely leash. Ambiguous.</div>
</div>

<div class="boon-card feudal">
<div class="boon-header"><span class="boon-parties">Darius → Chuc Luc</span><span class="boon-level level-fealty">Filial</span></div>
<div class="boon-desc">Sire-childe. Every word is an instruction. Pipeline is the job.</div>
</div>

<div class="dash-section green">NPCs Owe PCs</div>

<div class="boon-card credit">
<div class="boon-header"><span class="boon-parties">Allicia → Sable</span><span class="boon-level level-moderate">Moderate?</span></div>
<div class="boon-desc">Blood (5 BP), cover, double-agent service. Blood Bond Step 1 distorts the accounting.</div>
</div>

<div class="dash-section purple">NPC Debts Affecting PCs</div>

<div class="boon-card npc-debt">
<div class="boon-header"><span class="boon-parties">Juggler → Lucian</span><span class="boon-level level-minor">Unknown</span></div>
<div class="boon-desc">Constrains Juggler's freedom on anything touching Lucian's interests.</div>
</div>

<div class="boon-card npc-debt">
<div class="boon-header"><span class="boon-parties">Allicia → Modius</span><span class="boon-level level-life">Blood Bond (3)</span></div>
<div class="boon-desc">Regnant/thrall. Ownership, not prestation. Sable's Step 1 is the competing claim.</div>
</div>

---

*Dashboard reflects game state as of July 20, 1990. Updated during scene bookkeeping.*
