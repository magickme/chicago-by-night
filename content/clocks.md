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
.clock-grid { display: grid; grid-template-columns: 1fr; gap: 1.5rem; margin: 1.5rem 0; }
.clock-card { border: 1px solid #d4d4d4; border-radius: 8px; padding: 1rem 1.25rem; background: #fafafa; }
.clock-card.critical { border-color: #dc2626; background: #fef2f2; }
.clock-card.keyed { border-color: #d97706; background: #fffbeb; }
.clock-card.closed { border-color: #a8a29e; background: #f5f5f4; opacity: 0.6; }
.clock-card.complete { border-color: #16a34a; background: #f0fdf4; }
.clock-name { font-weight: 700; font-size: 1.05rem; margin-bottom: 0.25rem; }
.clock-pips { font-size: 1.4rem; letter-spacing: 0.15rem; margin: 0.35rem 0; font-family: monospace; }
.pip-filled { color: #dc2626; }
.pip-empty { color: #d4d4d4; }
.pip-filled.green { color: #16a34a; }
.pip-filled.amber { color: #d97706; }
.pip-filled.blue { color: #2563eb; }
.clock-status { font-size: 0.85rem; color: #57534e; margin-top: 0.25rem; }
.clock-badge { display: inline-block; font-size: 0.7rem; font-weight: 700; text-transform: uppercase; padding: 0.1rem 0.4rem; border-radius: 3px; margin-left: 0.5rem; }
.badge-critical { background: #dc2626; color: white; }
.badge-keyed { background: #d97706; color: white; }
.badge-closed { background: #a8a29e; color: white; }
.badge-complete { background: #16a34a; color: white; }
.section-label { font-size: 0.8rem; text-transform: uppercase; letter-spacing: 0.1rem; color: #78716c; font-weight: 700; margin: 2rem 0 0.75rem; padding-bottom: 0.25rem; border-bottom: 1px solid #e7e5e4; }
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
