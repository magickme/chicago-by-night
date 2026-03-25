---
title: "Method — How This Chronicle Actually Runs"
url: "/guide/"
hidemeta: true
tags: ["guide", "mythic", "vtm", "solo-rpg", "chicago-by-night"]
summary: "Three engines, two PCs, one LLM Game Master. The complete solo VTM methodology from this chronicle."
ShowToc: true
TocOpen: true
---

This page describes the exact methodology used to run **Forged in Steel** — not a theoretical framework, but what we actually do at the table (which is a terminal and an Obsidian vault). Everything below has been tested across 34 scenes and seven months of in-game time.

---

## The Three Engines

The chronicle runs on three systems simultaneously:

**V20 (Vampire: The Masquerade 20th Anniversary Edition)** handles all game mechanics: dice pools, combat, Disciplines, feeding, Humanity, blood points. Every roll in the chronicle is a V20 roll. The rules are compiled into a single reference file (~800 lines) that the GM reads at session open.

**Mythic Game Master Emulator 2nd Edition** handles story structure: scene checks, Fate Questions, Random Events, Chaos Factor, and the Lists (Threads + Characters). Mythic decides whether the expected scene plays as written, gets altered, or gets replaced entirely by something nobody planned.

**Tourniquet (The Scale)** handles narrative momentum. Every dice roll feeds a running counter from -10 to +10. Positive Scale means things are going the PC's way. Negative means the world is closing in. At the extremes, Major Grace or Major Trouble triggers — the story lurches in a direction determined by oracle rolls, not player planning.

The three engines interact on every roll. You roll V20 dice. The successes/failures determine the fiction. The individual die faces (8-10 add to Scale, 1-3 subtract) move the momentum tracker. And the scene itself exists because Mythic's scene check allowed it.

---

## Two PCs, One Chronicle

The chronicle follows two player characters running parallel storylines in the same city:

**Darius Cole** (Ventrue 10th generation) — the systems guy. Builds pipelines, reads people like balance sheets, operates by the 48 Laws of Power. His storyline is infrastructure: money, docks, cover stories, mortal contacts.

**Sable Price** (Toreador 9th generation) — the survivor. Navigates desire, beauty, and predation. Operates by the Art of Seduction. Her storyline is relationship: the Allicia alliance, the Modius leash, the absent sire, the mother she can never see again.

Scenes alternate between them. Each PC has their own Scale, Chaos Factor, and thread list. They share a Characters List. They intersect at Elysium, joint crisis scenes, and when one PC's actions create consequences the other walks into.

---

## The Session Loop

Every session follows this exact sequence:

### 1. Read the State

Three files, every time:
- **GAME-REFERENCE** — the rules (V20 mechanics, Mythic procedures, Tourniquet, all Disciplines, NPC generation)
- **Session State** — the single source of truth for all mutable data (blood pools, willpower, Scale, Chaos Factor, threat clocks, NPC dispositions, thread progress, story oracles)
- **Voice Reference** — prose style patterns, NPC voice directives, clan-specific writing guides, elder psychology, political dynamics

### 2. Calculate Blood

Deduct 1 blood point per in-game day since the last scene. Vampires burn blood every night upon waking. If blood is low, feeding becomes the scene's first priority.

### 3. Scene Check

Roll 1d10 against the current Chaos Factor:
- **Odd roll ≤ CF** → **ALTERED.** The scene happens but one element changes. Roll on the Scene Adjustment Table (remove/add character, remove/add object, reduce/increase activity, or make two adjustments).
- **Even roll ≤ CF** → **INTERRUPTED.** The planned scene doesn't happen. A Random Event replaces it (roll d100 on the Event Focus Table, interpret through current context).
- **Roll > CF** → **NORMAL.** Play as written.

This means at CF 5 (default), half the scenes get modified. At CF 3, only 30% do. The system self-regulates: when the PC is in control, CF drops, scenes play normally. When chaos rises, scenes mutate.

### 4. Setup

State three things before play begins:
- **Agenda** — what the PC wants this scene
- **Stakes** — what can go wrong
- **Relevant Threads** — which active threads touch this scene

### 5. Play

Back-and-forth between player and GM. The player decides what the PC does. The GM (Claude, the LLM) describes the world, plays NPCs, calls for rolls, and narrates consequences.

Every roll gets recorded in a **Scale Tracker** table:

| Roll | Pool | Result | Dice | Scale Δ | Scale Total | Notes |
|---|---|---|---|---|---|---|
| Man+Subter | 6 | 6 succ | 6,10,8,10,5,8 | +4 | +4 | Credibility check |

Every binary uncertainty gets a **Fate Question**:

> **Fate:** Does Lucian know about the warehouse? Odds: Likely. Roll: 5+2=7, modified 8. **No.**

### 6. Bookkeeping

After play ends, update everything:
- NPC dispositions (who likes you more, who likes you less)
- Threat clock changes (what ticked up, what triggered)
- Chaos Factor adjustment (in control = -1, mixed = unchanged, badly = +1)
- Lists update (add/remove threads and characters)
- Story Oracle changes
- Blood, Willpower, Humanity, XP
- Relationship maps (Mermaid diagrams on the blog)
- Threat clocks page (visual pip displays on the blog)
- Quest log (status updates on the blog)

