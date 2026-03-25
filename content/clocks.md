---
title: "Threat Clocks"
description: "Live pressure board for the Gary sandbox. Every clock ticking toward crisis."
layout: "page"
slug: "clocks"
menu:
  main:
    weight: 4
    params:
      icon: "clock"
---

<style>
.clock-grid { display: grid; grid-template-columns: 1fr; gap: 2rem; margin: 2rem 0; }
.clock-card { border: 2px solid #d4d4d4; border-radius: 12px; padding: 2rem; background: #fafafa; font-size: 18px !important; }
.clock-card * { font-size: inherit; }
.clock-card.critical { border-color: #dc2626; border-width: 3px; background: #fef2f2; }
.clock-card.keyed { border-color: #d97706; border-width: 3px; background: #fffbeb; }
.clock-card.closed { border-color: #a8a29e; background: #f5f5f4; opacity: 0.5; }
.clock-card.complete { border-color: #16a34a; border-width: 3px; background: #f0fdf4; }
.clock-name { font-weight: 700 !important; font-size: 24px !important; margin-bottom: 0.5rem; }
.clock-pips { font-size: 56px !important; letter-spacing: 0.4rem; margin: 0.75rem 0; font-family: monospace; line-height: 1.2; }
.pip-filled { color: #dc2626 !important; }
.pip-empty { color: #d4d4d4 !important; }
.pip-filled.green { color: #16a34a !important; }
.pip-filled.amber { color: #d97706 !important; }
.pip-filled.blue { color: #2563eb !important; }
.clock-status { font-size: 16px !important; color: #57534e !important; margin-top: 0.75rem; line-height: 1.6; }
.clock-status strong { color: #1c1917 !important; }
.clock-badge { display: inline-block; font-size: 13px !important; font-weight: 700; text-transform: uppercase; padding: 0.25rem 0.7rem; border-radius: 4px; margin-left: 0.5rem; vertical-align: middle; letter-spacing: 0.05rem; }
.badge-critical { background: #dc2626; color: white !important; }
.badge-keyed { background: #d97706; color: white !important; }
.badge-closed { background: #a8a29e; color: white !important; }
.badge-complete { background: #16a34a; color: white !important; }
.section-label { font-size: 18px !important; text-transform: uppercase; letter-spacing: 0.12rem; color: #78716c !important; font-weight: 700; margin: 3rem 0 1rem; padding-bottom: 0.5rem; border-bottom: 2px solid #e7e5e4; }
</style>

*Gary, Indiana. Updated: **July 17, 1990.** All clocks /6. At 4/6, local heat spills into Masquerade. At 6/6, active crisis.*

---

<div class="section-label">Political Pressure</div>
<div class="clock-grid">

<div class="clock-card">
<div class="clock-name">Modius Leash — Darius</div>
<div class="clock-pips"><span class="pip-filled blue">&#9632;</span><span class="pip-empty">&#9632;&#9632;&#9632;&#9632;&#9632;</span></div>
<div class="clock-status"><strong>1/6</strong> — The handshake. Prince trusts Darius after Torch play.</div>
</div>

<div class="clock-card critical">
<div class="clock-name">Modius Leash — Sable <span class="clock-badge badge-critical">CRITICAL</span></div>
<div class="clock-pips"><span class="pip-filled">&#9632;&#9632;&#9632;&#9632;&#9632;</span><span class="pip-empty">&#9632;</span></div>
<div class="clock-status"><strong>5/6</strong> — Blood sharing violation undiscovered. Drawing room surveillance. One more tick = property, suspect, or sacrifice.</div>
</div>

<div class="clock-card">
<div class="clock-name">Cover Story Exposure</div>
<div class="clock-pips"><span class="pip-filled amber">&#9632;&#9632;&#9632;</span><span class="pip-empty">&#9632;&#9632;&#9632;</span></div>
<div class="clock-status"><strong>3/6</strong> — Lucian + Modius both holding questions. Chuc Luc building replacement identity.</div>
</div>

<div class="clock-card">
<div class="clock-name">Sharon's Vendetta</div>
<div class="clock-pips"><span class="pip-filled">&#9632;</span><span class="pip-empty">&#9632;&#9632;&#9632;&#9632;&#9632;</span></div>
<div class="clock-status"><strong>1/6</strong> — Letter sent to Denise Price. At 2/6: proxy arrives in Gary. At 4/6: Sharon arrives personally.</div>
</div>

<div class="clock-card complete">
<div class="clock-name">Allicia Alliance <span class="clock-badge badge-complete">COMPLETE</span></div>
<div class="clock-pips"><span class="pip-filled green">&#9632;&#9632;&#9632;&#9632;&#9632;&#9632;</span></div>
<div class="clock-status"><strong>6/6</strong> — Blood Bond Step 1 (Allicia to Sable). Competing with Modius's 3-step bond.</div>
</div>

</div>

<div class="section-label">Investigation &amp; Hunters</div>
<div class="clock-grid">

<div class="clock-card critical">
<div class="clock-name">Torch / Rack Heat <span class="clock-badge badge-critical">CRITICAL</span></div>
<div class="clock-pips"><span class="pip-filled">&#9632;&#9632;&#9632;&#9632;&#9632;</span><span class="pip-empty">&#9632;</span></div>
<div class="clock-status"><strong>5/6</strong> — FBI physically visited. Shepard questioned Victor, has Warren Birch name. One more tick = the Torch becomes a trap.</div>
</div>

<div class="clock-card">
<div class="clock-name">Dane Identifies Darius</div>
<div class="clock-pips"><span class="pip-filled amber">&#9632;&#9632;</span><span class="pip-empty">&#9632;&#9632;&#9632;&#9632;</span></div>
<div class="clock-status"><strong>2/6</strong> — Patient, thorough, nine months of data. At 3/6: Dane appears in 1d4 scenes.</div>
</div>

<div class="clock-card">
<div class="clock-name">Gregory + Shepard Convergence</div>
<div class="clock-pips"><span class="pip-filled amber">&#9632;&#9632;</span><span class="pip-empty">&#9632;&#9632;&#9632;&#9632;</span></div>
<div class="clock-status"><strong>2/6</strong> — FBI investigating Lakeside/Torch. At 4/6: they share intelligence.</div>
</div>

<div class="clock-card">
<div class="clock-name">Masquerade Heat</div>
<div class="clock-pips"><span class="pip-filled">&#9632;</span><span class="pip-empty">&#9632;&#9632;&#9632;&#9632;&#9632;</span></div>
<div class="clock-status"><strong>1/6</strong> — Fragile but not burning. At 4/6: local heat auto-spills. At 6/6: Chicago sends an Archon.</div>
</div>

</div>

<div class="section-label">Territory Heat</div>
<div class="clock-grid">

<div class="clock-card keyed">
<div class="clock-name">Dock Pipeline Exposure <span class="clock-badge badge-keyed">KEYED</span></div>
<div class="clock-pips"><span class="pip-filled amber">&#9632;&#9632;&#9632;</span><span class="pip-empty">&#9632;&#9632;&#9632;</span></div>
<div class="clock-status"><strong>3/6</strong> — Pipeline ACTIVE. Eddie Fells Dominated. Warehouse operational. <strong>Lucian makes friendly contact soon.</strong></div>
</div>

<div class="clock-card">
<div class="clock-name">Docks Heat</div>
<div class="clock-pips"><span class="pip-filled amber">&#9632;&#9632;</span><span class="pip-empty">&#9632;&#9632;&#9632;&#9632;</span></div>
<div class="clock-status"><strong>2/6</strong> — Dockworkers guarding words around strangers.</div>
</div>

<div class="clock-card">
<div class="clock-name">Wasteland Heat</div>
<div class="clock-pips"><span class="pip-filled">&#9632;</span><span class="pip-empty">&#9632;&#9632;&#9632;&#9632;&#9632;</span></div>
<div class="clock-status"><strong>1/6</strong> — Gangs, anarchs, bodies.</div>
</div>

<div class="clock-card">
<div class="clock-name">West Side Heat</div>
<div class="clock-pips"><span class="pip-empty">&#9632;&#9632;&#9632;&#9632;&#9632;&#9632;</span></div>
<div class="clock-status"><strong>0/6</strong> — Room to build quietly.</div>
</div>

</div>

<div class="section-label">Resolved</div>
<div class="clock-grid">

<div class="clock-card closed">
<div class="clock-name">Blood at Dawn <span class="clock-badge badge-closed">CLOSED</span></div>
<div class="clock-pips"><span class="pip-empty">&#9632;&#9632;&#9632;&#9632;&#9632;&#9632;</span></div>
<div class="clock-status">Spirit destroyed, Falcon delivered, Wierus exits as threat.</div>
</div>

<div class="clock-card closed">
<div class="clock-name">Williams Retaliation <span class="clock-badge badge-closed">CLOSED</span></div>
<div class="clock-pips"><span class="pip-empty">&#9632;&#9632;&#9632;&#9632;&#9632;&#9632;</span></div>
<div class="clock-status">Williams destroyed. Church operation burned.</div>
</div>

</div>

---

*Clocks tick during scene bookkeeping. At 4/6+, local heat spills into Masquerade Heat. At 6/6, the clock triggers a crisis that reshapes the board. See [Relationship Maps](/relationships/) for the full NPC network.*
