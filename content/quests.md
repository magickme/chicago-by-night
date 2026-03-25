---
title: "Quest Log"
description: "Every thread in Gary. Main quests, side quests, and the jobs nobody asked for."
layout: "page"
slug: "quests"
menu:
  main:
    weight: 3
    params:
      icon: "tag"
---

<style>
.quest-section { margin: 2.5rem 0; }
.quest-section-title { font-size: 22px !important; font-weight: 800; text-transform: uppercase; letter-spacing: 0.1rem; padding-bottom: 0.5rem; margin-bottom: 1.5rem; }
.quest-section-title.main { color: #eab308; border-bottom: 3px solid #eab308; }
.quest-section-title.side { color: #3b82f6; border-bottom: 3px solid #3b82f6; }
.quest-section-title.optional { color: #a78bfa; border-bottom: 3px solid #a78bfa; }
.quest-section-title.complete { color: #16a34a; border-bottom: 3px solid #16a34a; }

.quest-card { border-left: 4px solid #d4d4d4; padding: 1rem 1.25rem; margin-bottom: 1.25rem; background: #fafafa; border-radius: 0 6px 6px 0; }
.quest-card.active { border-left-color: #eab308; }
.quest-card.side-active { border-left-color: #3b82f6; }
.quest-card.optional-active { border-left-color: #a78bfa; }
.quest-card.done { border-left-color: #16a34a; background: #f0fdf4; opacity: 0.7; }
.quest-card.locked { border-left-color: #78716c; background: #f5f5f4; opacity: 0.5; }
.quest-card.critical { border-left-color: #dc2626; border-left-width: 5px; background: #fef2f2; }

.quest-header { display: flex; align-items: center; gap: 0.75rem; flex-wrap: wrap; }
.quest-name { font-weight: 700; font-size: 18px !important; color: #1c1917; }
.quest-pc { font-size: 12px !important; font-weight: 700; text-transform: uppercase; padding: 0.15rem 0.5rem; border-radius: 3px; letter-spacing: 0.05rem; }
.pc-darius { background: #dbeafe; color: #1e40af; }
.pc-sable { background: #fce7f3; color: #9d174d; }
.pc-both { background: #ede9fe; color: #5b21b6; }
.quest-status { font-size: 12px !important; font-weight: 700; text-transform: uppercase; padding: 0.15rem 0.5rem; border-radius: 3px; }
.status-active { background: #fef3c7; color: #92400e; }
.status-done { background: #dcfce7; color: #166534; }
.status-locked { background: #e7e5e4; color: #57534e; }
.status-critical { background: #fecaca; color: #991b1b; }
.status-advancing { background: #dbeafe; color: #1e40af; }
.status-hidden { background: #292524; color: #a8a29e; }

.quest-desc { font-size: 15px !important; color: #57534e; margin-top: 0.5rem; line-height: 1.6; }
.quest-desc strong { color: #1c1917; }
.quest-objective { font-size: 14px !important; color: #78716c; margin-top: 0.4rem; padding-left: 1rem; border-left: 2px solid #e7e5e4; }
.quest-reward { font-size: 13px !important; color: #16a34a; margin-top: 0.3rem; font-style: italic; }
</style>

*Act I: Forged in Steel. Gary, Indiana. Updated: **July 17, 1990.***

---

<div class="quest-section">
<div class="quest-section-title main">Main Quests</div>

<div class="quest-card active">
<div class="quest-header">
<span class="quest-name">Build the Pipeline</span>
<span class="quest-pc pc-darius">Darius</span>
<span class="quest-status status-active">Active</span>
</div>
<div class="quest-desc">Establish a smuggling pipeline through Gary's docks for Chuc Luc. Route Mafia money through Gary Exports Co. without Lucian knowing who's really behind it.</div>
<div class="quest-objective"><strong>Progress:</strong> Pipeline OPERATIONAL. Berth 7 receiving (Eddie Fells, Dominated). Warehouse active behind Gary Exports. Customs gap = Eddie. Torch secured as front. First shipment next week. Chuc Luc's seed money deployed.<br><strong>Remaining:</strong> First successful cargo run. Chuc Luc's final approval. Cover must hold.</div>
</div>

<div class="quest-card active">
<div class="quest-header">
<span class="quest-name">Maintain the Cover</span>
<span class="quest-pc pc-darius">Darius</span>
<span class="quest-status status-active">Active — 3/6</span>
</div>
<div class="quest-desc">Darius is 10th generation pretending to be 12th. The Warren Birch identity must survive scrutiny from two elders, the FBI, and a sire who's building a replacement.</div>
<div class="quest-objective"><strong>Threats:</strong> Modius flagged the money question. Lucian noticed the connections. Shepard has Warren Birch's name. Danov could read the blood.<br><strong>In progress:</strong> Chuc Luc building replacement identity. Warren Birch proxy planned (Danov's forger, 4-6 weeks).</div>
</div>

<div class="quest-card critical">
<div class="quest-header">
<span class="quest-name">Navigate the Modius Leash</span>
<span class="quest-pc pc-sable">Sable</span>
<span class="quest-status status-critical">Critical — 5/6</span>
</div>
<div class="quest-desc">Modius controls Sable through the spy assignment, the studio key, and the drawing room surveillance. One more tick and she becomes property, suspect, or sacrifice.</div>
<div class="quest-objective"><strong>Blood sharing violation undiscovered.</strong> Sable feeding Allicia in secret. False reports to Modius. One discovery = crisis.<br><strong>Endgame:</strong> Break free, submit, or find leverage before Baptism by Fire.</div>
</div>


</div>

<div class="quest-section">
<div class="quest-section-title side">Side Quests</div>

<div class="quest-card side-active">
<div class="quest-header">
<span class="quest-name">The FBI Problem</span>
<span class="quest-pc pc-darius">Darius</span>
<span class="quest-status status-advancing">Plan Forming</span>
</div>
<div class="quest-desc">SA William Shepard is investigating the Torch. He has the Warren Birch name. He interviewed Victor. Torch Heat at 5/6.</div>
<div class="quest-objective"><strong>Plan:</strong> Create a Dominated proxy to become Warren Birch. Danov's forger for federal-grade ID (4-6 weeks). Juggler partnered on containment. Proxy candidate TBD.</div>
</div>

<div class="quest-card side-active">
<div class="quest-header">
<span class="quest-name">Handle Marcus Webb</span>
<span class="quest-pc pc-darius">Darius</span>
<span class="quest-status status-critical">Urgent</span>
</div>
<div class="quest-desc">Darius's mortal right hand from before the Embrace. Filed the mortgage assumption. Noticed Darius sounds different on the phone. Chuc Luc: "You will solve it or I will."</div>
<div class="quest-objective"><strong>Options:</strong> Dominate (Condition over weeks). Distance (cut contact). Let Chuc Luc handle it (Marcus dies). The decision defines Humanity 7.</div>
</div>

<div class="quest-card side-active">
<div class="quest-header">
<span class="quest-name">Protect Allicia</span>
<span class="quest-pc pc-sable">Sable</span>
<span class="quest-status status-active">Active</span>
</div>
<div class="quest-desc">Modius is freezing Allicia out. Starving her. Sable is feeding her in secret (Blood Bond Step 1, Allicia to Sable). The drawing room has surveillance.</div>
<div class="quest-objective"><strong>Alliance at 6/6.</strong> Allicia counting words (7). Competing with Modius's 3-step Bond. Must reach crisis point before Baptism by Fire.</div>
</div>

<div class="quest-card side-active">
<div class="quest-header">
<span class="quest-name">Sullivan Dane's Hunt</span>
<span class="quest-pc pc-darius">Darius</span>
<span class="quest-status status-active">Active — 2/6</span>
</div>
<div class="quest-desc">True Faith 5. Burn-scarred. Methodical. Nine months of data. He views vampires with pity, not hatred. That's what makes him terrifying.</div>
<div class="quest-objective"><strong>At 3/6:</strong> Dane appears in 1d4 scenes. <strong>At 5/6:</strong> Actively hunting Darius. Must reach 3/6+ before Baptism by Fire (he watches from a car outside).</div>
</div>

<div class="quest-card side-active">
<div class="quest-header">
<span class="quest-name">Sharon's Vendetta</span>
<span class="quest-pc pc-sable">Sable</span>
<span class="quest-status status-active">Active — 1/6</span>
</div>
<div class="quest-desc">Toreador 7th. Presence 5. Sixty years of rage. She destroyed Sable's paintings. Sent a letter to Denise Price. She's patient. She's precise. She's coming.</div>
<div class="quest-objective"><strong>At 2/6:</strong> Sharon sends a proxy to Gary. <strong>At 4/6:</strong> Sharon arrives personally. <strong>At 6/6:</strong> She moves to destroy Sable.</div>
</div>

<div class="quest-card side-active">
<div class="quest-header">
<span class="quest-name">Sal Cantone's Retaliation</span>
<span class="quest-pc pc-darius">Darius</span>
<span class="quest-status status-advancing">Managed</span>
</div>
<div class="quest-desc">Chicago outfit. His drug pipeline through Berth 7 was stolen. Panel van comes Tuesdays and Fridays. First watcher sent, memory rewritten. Buys about a week.</div>
<div class="quest-objective"><strong>Cantone will escalate.</strong> Second team or comes himself. Outfit money. This thread connects to Chicago (Act II).</div>
</div>

<div class="quest-card side-active">
<div class="quest-header">
<span class="quest-name">The Denise Price Problem</span>
<span class="quest-pc pc-sable">Sable</span>
<span class="quest-status status-active">Active</span>
</div>
<div class="quest-desc">Sable's mother. Hairdresser from Robert Taylor Homes. Found the Gary area code. Called the studio. Sable hung up. Someone gave Denise that number — probably Sharon.</div>
<div class="quest-objective">The phone is unplugged. The problem isn't. A mother's love weaponized by a Toreador elder.</div>
</div>

<div class="quest-card side-active">
<div class="quest-header">
<span class="quest-name">Deliver Lucian's Feeding Rights</span>
<span class="quest-pc pc-darius">Darius</span>
<span class="quest-status status-active">Pending</span>
</div>
<div class="quest-desc">Modius granted annual feeding rights to Lucian. Darius was ordered to deliver the terms. Still undelivered. The ancient Gangrel is waiting.</div>
<div class="quest-objective">Pipeline Exposure at 3/6 triggers Lucian making friendly contact. The delivery and the warning may arrive in the same conversation.</div>
</div>

<div class="quest-card side-active">
<div class="quest-header">
<span class="quest-name">Find Michael Payne</span>
<span class="quest-pc pc-sable">Sable</span>
<span class="quest-status status-active">Escalated</span>
</div>
<div class="quest-desc">Sable's sire. Malkavian 9th. Painter. Absent since the Embrace. Called to Primogen by Sharon. Missing.</div>
<div class="quest-objective">Nobody knows where Michael is. Sharon might. The cemetery scene was the last sighting. A sire who vanishes before his childe learns to survive.</div>
</div>

</div>

<div class="quest-section">
<div class="quest-section-title optional">Optional / Discovered</div>


<div class="quest-card optional-active">
<div class="quest-header">
<span class="quest-name">Mr. White — Milwaukee Buyer</span>
<span class="quest-pc pc-darius">Darius</span>
<span class="quest-status status-locked">Locked — October</span>
</div>
<div class="quest-desc">Pale, old, accented. Buys from the trafficking network twice yearly: October and March. Possible Kindred. Williams's notebook has the schedule.</div>
<div class="quest-objective">October buy window approaching. Connection to Milwaukee (Act IV). Intelligence from the notebook.</div>
</div>

<div class="quest-card optional-active">
<div class="quest-header">
<span class="quest-name">Church Disposal</span>
<span class="quest-pc pc-darius">Darius</span>
<span class="quest-status status-advancing">In Progress</span>
</div>
<div class="quest-desc">Ray Pulaski burns Polk & 13th church before the weekend. Squatter candle or faulty wiring. Destroy the trafficking evidence before someone else finds it.</div>
</div>

<div class="quest-card optional-active">
<div class="quest-header">
<span class="quest-name">Big Six — Mortal Ghost</span>
<span class="quest-pc pc-sable">Sable</span>
<span class="quest-status status-active">Background</span>
</div>
<div class="quest-desc">Marcus Tillman. GD lieutenant. Two near-misses at the Torch. Possessive about Sable since the clubs on 75th Street. The cage was always the same shape.</div>
</div>

<div class="quest-card optional-active">
<div class="quest-header">
<span class="quest-name">Keisha and Amy</span>
<span class="quest-pc pc-sable">Sable</span>
<span class="quest-status status-active">Background</span>
</div>
<div class="quest-desc">Two girls rescued from Williams's church. At the Fifth Avenue studio. Keisha is 16, from Englewood. Amy is ~15, white, not talking. They need placement. Mortal problem in an immortal's world.</div>
</div>

</div>

<div class="quest-section">
<div class="quest-section-title complete">Completed</div>

<div class="quest-card done">
<div class="quest-header">
<span class="quest-name">Blood at Dawn</span>
<span class="quest-pc pc-both">Both PCs</span>
<span class="quest-status status-done">Complete</span>
</div>
<div class="quest-desc">Spirit destroyed. Raymond Falcon delivered. John Wierus exits as a threat. The Torch survived. Five blog posts worth of crisis.</div>
</div>

<div class="quest-card done">
<div class="quest-header">
<span class="quest-name">The Torch Auction</span>
<span class="quest-pc pc-darius">Darius</span>
<span class="quest-status status-done">Complete</span>
</div>
<div class="quest-desc">Mortgage assumed under Warren Birch. $800/month. Lakeside Holdings dissolved. The building belongs to a dead man who doesn't exist.</div>
</div>

<div class="quest-card done">
<div class="quest-header">
<span class="quest-name">Williams Slave Auction</span>
<span class="quest-pc pc-both">Both PCs</span>
<span class="quest-status status-done">Complete</span>
</div>
<div class="quest-desc">Williams delivered to Lucian. Claudette exposed. Church operation burned. Keisha and Amy rescued. FBI tipped. Roger Lister Dominated into confession. 43 entries in a dead man's notebook.</div>
</div>

<div class="quest-card done">
<div class="quest-header">
<span class="quest-name">Allicia Alliance</span>
<span class="quest-pc pc-sable">Sable</span>
<span class="quest-status status-done">Complete — 6/6</span>
</div>
<div class="quest-desc">Blood Bond Step 1 (Allicia to Sable). Fed from Sable in the lake. Seven words counted. The alliance is formed. Now it must be protected.</div>
</div>

<div class="quest-card done">
<div class="quest-header">
<span class="quest-name">Lucian Feeding Rights</span>
<span class="quest-pc pc-darius">Darius</span>
<span class="quest-status status-done">Complete</span>
</div>
<div class="quest-desc">Annual, renewable. Modius's generosity, not Lucian's victory. Brokered by Darius. Accepted by Lucian. "We will not discuss it again."</div>
</div>

<div class="quest-card done">
<div class="quest-header">
<span class="quest-name">Secure The Torch</span>
<span class="quest-pc pc-darius">Darius</span>
<span class="quest-status status-done">Complete</span>
</div>
<div class="quest-desc">Gerald Fisk mesmerized. Mortgage assumed. Victor briefed (kept ignorant). Juggler partnership established. Three-layer ownership: mortgage / night / FBI file.</div>
</div>

<div class="quest-card done">
<div class="quest-header">
<span class="quest-name">Warehouse + Customs Gap</span>
<span class="quest-pc pc-darius">Darius</span>
<span class="quest-status status-done">Complete</span>
</div>
<div class="quest-desc">Found a working pipeline and stole it. Eddie Fells Dominated. Sal Cantone's operation dead. Warehouse operational. Chuc Luc's orders exceeded.</div>
</div>

</div>

---

*Quest log reflects game state as of July 17, 1990. Main quests drive toward Baptism by Fire (NYE 1990). Completed quests leave threads that feed into future arcs.*