### 7. Write the Story

After play and bookkeeping, write the scene as finished narrative prose. The play transcript becomes the story — same events, same outcomes, but rendered in the chronicle's literary voice (Ellroy, Raymond, Baldwin, Thompson, Slim, with Ligotti in small doses).

### 8. Publish

Create a Hugo blog post, build locally, deploy to Cloudflare Pages. The chronicle is public.

---

## The Oracle Stack

### Fate Check (Primary Oracle)

Roll 2d10, sum them, apply modifiers.

**Odds modifier** (how likely is this?): Certain (+4) through Impossible (-4).

**Chaos Factor modifier**: CF 1 (-4) through CF 9 (+4). Default CF 5 = +0.

| Modified Total | Result |
|---|---|
| 18-20 | Exceptional Yes |
| 11-17 | Yes |
| 5-10 | No |
| 2-4 | Exceptional No |

**Random Event trigger**: if both d10 show the same number AND that digit ≤ CF, a Random Event fires alongside the Fate answer.

### Random Events

Roll d100 on the Event Focus Table:

| d100 | Focus |
|---|---|
| 1-7 | Remote Event (offscreen, PC learns now) |
| 8-28 | NPC Action |
| 29-35 | New NPC enters |
| 36-45 | Move Toward Thread |
| 46-52 | Move Away from Thread |
| 53-55 | Close Thread |
| 56-67 | PC Negative |
| 68-75 | PC Positive |
| 76-83 | Ambiguous |
| 84-92 | NPC Negative |
| 93-100 | NPC Positive |

The GM interprets the result through current context. "PC Negative" in a scene about the FBI at the Torch means Shepard got there first. "NPC Action" means rolling on the Characters List to see who does something.

### Story Oracle (Custom)

Each PC has a d10 table of personal story prompts. When Major Grace or Trouble fires, roll the Story Oracle first to tie the result to a personal storyline, then roll the Grace/Trouble chart.

### Encounter System

Adapted from Chicago by Night for Gary: roll 2d10, sum for Theme (2-20: Beast, Conspiracy, Desire, Diablerie, Fools, Heroic, Horror, Intrigue, Introductions, Masquerade, Nostalgia, Paranoia, Premonitions, Pursuit, Romance, Secrets, Threats, Vengeance, Weirdness), then 1d10 for the specific encounter within that theme.

---

## The Scale (Tourniquet)

The Scale is a running momentum counter from -10 to +10. It starts at 0 and carries between scenes, resetting only when Major Grace or Major Trouble triggers.

### How It Moves

On every action roll, count the individual die faces:
- Each die showing **8, 9, or 10** adds +1 to the Scale
- Each die showing **1, 2, or 3** subtracts -1
- Dice showing 4-7 don't affect it
- 1s that cancel successes (per V20 botch rules) don't count for Scale

### Burning

If a single roll adds or subtracts 3+ points and those points WON'T drive the Scale to ±10, you can **burn** them for an immediate Minor Grace or Minor Trouble instead of banking them.

### Major Events

At +10: **Major Grace** fires. Roll Story Oracle, then Grace chart. The story lurches in the PC's favor. Scale resets to 0.

At -10: **Major Trouble** fires. Same procedure, opposite direction. Scale resets to 0.

### Grace/Trouble Charts

| d10 | Grace | Trouble |
|---|---|---|
| 1 | Insight (+2 dice or -1 enemy succ) | Trauma (-2 dice penalty) |
| 2 | Vigor (recover health) | Frenzy check |
| 3-4 | Advantage (-2 difficulty) | Undermined (+2 difficulty) |
| 5-6 | Found (clue or item) | Broken (item lost) |
| 7 | Powerful (+2 damage/success) | Threat (new danger) |
| 8-10 | Shift (story moves in PC's favor) | Shift (story moves against PC) |

Minor = one scene. Major = lasting until resolved. Major Shift compounds — reroll for a secondary effect.

---

## Threat Clocks

All pressure tracks run /6. They advance when specific conditions are met and trigger keyed scenes at specific thresholds.

**At 2/6**: the rumor hardens. People start naming the pattern.

**At 4/6**: local heat spills into Masquerade Heat. Hunters, police, and civilians reinforce each other.

**At 6/6**: active crisis. The clock fires and reshapes the board.

### Keyed Scenes

Clocks trigger automatic events:
- **Pipeline Exposure 3/6**: Lucian makes friendly contact (warning)
- **Dane 3/6**: Sullivan Dane appears in the next 1d4 scenes
- **Modius Leash 4/6**: automatic summons to the mansion
- **Masquerade 4/6**: local heat auto-spills +1 to Masquerade; at 6/6 Chicago sends an Archon
- **Sharon 2/6**: proxy arrives in Gary; at 4/6 Sharon comes personally

Current clocks are tracked visually at [Threat Clocks](/clocks/).

---

## NPC System

### Dispositions

Every NPC has an integer disposition from -5 to +5. This number sets the **default odds for Fate Questions** about that NPC's cooperation:

| Disposition | Fate Question Odds |
|---|---|
| +3 or higher | Very Likely |
| +1 to +2 | Likely |
| 0 | 50/50 |
| -1 to -2 | Unlikely |
| -3 or lower | Very Unlikely |

Dispositions update after significant interactions: betrayal -2, favor +1, impressive display +1, insult -1, saving their unlife +3.

### Quick NPC Score

NPCs without full character sheets get a single number that serves as their difficulty, dice pool, and half their auto-successes:

| Score | Type |
|---|---|
| 4 | Skilled adult / mortal professional |
| 6 | Neonate vampire |
| 8 | Experienced vampire |
| 10 | Elder |
| 14 | Ancient |

### GM Personality Directives

Every major NPC has a voice directive that tells the GM (Claude) how to play them:
- **Modius**: paranoid, speaks in implications, never gives direct orders
- **Lucian**: ancient patience, short declarative sentences, knows more than he reveals
- **Juggler**: pragmatic, profane, direct, says what he means
- **Chuc Luc**: cold, transactional, every word is an instruction
- **Sullivan Dane**: quiet, patient, methodical, views vampires with pity

---

## Claude as Game Master

The GM is Claude (Anthropic's LLM). This is not a chatbot playing pretend — it's a structured collaboration:

- Claude reads the complete rules, current state, and voice reference at session open
- Claude plays all NPCs using specific voice directives
- Claude narrates the world using the chronicle's literary style
- Claude calls for rolls, tracks the Scale, asks Fate Questions when binary outcomes matter
- Claude does NOT decide PC actions — the player always decides what their character does
- Claude writes the narrative prose after play, maintaining voice consistency across 30+ scenes

The player rolls physical dice (or types results). The player makes all decisions. The system generates the surprises. Claude weaves it into story.

### What Claude Maintains

After every scene, Claude updates:
- Session state file (all mutable game data)
- Scene file in Obsidian (frontmatter, play log, bookkeeping, narrative)
- Blog post (Hugo page bundle)
- Relationship maps (Mermaid diagrams)
- Threat clocks page (visual pips)
- Quest log (status updates)
- Territory map (if locations change)
- Obsidian canvas (relationship map)

### What the Player Maintains

- Dice rolls
- PC decisions
- Creative direction ("what tone should this scene have?")
- Music selection
- Final approval on all narrative

---

## The Vault

Everything lives in an Obsidian vault with this structure:

```
solo-rpg/
├── vampire/
│   ├── GAME-REFERENCE.md          (rules — immutable)
│   ├── session-state.md           (current state — mutable)
│   ├── WOD-VOICE-REFERENCE.md     (prose style — immutable)
│   └── Chicago by Night/
│       ├── Darius Scenes/         (play logs, 18 scenes)
│       ├── Sable Scenes/          (play logs, 16 scenes)
│       ├── Overview/              (campaign bible, setup docs)
│       ├── NPCs/                  (dossiers by city)
│       ├── Locations/             (by city, with images)
│       ├── Templates/             (scene, NPC, location templates)
│       └── Gary Relationship Map.canvas
├── hugo-site/                     (blog, git submodule)
│   └── content/
│       ├── posts/                 (30 published scenes)
│       ├── reading-order.md       (chronological scene list)
│       ├── quests.md              (quest log)
│       ├── clocks.md              (threat clocks)
│       ├── relationships.md       (Mermaid diagrams)
│       ├── map.md                 (Leaflet.js territory map)
│       └── music.md               (soundtrack by act)
└── scripts/                       (Python utilities)
```

The vault is the source of truth. The blog is the public face. The game is the conversation between a player, a system, and an LLM that reads 800 lines of rules before every session and plays Sullivan Dane with the quiet patience of a man who has been watching the same city for nine months.

---

## What Makes This Work

**Mythic provides surprise.** Without it, a solo game is just writing fiction. The scene check, Fate Questions, and Random Events generate outcomes the player didn't plan and couldn't predict. When a d100 roll of 61 puts the FBI inside the Torch before Darius can brief Victor, that's not authorship — that's play.

**V20 provides weight.** The dice matter. A failed Awe roll costs the Advantage that's been carrying the character for fourteen scenes. A 6-success Mesmerize rewrites a man's will. The mechanics create consequences that the narrative must honor.

**The Scale provides shape.** Without Tourniquet, scenes are flat — things happen, but there's no momentum. The Scale gives every scene a direction. At +7, three points from Major Grace, the dice are loaded with potential. At -4, the world is pressing in. The number changes how the GM narrates: confidence vs. pressure, doors opening vs. walls closing.

**The LLM provides consistency.** Claude maintains NPC voices across 34 scenes, tracks 15 threat clocks, remembers that Victor doesn't know about Warren Birch, and writes prose that doesn't break the fourth wall or use the word "delve." The institutional memory is the difference between a game that drifts and a game that compounds.

**The blog provides accountability.** Publishing every scene means every decision is permanent. You can't retcon a botched Awe roll or a sire's death threat. The public record makes the game real.

> *"The game is the game."*
> — Avon Barksdale (and every vampire in Gary who's figured it out)
