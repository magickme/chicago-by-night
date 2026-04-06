---
title: "Random Tables"
description: "Canonical oracle and encounter tables for Chicago Chronicles, generated from the live vault."
layout: "page"
slug: "random-tables"
menu:
  main:
    weight: 6
    params:
      icon: "hash"
---

*Chicago Chronicles random tables. Generated from the vault's current canonical sources, including live Mythic lists and story oracles from `session-state.md`.*



## Mythic and Tourniquet Core

## FATE CHART (Mythic GME 2E — d100 roll-under)

Roll d100 (percentile). Compare to threshold from the chart below. Roll ≤ threshold = Yes. Roll > threshold = No.
Exceptional results: ExYes = roll ≤ threshold/5 (round down, min 1). ExNo = roll ≥ 100 - floor((100-threshold)/5) + 1.
Example: threshold 50 → ExYes ≤10, Yes 11-50, No 51-90, ExNo 91-100.
Example: threshold 65 → ExYes ≤13, Yes 14-65, No 66-93, ExNo 94-100.
Example: threshold 35 → ExYes ≤7, Yes 8-35, No 36-87, ExNo 88-100.

Fate Chart (Odds vs CF — cell = Yes threshold, roll d100 ≤ this = Yes):

| Odds \ CF | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 |
|---|---|---|---|---|---|---|---|---|---|
| Certain | 85 | 90 | 90 | 90 | 90 | 95 | 95 | 95 | 95 |
| Nearly Certain | 75 | 80 | 80 | 85 | 85 | 85 | 90 | 90 | 95 |
| Very Likely | 55 | 60 | 65 | 70 | 75 | 80 | 85 | 90 | 90 |
| Likely | 35 | 45 | 50 | 55 | 65 | 70 | 75 | 80 | 85 |
| 50/50 | 20 | 25 | 35 | 45 | 50 | 55 | 65 | 70 | 75 |
| Unlikely | 10 | 15 | 20 | 25 | 35 | 45 | 50 | 55 | 65 |
| Very Unlikely | 5 | 8 | 10 | 15 | 25 | 30 | 35 | 40 | 50 |
| Nearly Impossible | 2 | 3 | 5 | 10 | 15 | 20 | 25 | 30 | 35 |
| Impossible | — | 1 | 2 | 5 | 10 | 12 | 15 | 18 | 25 |

Interpreting: Yes = expectation confirmed. Exceptional Yes = yes, intensified to next logical level. No = next most expected outcome. Exceptional No = opposite of Yes, or opposite intensified.
LORE VALIDATION ON EXCEPTIONAL RESULTS: Before narrating an ExYes or ExNo, PAUSE. Check: does this outcome contradict published source material (BbF structure, NPC timelines, faction politics, canon events)? If yes, find a lore-consistent version that preserves the QUALITY of the exceptional result (same narrative impact, different specific form). The oracle says WHAT happens (yes, intensified). The GM must validate HOW it happens against established lore. Do not narrate first and retcon later.
Random Event trigger: doubles on d100 (11, 22, 33, 44, 55, 66, 77, 88, 99) where the single digit ≤ CF. The Random Event occurs IN ADDITION to the Fate answer (roll still answers the question).
When to ask: binary outcome matters, NPC action/knowledge uncertain, coincidence/luck in play, consequences unclear. Don't ask about PC actions or controlled narrative elements.
Fate Questions as RPG rules: treat CF as 5 regardless of actual CF. Treat Exceptional results as regular Yes/No unless the rule uses degrees of success.
Recording format: `**Fate:** [Q]? Odds: [X]. CF: [Y]. Threshold: [T]. d100: [roll]. **[Answer].** [+Random Event if doubles ≤ CF.]`

Quick Yes/No Oracle (d10+modifier) is retained for low-stakes checks where you don't want to risk Random Events.

## RANDOM EVENTS

Trigger: doubles on d100 Fate roll (11, 22, 33...) where single digit ≤ CF, or Interrupted Scene.
Generate: roll Event Focus (d100), then interpret Event Meaning through current Context. The GM (LLM) produces a contextually appropriate interpretation combining an Action concept and a Description concept based on the Event Focus result and the adventure's current situation.
Event Focus Table (d100):

| d100 | Focus |
|---|---|
| 1-7 | Remote Event (offscreen, PC learns now) |
| 8-28 | NPC Action (existing NPC does something; roll Characters List) |
| 29-35 | New NPC (new character enters) |
| 36-45 | Move Toward Thread (closer to resolving; roll Threads List) |
| 46-52 | Move Away from Thread (setback; roll Threads List) |
| 53-55 | Close Thread (resolved or nullified; roll Threads List) |
| 56-67 | PC Negative (bad for PC) |
| 68-75 | PC Positive (good for PC) |
| 76-83 | Ambiguous (unclear, may be foreshadowing) |
| 84-92 | NPC Negative (bad for NPC; roll Characters List) |
| 93-100 | NPC Positive (good for NPC; roll Characters List) |

If rolled Focus references empty List, use Current Context instead.

## SCENE TESTING

Scene Check procedure is in HOW TO RUN A SCENE (step 2). First scene of adventure is NOT tested.
Altered Scene methods: (1) next most expected scene, (2) tweak one element, (3) test alteration as Fate Question, (4) Scene Adjustment Table:

| d10 | Adjustment |
|---|---|
| 1 | Remove a Character |
| 2 | Add a Character |
| 3 | Reduce/Remove an Activity |
| 4 | Increase an Activity |
| 5 | Remove an Object |
| 6 | Add an Object |
| 7-8 | Make 2 Adjustments (roll twice, reroll 7-8) |
| 9-10 | Reroll or choose contextually |

Automatic Interrupt: when you have no idea what happens next, skip CF roll and make next scene an automatic Interrupt.

## THE SCALE

Range: -8 to +8. Carries between scenes. Resets to 0 ONLY after triggering Major Trouble or Major Grace.
The Scale interacts with every action roll the character takes (not soak or willpower rolls).
### Adding Points

On any action roll:
- Each die showing 8, 9, or 10 adds +1 to the Scale
- Each die showing 1, 2, or 3 subtracts -1 from the Scale
- Dice showing 4-7 do not affect the Scale
- Subtract 1s first (per normal VtM botch rules); subtracted dice don't count for Scale
### Triggers

| Condition | Result |
|---|---|
| Hits -8 | Major Trouble triggers. Roll Story Oracle (d10), then Trouble chart (d10). Reset to 0. |
| Hits +8 | Major Grace triggers. Roll Story Oracle (d10), then Grace chart (d10). Reset to 0. |

### Burning the Scale

If adding or subtracting 3+ points and those points will not drive the Scale to ±8, you may burn them instead.
- Grace Burn (+3): Player chooses one — +1 die to next roll, free Discipline activation (if plausible), or +1 NPC disposition shift. Reset Scale to 0.
- Trouble Burn (-3): GM chooses one — -1 die to next roll, Discipline complication, or -1 NPC disposition shift. Reset Scale to 0.
- Must burn ALL points from that roll (cannot partial burn).
- Offer burn concisely (one line, end of roll narration). If player doesn't address within their next message, bank automatically. Don't re-ask or interrupt narrative flow with repeated burn offers.

### Trouble (d10)

| Roll | Result | Minor | Major |
|---|---|---|---|
| 1 | Trauma | fades after scene. | lasting (physical = full rest + 5 BP; mental/social = roleplay recovery + trigger Major Grace). |
| 2 | Frenzy | standard frenzy check at normal diff. | frenzy check at +2 diff. |
| 3 | Hurt | 3 dmg (1d10: 1-5 B, 6-10 L), soak normally. | 6 dmg (same type roll). |
| 4 | Undermined | until successful roll. | until Major Grace. |
| 5 | Broken | retrievable. | gone forever. |
| 6-7 | Threat | equal/weaker, +1 succ needed on next Resisted or +2 diff. | greater, +2 bonus or +2 diff permanently. |
| 8-10 | Shift | narrate shift. | shift + compound (reroll: 1-2 Trauma, 3 Frenzy, 4-5 Hurt, 6-7 Broken, 8-10 Threatened). |

### Grace (d10)

| Roll | Result | Minor | Major |
|---|---|---|---|
| 1 | Insight | +2 dice next roll OR -1 foe succ on next Resisted. | keep Minor for scene OR double for one roll. |
| 2 | Vigor | recover 1 HL. | recover from Trauma OR 3 HL OR heal 1 agg. |
| 3-4 | Advantage | one roll. | until fail/scene end/burn trouble. |
| 5-6 | Found | a clue or non-major item. | major plot element, rare item, or quest resolution if narratively appropriate. |
| 7 | Powerful | +2 dmg or +2 degrees of success. | +4 dmg or +4 degrees. Extra succ can snatch victory from failure. |
| 8-10 | Shift | narrate shift. | shift + compound (reroll: 1-2 Insight, 3-4 Vigor, 5-6 Advantage, 7-8 Found, 9-10 Powerful). |

## ORACLES

Story Oracle (d10): Custom 10-entry table in session-state.md. Roll before Trouble/Grace to tie results to personal storylines. Entry 10 is always "(something new)." Remove resolved entries; fill empty slots with new story elements or roll Reason Oracle.

Reason Oracle (d10): Why is something happening?

| Roll | Source |
|---|---|
| 1 | Concept |
| 2 | Nature |
| 3 | Demeanor |
| 4 | Sire |
| 5 | Clan |
| 6 | Attribute |
| 7 | Ability |
| 8 | Background |
| 9 | Merit or Flaw |
| 10 | Humanity or Path |

Quick Yes/No Oracle (d10+modifier) — use for quick, low-stakes checks where you don't want to risk triggering a Random Event. For narrative Fate Questions during play, use the d100 Fate Chart instead:
Odds modifier: Slim to none -4, Not Likely -2, Don't Know 0, Likely +2, Very Likely +4. Roll 1d10 + modifier. 6+ = Yes.

| Total | Result |
|---|---|
| 0 or under | No, and more bad news |
| 1-2 | No |
| 3-5 | No, but some good news |
| 6-7 | Yes, but some bad news |
| 8-9 | Yes |
| 10+ | Yes, and some good news |

Threats Oracle (d10):

| Roll | Threat | Sub-roll (d10) |
|---|---|---|
| 1 | Supernatural (werewolf, mage, ghost) | — |
| 2-3 | Vampire | 1-2 Elder, 3-6 Ancilla, 7-10 Neonate |
| 4-5 | Ghoul | 1-4 Highly Skilled, 5-10 Average |
| 6-9 | Human | 1-4 Highly Skilled, 5-10 Young/Unskilled |
| 10 | Animal | 1 Exotic/Monstrous, 2-5 Wild, 6-10 Pet |

Clan Oracle (2d10): First roll = sect, second = clan.

| Roll | Sect | Clans (d10) |
|---|---|---|
| 1-5 | Camarilla | 1 Brujah, 2 Gangrel, 3 Malkavian, 4 Nosferatu, 5 Toreador, 6 Tremere, 7 Ventrue, 8 obscure bloodline, 9 Sabbat/Ind defector, 10 Caitiff |
| 6 | Sabbat | 1-3 Lasombra, 4-6 Tzimisce, 7-10 Antitribu |
| 7-8 | Independent | 1-3 Assamite, 4-6 Followers of Set, 7-8 Giovanni, 9-10 Ravnos |
| 9-10 | Anarch | 1-7 roll Camarilla, 8-10 Caitiff |

Encounter System (CbN adapted for Gary): Roll 2d10, sum for Theme (2-20). Then 1d10 for specific encounter.

| 2d10 | Theme |
|---|---|
| 2 | The Beast (hunger, frenzy, loss of control) |
| 3 | Conspiracy (hidden plots, secret meetings) |
| 4 | Desire (want, temptation, obsession) |
| 5 | Diablerie (forbidden hunger, consumption) |
| 6 | Fools (absurdity, ridiculous undead) |
| 7 | Heroic (a chance to do the right thing) |
| 8 | Horror (terror, monstrous, uncanny) |
| 9 | Intrigue (political maneuvering, deals) |
| 10 | Introductions (new NPCs, unexpected arrivals) |
| 11 | Masquerade (threats to the secret) |
| 12 | Nostalgia (memories, mortal life echoes) |
| 13 | Paranoia (surveillance, distrust) |
| 14 | Premonitions (visions, omens) |
| 15 | Pursuit (being chased or chasing) |
| 16 | Romance (connection, vulnerability) |
| 17 | Secrets (discovering hidden truths) |
| 18 | Threats (direct danger, enemies moving) |
| 19 | Vengeance (payback, old debts) |
| 20 | Weirdness (bizarre, unexplained, Malkavian territory) |

Gary Location Map: The Rack = The Torch, Rack strip. Elysium = Modius's mansion. The Hive = Downtown Gary. The Barrens = Wasteland, Telton Cemetery, Docks, abandoned factories. Haven = Darius's haven.

Location Oracle (d10 twice — first roll picks table, second picks entry; table 10 is blank for custom locations):

| Table | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 |
|---|---|---|---|---|---|---|---|---|---|---|
| 1 | Airport | After-Hours Dive Bar | Alley | All-You-Can-Eat Buffet | Amusement Park | Animal Shelter | Aquatics Center | Army Surplus Store | Art Gallery | Art House Cinema |
| 2 | Asylum | Attorney's Office | Bank | Bookstore | Brothel | Bus Station | City Hall | Courthouse | Community College | Crematorium |
| 3 | Doctors Office | Dojo | Docks | Drug Lab | Electronics Shop | Elysium | Ethnic Enclave | Factory | Fashion House | Five-Star Hotel |
| 4 | Front Company | Gas Station | Gun Shop | Hardware Store | Hidden Temple | Homeless Shanty | Hospital | Indy Coffee Shop | Junk Shop | Junk Yard |
| 5 | Laundromat | Library | Mechanic's Shop | Morgue | Museum | Newspaper Office | Nightclub | Nightclub, Trendy | No Tell Motel | Occult Bookseller |
| 6 | Park | Pawnshop | Penthouse Condo | Photo Studio | Place of Worship | Police Substation | Police Station | Powerplant | Private Club | Private Detective Agency |
| 7 | Psychic's Parlor | Public Swimming Pool | Racetrack | Restaurant | Rental Car Service | Roller Rink | Safe House | Sewer | Shooting Range | Slaughterhouse |
| 8 | Slum Housing | Street Corner | Street Food Vendor | Sweatshop | Subway or Rail Station | Taxi Dispatch | Tech-Sector Office | Tenement Squat | Theater | TV or Radio Station |
| 9 | Underground Boxing Club | Underground Nightclub | Underground Parking Lot | University | University Lab | Upscale Neighborhood | Used Car Dealership | Waste Plant | Zoo | — |
| 10 | — | — | — | — | — | — | — | — | — | — |

Personalities Oracle (d10 twice — first roll picks table, second picks entry; blank slots on tables 9-10 for custom archetypes):

| Table | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 |
|---|---|---|---|---|---|---|---|---|---|---|
| 1-2 | Academic | Actor | Artist | Armed Robber | Bodyguard | Burglar | Card Shark | Clown | Club Kid | Comedian |
| 3-4 | Computer Tech | Cowboy | Church Goer | Detective | Dilettante | Doctor | Drifter | Drug Dealer | Farmer | Federal Agent |
| 5-6 | Gang Member | Journalist | Musician | Office Worker | Organized Crime Soldier | Organized Crime Boss | Photographer | Public Official, Local | Public Official, National | Priest |
| 7-8 | Punk | Prostitute | Runaway | Scholar | Soldier | Spouse | Store Clerk | Street Rat | Student | Sycophant |
| 9-10 | Teenager | Truck Driver | TV/Radio News Personality | Uniformed Police Officer | Writer | — | — | — | — | — |

City District Oracle (d10):

| Roll | District |
|---|---|
| 1 | Downtown, Business |
| 2 | Downtown, Neighborhood |
| 3 | Historical |
| 4 | Industrial |
| 5 | Midtown Business |
| 6 | Midtown Neighborhood |
| 7 | Slum |
| 8 | Suburb, new |
| 9 | Suburb, older |
| 10 | Abandoned or Warehouse district |

NPC Behavior (Mythic GME): Know + unimportant = improvise. Know + want to test = Fate Question. No idea = generate via context. Yes=expected. ExYes=expected+intense. No=next-most-expected. ExNo=opposite/intensified. Random Event=additional action.
Threading over inventing: When oracle results require new NPCs or complications, FIRST check: can this be achieved by connecting existing NPCs in a new way? Prefer threading existing characters into novel configurations over introducing standalone new ones. Cross-faction connections produce the strongest engagement.
Published adventure check: When a Fate Question or Random Event touches a PUBLISHED adventure (BbF, Blood at Dawn, Ashes to Ashes, etc.), check the published source structure before narrating. Adding to published material is fine; contradicting it breaks continuity.


## Chicago / Gary Encounter Tables

# Ashes and Blood — Chicago Encounter System

> *"Gary was a cage. Chicago is an arena. Bigger cage, more animals,
> better lighting. Same blood on the floor."*
> — Darius Cole, internal

**Sources:** Chicago by Night 1E (Chapter 5 Encounters), Ashes to Ashes,
Blood Bond, Succubus Club, Mythic GME 2nd Edition (Picard),
Tourniquet Revised (Parigo).

**Usage:** Roll **2d10** and add for a **Theme** (2-20). Roll **d10** for a
specific encounter. Each encounter has a **location type** in parentheses.
Use the Chicago Location Map below to place the scene.

**Scope:** Acts II and III of the campaign. The coterie has left Gary.
Chicago is Lodin's machine, the Succubus Club is the social center,
and two Methuselahs are playing chess with every Kindred on the board.

---

## How It Works

Roll **2d10** and add the results for a **Theme** (2-20). Then roll **d10**
for a specific encounter within that theme. Each encounter has a
**location type** in parentheses — use the Chicago Location Map below to
place the scene in a specific district.

When an encounter says "Roll Characters List," roll d25 against the
Chicago Characters List below. When it says "Roll Story Oracle," use
Darius's Story Oracle from Ashes-and-Blood.md or session-state.md.

**Tone shift from Gary:** Chicago is larger, faster, more layered. Gary
had seven Kindred and twelve blocks that mattered. Chicago has dozens
of Kindred, six Primogen, two Methuselahs, organized crime, federal
surveillance, and the Sabbat probing the perimeter. The encounters
reflect this density. More factions, more angles, more ways to be
destroyed by someone you never saw coming.

The dominant register is **decadence** — excess, corruption,
sophistication covering rot. The Succubus Club is the symbolic center:
a nightclub built on top of a Methuselah's tomb, where Blood Dolls
offer their wrists voluntarily and the music never stops. Gary was
industrial collapse. Chicago is imperial decline.

---

## Chicago Characters List (d25)

| Slot | Character |
|---|---|
| 1 | Lodin (Prince, Ventrue 7th) |
| 2 | Lodin |
| 3 | Ballard (Lieutenant, Ventrue 8th, 500 lbs) |
| 4 | Ballard |
| 5 | Critias (Brujah Primogen, Blood Bound to Menele) |
| 6 | Tyler (Brujah Primogen, secret Sabbat deal) |
| 7 | Annabelle Triabell (Toreador Primogen) |
| 8 | Nicolai (Tremere Primogen) |
| 9 | Kevin Jackson (Ventrue, Cabrini Green, Bloods) |
| 10 | Capone (Ventrue 8th, organized crime) |
| 11 | Chuc Luc (offscreen sire, Ventrue 9th) |
| 12 | Chuc Luc |
| 13 | Helena / "Portia" (Toreador Methuselah, 4th gen) |
| 14 | Menele (Brujah Methuselah, torpored, 4th gen) |
| 15 | Damien (Brujah 6th, apparent age 14) |
| 16 | Gengis (Succubus Club bartender / enforcer) |
| 17 | Sir Henry (ancient Toreador, Succubus Club regular) |
| 18 | Khalid al-Rashid (Nosferatu, sewer network) |
| 19 | Modius (offscreen, Gary Prince, Toreador 7th) |
| 20 | Jefferson Foster (Sabbat Ventrue 9th, offscreen Act II) |
| 21 | Belthazar (Ventrue elder, vendetta) |
| 22 | FBI Agent Shepard |
| 23 | Drummond (Ventrue, eccentric railroad baron) |
| 24 | Sabbat scouts (Rigaud, Wade, embedded) |
| 25 | Society of Leopold (Sayles, Tomba) |

**Weighting rationale:** Lodin and Ballard double-weighted as the
Prince and his enforcer, the two figures most likely to intrude on
any scene. Chuc Luc double-weighted as the offscreen sire whose
pipeline operations drive Darius's arc. Helena and Menele split
across separate slots because their interests diverge. The Sabbat
and hunters occupy single slots — they're present but peripheral
until Act III.

---

## Chicago Threads List

| Slot | Thread |
|---|---|
| 1 | Ashes to Ashes: find the Prince |
| 2 | Ashes to Ashes: find the Prince |
| 3 | Chuc Luc's pipeline (Chicago expansion) |
| 4 | Chuc Luc's pipeline (Chicago expansion) |
| 5 | The cover story (Darius's true generation / sire) |
| 6 | The Methuselah game (Helena vs. Menele) |
| 7 | The Methuselah game (Helena vs. Menele) |
| 8 | Blood Bond web (Lodin, Modius, Jefferson) |
| 9 | Blood Bond web (Lodin, Modius, Jefferson) |
| 10 | Sabbat infiltration (Rigaud, Wade, scouts) |
| 11 | Ballard's coup (undermining the Primogen) |
| 12 | The Succubus Club (social nexus, Helena's vault) |
| 13 | Annabelle's Party (Ballard vs. Toreador Primogen) |
| 14 | Player of Pawns (Critias's chess game) |
| 15 | Paper Chase (Nicolai's Tremere test) |
| 16 | The hunter network (Shepard, Society of Leopold) |
| 17 | Sharon Payne's vendetta (Sable's thread) |
| 18 | Kevin Jackson's territory war |
| 19 | The Anarch Brewery (North Side) |
| 20 | Protect the Masquerade |
| 21 | Gary aftermath (Modius's rage, unfinished business) |
| 22 | Blood Bond (Act III main quest, LATENT until April) |
| 23 | Fundamental Differences (LATENT, Succubus Club) |
| 24 | Death's Sweet Sting (LATENT, Succubus Club) |
| 25 | Grand Elusion (LATENT, Succubus Club) |

**Thread notes:** Act II threads (slots 1-21) are active from January
1992. Act III threads (slots 22-25) activate in April 1992 when the
Sabbat announce themselves. Ashes to Ashes double-weighted because
the kidnapped Prince dominates the first week. The Methuselah game
double-weighted because Helena and Menele touch everything. Chuc
Luc's pipeline double-weighted as Darius's operational spine.

---

## Chicago Location Map

| CbN Location | Chicago Equivalent |
|---|---|
| **The Rack** | Rush Street clubs, The Succubus Club, The Cave, bar scene |
| **Elysium** | Art Institute, Opera House, Museum of Science and Industry |
| **Papillion** | Red light district, Rush Street lower end, Division Street |
| **The Hive** | The Loop, Michigan Avenue, corporate towers, Sears Tower |
| **The Barrens** | Cabrini Green, South Side, industrial districts, Stockyards |
| **Haven** | Coterie's current haven |
| **Anywhere** | Roll Chicago City Oracle |
| **Downtown** | The Loop, State Street, financial district |

---

## Theme Table (2d10)

| 2d10 | Theme | Tone |
|---|---|---|
| 2 | **The Beast** | Hunger, Frenzy, loss of control |
| 3 | **Conspiracy** | Hidden plots, secret meetings |
| 4 | **Desire** | Want, temptation, obsession |
| 5 | **Diablerie** | Consumption of souls, forbidden hunger |
| 6 | **Fools** | Comedy, absurdity, the ridiculous undead |
| 7 | **Heroic** | A chance to do the right thing |
| 8 | **Horror** | Terror, the monstrous, the uncanny |
| 9 | **Intrigue** | Political maneuvering, deals, leverage |
| 10 | **Introductions** | Meeting new NPCs, unexpected arrivals |
| 11 | **Masquerade** | Threats to the secret, mortal attention |
| 12 | **Nostalgia** | Memories, echoes of the past, mortal life |
| 13 | **Paranoia** | Surveillance, distrust, things not as they seem |
| 14 | **Premonitions** | Visions, omens, glimpses of what's coming |
| 15 | **Pursuit** | Being chased or chasing someone |
| 16 | **Romance** | Connection, attraction, vulnerability |
| 17 | **Secrets** | Discovering hidden truths |
| 18 | **Threats** | Direct danger, enemies making moves |
| 19 | **Vengeance** | Payback, grudges, old debts called in |
| 20 | **Weirdness** | The bizarre, the unexplained, Malkavian territory |

---

## Encounter Tables (d10 per theme)

Use these as prompts. "The characters" = the coterie. Adapt freely.

#### THE BEAST

| d10 | Encounter | Location |
|---|---|---|
| 1-2 | **Rush Hour Bloodbath.** A packed Red Line car at midnight. Standing room only, bodies pressed together, arterial heat in the recycled air. The scent of an open wound somewhere in the crowd triggers a Frenzy roll. If the coterie loses control underground, a dozen witnesses have nowhere to run. | The Rack |
| 3-4 | **Succubus Tasting Room.** In the Succubus Club's lower levels, a Blood Doll offers a wrist laced with methamphetamine. One taste and the world turns chemical and bright. Frenzy roll at +2 difficulty. The hallucination period lasts until dawn, and whoever's watching from the balcony above sees everything. | The Rack |
| 5-6 | **The Stockyards at 3 AM.** The old Union Stockyards south of Bridgeport still smell like the killing floor, seventy years later. Animal blood seeps from a rendering plant's drainage pipe. A dozen rats are fighting over the runoff. The Beast responds to the stink of industrial slaughter with something close to nostalgia. Frenzy roll. A Gangrel is already feeding here, and she doesn't share. | Barrens |
| 7-8 | **Soldier Field Aftermath.** A Bears game lets out. Forty thousand drunk humans flood the parking lots in a wash of body heat and spilled beer. The sheer density of prey is staggering. Frenzy roll. Lodin's Sheriff has people watching for exactly this kind of mistake. | The Hive |
| 9 | **The Ghoul Who Bit Back.** A feeding gone wrong in a Gold Coast apartment. The target fought harder than expected, clawing at the coterie member's face, screaming into the pillow. She's someone's wife. The husband is downstairs. There's blood on the Berber carpet and the answering machine light is blinking. | Haven |
| 10 | **Lake Effect.** Walking the lakefront path south of Navy Pier, alone. No mortals, no witnesses. Lake Michigan lies flat and black under a winter sky. The Beast is quiet for once. Then a jogger rounds the bend, headphones in, alone, oblivious. The silence afterward is the worst part. | Anywhere |

#### CONSPIRACY

| d10 | Encounter | Location |
|---|---|---|
| 1-2 | **Ballard's Invitation.** Lawrence Ballard, Lodin's 500-pound lieutenant, summons a coterie member to dinner at Daley's Restaurant. He orders for both of them. He talks about loyalty. He never quite asks a question, but by dessert it's clear he wants the coterie spying on the Primogen. Refusing isn't presented as an option. | The Hive |
| 3-4 | **The Dead Drop.** A sealed envelope appears in the coterie's haven. Inside: a photograph of Chuc Luc's restaurant in New Chinatown, taken from across the street. No note. No sender. Someone knows Darius's connection. | Haven |
| 5-6 | **Capone's Errand Boy.** A Vietnamese man in an expensive suit approaches Darius at a Rush Street bar. He speaks English with a flat Chicago accent. He says Capone wants to discuss the Gary pipeline. He doesn't say how Capone found out. The meeting is tonight, at a meatpacking warehouse in the Back of the Yards. | The Rack |
| 7 | **Critias at the Art Institute.** The Brujah Primogen lingers in front of a Roman bust, comparing it unfavorably to someone he knew in Athens. He seems to be speaking to no one. When the coterie passes, he mentions a name connected to one of their threads. He doesn't look at them when he says it. | Elysium |
| 8 | **The Primogen's Closed Session.** Word reaches the coterie that the six Primogen met without Lodin present. An unprecedented breach of protocol. Nicolai's ghoul whispers that the subject was the coterie specifically. No one will confirm what was decided. | Elysium |
| 9 | **Kevin Jackson's Proposal.** Jackson controls the Cabrini Green projects through the Bloods. He arrives at the coterie's haven uninvited, flanked by two ghouls carrying Uzis under their coats. He offers territory on the South Side. The cost: a favor, unnamed, to be called in later. He smiles like a man who already owns you. | Haven |
| 10 | **The Wiretap.** A sweep of the coterie's haven turns up a listening device. Professional installation, possibly police, possibly Kindred. Tracing the signal leads to a relay in the Loop, rented under a name that traces to the Arcanum. | Haven |

#### DESIRE

| d10 | Encounter | Location |
|---|---|---|
| 1-3 | **The Blood Doll's Plea.** In the Succubus Club's Labyrinth, a mortal recognizes Darius from Gary. She followed a Kindred here two months ago and hasn't left. Track marks on both wrists. She's strung out on Vitae and begging for more, or for someone to take her home. She used to work the pawnshop circuit in Gary. She owes debts she can't pay. | The Rack |
| 4-5 | **Magnificent Mile Window.** Passing the shops on Michigan Avenue, the coterie sees a life they can't return to. A couple laughing in a restaurant window. A child asleep in a stroller. The Ventrue feeding restriction means Darius can only consume people in crisis. These happy mortals are poison to him. The wanting is physical. | The Hive |
| 6-7 | **The Offer from Annabelle.** Annabelle Triabell, Toreador Primogen, invites Sable to a private gathering at her Wicker Park salon. The room smells of oil paint and old money. Annabelle offers mentorship, introduction to Toreador society, a patron's shield. The price is aesthetic loyalty, which means cutting ties with anyone Annabelle deems inelegant. | Elysium |
| 8-9 | **Sears Tower at Midnight.** An invitation to the 107th floor. Lodin's old haven, now sealed but accessible through a service elevator. The view of Chicago at night is a kingdom spread below. Whoever arranged this meeting is offering a glimpse of what it feels like to own a city. Roll Characters List for who's waiting. | The Hive |
| 10 | **Emily Carter.** A woman at the Succubus Club bar orders bourbon and looks at Darius like she's already decided something. She's beautiful, reckless, and carrying Jefferson Foster's blood in her veins. Three drinks, and she'll try to share. | The Rack |

#### DIABLERIE

| d10 | Encounter | Location |
|---|---|---|
| 1-2 | **The Alley Behind the Cave.** Horace's Malkavian bar. In the service alley, a Kindred is pinned against the dumpster by two others. One is feeding from the throat. The other is feeding from the wrist. The victim's aura is being consumed in real time. The attackers see the coterie. They don't stop. | The Rack |
| 3-4 | **Nicolai's Warning.** The Tremere Primogen summons the coterie to a meeting at the Chantry. On his desk: an aura photograph of a Chicago Kindred whose soul-threads are corrupted with black veins. Nicolai identifies them by name. He wants the coterie to confirm it and report. He doesn't say what the Tremere will do after. | Downtown |
| 5-6 | **The Torpored Elder.** Beneath an abandoned factory on the West Side, behind a false wall, a coffin. Inside: a staked Kindred of unknown clan and age. The blood smells ancient. Someone went to great effort to hide this body, and someone else left a trail of breadcrumbs for the coterie to find it. The temptation is a test. Whose test? | Barrens |
| 7-8 | **The Confession.** At Elysium, an ancilla pulls the coterie aside. Shaking hands, dilated pupils. She committed Diablerie three nights ago and can feel the soul of her victim pressing against the inside of her skull. She needs help hiding the evidence before anyone reads her aura. She offers anything. | Elysium |
| 9-10 | **Jefferson's Sermon.** Through Emily Carter or a Sabbat contact, the coterie receives a recorded message from Jefferson Foster. He speaks calmly about the Amaranth as liberation rather than murder. He calls the Camarilla's prohibition cowardice. The recording ends with coordinates to a location outside Chicago. Something is buried there. | Anywhere |

#### FOOLS

| d10 | Encounter | Location |
|---|---|---|
| 1-2 | **The Poseur Prince.** A neonate at the Succubus Club is telling anyone who'll listen that he's Lodin's secret childe. He has the Ventrue bearing, the expensive suit, and nothing behind the eyes. Gengis is watching from behind the bar, deciding whether to let this play out or shut it down. The real danger: Ballard is also watching. | The Rack |
| 3-4 | **Houdini's Last Trick.** Ehrich Weiss, the renegade Tremere formerly known as Houdini, is performing escape acts at The Cave. Chained, staked, locked in a trunk, dumped in Lake Michigan. He keeps escaping. The mortals think it's theater. Nicolai has sent two Gargoyles to retrieve him. The situation is about thirty seconds from catastrophe. | The Rack |
| 5-6 | **L Train Diplomat.** Two Brujah are having a Kindred political argument on a crowded Blue Line car at 1 AM. One of them is shouting about Lodin's Blood Hunt policies. A transit cop is walking through the next car. The mortals are filming on camcorders. Someone has to shut this down before the six o'clock news. | Anywhere |
| 7-8 | **The Ghoul Wedding.** A ghoul is throwing a lavish wedding reception at the Palmer House, funded entirely by stolen Vitae profits. Three Kindred are in attendance pretending to eat. The bride's mortal family keeps asking why the groom's friends are so cold and pale. The champagne toast is imminent and glass-clinking will get awkward fast. | The Hive |
| 9-10 | **Drummond's Party.** Drummond, the eccentric railroad Ventrue, has rented the entire Field Museum for a private soiree. He's dressed a dozen mannequins as guests and is introducing them by name. The hired jazz band is deeply uncomfortable. Real Kindred are arriving and can't tell which figures in the dim exhibit halls are dummies, ghouls, or predators. | Elysium |

#### HEROIC

| d10 | Encounter | Location |
|---|---|---|
| 1-2 | **Cabrini Green Fire.** A high-rise in the projects catches fire on the ninth floor. Families trapped above. Fire department is twenty minutes out. Kevin Jackson's ghouls are evacuating gang members and leaving everyone else. Two children are screaming from a window. Rotschreck check to enter, Humanity check to walk away. | Barrens |
| 3-4 | **The Runaway Fledgling.** A week-old Kindred, Embraced without permission by a Malkavian who vanished, is hiding in a Dumpster behind a Magnificent Mile restaurant. She doesn't know what she is. She fed on her roommate last night and thinks she killed her. She's a Masquerade breach on legs, and if the Sheriff finds her first, she's ash. | The Hive |
| 5-6 | **Neon's Hunger.** Neon, the seven-year-old Caitiff, hasn't fed in four nights. Damien left her in a safe house and hasn't returned. She's tiny and shaking and her eyes have gone solid black. She needs blood. She'll take it from anyone. The moral calculus of feeding a child vampire is not something the Traditions cover. | Barrens |
| 7-8 | **The Mortal Witness.** A homeless man sheltering under the Michigan Avenue bridge saw a Kindred kill someone last night. He told a cop, who didn't believe him. He told a reporter, who is starting to. The man isn't crazy. He's specific. He can describe the killer's face. If the coterie silences him, they protect the Masquerade. If they don't, the killer walks and the Masquerade cracks. | Anywhere |
| 9-10 | **Damien's Stand.** Damien, the 6th-generation Brujah in a fourteen-year-old body, has cornered a pack of three Sabbat scouts in a Lincoln Park alley. He can take them. But one of them is holding a mortal hostage, a teenage girl. Damien won't risk her. He sends word to the coterie: come now, bring muscle, and nobody innocent dies. | Barrens |

#### HORROR

| d10 | Encounter | Location |
|---|---|---|
| 1-2 | **The Sound Beneath the Succubus Club.** In the Labyrinth, the lowest level of the Succubus Club, the walls vibrate with a subsonic pulse. Blood Dolls complain of nausea. Gengis says it's been happening for weeks. The pulse keeps time with a heartbeat, but there's nothing alive down there. Or there shouldn't be. Helena's vault is somewhere below. | The Rack |
| 3-4 | **The L Train at 4 AM.** The coterie boards the Red Line and realizes every passenger in the car is dead. Throats opened, blood pooled on the floor, bodies propped upright in their seats. The train keeps moving. The next station is two minutes away. The conductor's booth is locked and something inside it is still broadcasting the automated stop announcements. | Anywhere |
| 5-6 | **The Meatpacking District.** Following a lead to the old Stockyards, the coterie discovers a cold-storage room containing forty-three body bags hung from ceiling hooks. Each bag holds a drained corpse. The bodies are arranged by blood type, labeled with handwritten tags. Someone has been building a supply chain. The padlock on the door is new. | Barrens |
| 7 | **Michael's Warning.** Michael, the Malkavian child from Gary, appears on a Chicago street corner at 2 AM. He shouldn't be here. He says one sentence, something that makes no sense now but will make terrible sense in three sessions. Then he walks into traffic and vanishes. He was never physically present. | Anywhere |
| 8 | **The Painting.** At Annabelle's Wicker Park salon, a new painting on the wall depicts a scene that hasn't happened yet: the coterie, in a location they recognize, surrounded by fire. The artist is unknown. Annabelle claims it was delivered anonymously. She doesn't seem alarmed. She seems fascinated. | Elysium |
| 9 | **The Nosferatu Tunnels.** Khalid al-Rashid controls the sewer network. The coterie needs passage and pays the toll. Halfway through the tunnel, the guide stops. Ahead, scratched into the concrete walls for a hundred feet, the same word repeated in a language none of them speak. The guide refuses to translate. He says it's a name. He turns around. | Barrens |
| 10 | **The Mirror.** In the coterie's haven, a mirror that used to show nothing now shows something. Not a reflection. A room that doesn't exist in the building, furnished in a style a century out of date. A figure in the room is sitting with its back to the glass. It hasn't moved. It might not be alive. But it wasn't there yesterday. | Haven |

#### INTRIGUE

| d10 | Encounter | Location |
|---|---|---|
| 1-2 | **Lodin's Chessboard.** The Prince summons the coterie to the Prudential Building. The office is all glass and steel, the city spread below like a circuit board. Lodin speaks about Gary, about Modius, about the docks. He knows more than he should. He offers patronage in exchange for complete transparency about the coterie's Gary operations. Complete. | The Hive |
| 3 | **The Anarch Brewery.** The Brujah anarchs operate from an abandoned brewery on the North Side. Damien vouches for the coterie. The anarchs want information on Lodin's security, specifically the police department's nightshift deployment. In exchange: safe passage through the North Side, no questions asked. | Barrens |
| 4 | **Tyler's Game.** Tyler, the Brujah Primogen, approaches Sable at the Art Institute. She's charming, measured, ancient. She asks about the coterie's time in Gary. She mentions Juggler fondly. She never quite says what she wants, but by the end of the conversation, she's planted three ideas that all benefit the Brujah and none benefit Lodin. | Elysium |
| 5 | **The Tremere Test.** Nicolai sends the coterie to retrieve a book from a rare-books dealer in Hyde Park. The book is real but the dealer is a Society of Leopold plant. Nicolai knows this. He wants to see how the coterie handles the trap. Passing means Tremere support. Failing means Nicolai writes them off. | The Hive |
| 6 | **Sir Henry's Grovel.** Sir Henry, the ancient Toreador who haunts the Succubus Club like a powdered ghost, corners the coterie. He claims to have information about the Methuselahs. He wants protection from Ballard, who has threatened to expose his feeding habits. The information might be real. Sir Henry has been in Chicago longer than almost anyone. | The Rack |
| 7 | **The Boon Market.** At Elysium, the coterie witnesses a formal prestation exchange between two elders. One boon is owed for a service rendered during the 1968 riots. The currency of favors becomes suddenly concrete. An intermediary approaches: someone wants to buy a boon the coterie doesn't know they're owed. | Elysium |
| 8 | **Portia's Interest.** The woman the Succubus Club knows as "Portia" watches the coterie from her usual balcony seat. She summons one of them with a nod. Her voice is older than the building. She asks a question about Gary that no one in Chicago should know to ask. She is Helena. She is 2,000 years old. She is interested. This is worse than being ignored. | The Rack |
| 9 | **The Ventrue Board Meeting.** Capone's Ventrue hold an informal directorate in a private room at the Metropolitan Club. Darius is invited as a courtesy to his generation. The agenda: redistribution of feeding rights on the North Side. The real agenda: determining which neonates are assets and which are liabilities. Darius is being assessed. | The Hive |
| 10 | **Gengis's Whisper.** The Succubus Club's bartender, scarred and ancient, slides a folded napkin across the bar. An address. A time. No name. Gengis has survived centuries by knowing everything and saying almost nothing. Whatever is at that address matters, or he wouldn't have written it down. | The Rack |

#### INTRODUCTIONS

| d10 | Encounter | Location |
|---|---|---|
| 1-2 | **The Assamite.** A stranger at Elysium. Dark-skinned, silent, drinking nothing. No one claims him. No one introduces him. When asked his clan, he changes the subject. He's interested in the coterie's reputation. He asks precise questions about Gary's power structure. He smells like old iron. He leaves before dawn and no one remembers exactly when. | Elysium |
| 3-4 | **Inyanga's Summons.** Inyanga, the Toreador elder who watches Chicago for Menele, sends an invitation to her South Side salon. She wants to discuss art, philosophy, the nature of immortality. She's been alive since before the Zulu kingdom. Her real interest is evaluating whether the coterie serves Helena or Menele. They may not know the difference yet. | The Hive |
| 5-6 | **The Giovanni Doctor.** Dr. Genet, Giovanni clan, has recently established a practice in Chicago specializing in "hospice care." She meets the coterie at a fundraising gala. She's warm, professional, and her handshake is cold enough to hurt. She wants allies outside the traditional power blocs. The Giovanni are playing their own game in Chicago, and she needs locals who owe no one. | Elysium |
| 7-8 | **Damien and Neon.** In a parking garage off Rush Street, the coterie encounters Damien carrying Neon on his back. The fourteen-year-old 6th-generation Brujah and the seven-year-old Caitiff are moving safe houses again. Damien sizes up the coterie with the look of someone who has killed ancillae older than their entire lineage. He decides they're useful. He tells them where Belthazar sleeps. | Barrens |
| 9-10 | **The Inconnu Observer.** A woman in a museum gallery, sketching a Caravaggio reproduction. She's been in the same chair for three nights. No one notices her except the coterie. When approached, she identifies herself only as a student of history. She knows every Kindred in Chicago by name and watches the Jyhad the way a naturalist watches an ecosystem. She may be Rebekah of the Inconnu. She may be someone worse. | Elysium |

#### MASQUERADE

| d10 | Encounter | Location |
|---|---|---|
| 1-2 | **The Tribune Reporter.** Joseph Peterson, Ventrue media magnate, controls the Tribune. But a junior reporter has gone rogue, investigating a pattern of exsanguinated bodies found in the Chicago River over six months. The reporter has photographs, autopsy reports, and a theory about a cult. Peterson wants it killed. The reporter's editor is not on the payroll. | The Hive |
| 3-4 | **Rush Street Feeding Gone Public.** A neonate is feeding in a club bathroom on Rush Street. The door wasn't locked. A bouncer walked in with a flashlight. The bouncer is on the floor, unconscious, and two club patrons saw the neonate bolt with blood on her chin. Cell phones don't exist yet, but Polaroid cameras do. | The Rack |
| 5-6 | **The Succubus Club Inspection.** A city health inspector has arrived at the Succubus Club's front door at 11 PM. He has a warrant. Gengis is stalling. The Labyrinth is full of Blood Dolls, and the subbasement contains things no mortal should see. Someone has to make this man leave, forget, or disappear, and each option has a different price. | The Rack |
| 7 | **Campus Witness.** A University of Chicago grad student is writing a thesis on "nocturnal subcultures" and has been hanging around the Rack with a tape recorder. Her field notes contain physical descriptions of six Kindred, accurate enough for identification. She thinks they're a goth community. She's half right. | The Rack |
| 8 | **The Church Vigil.** A Catholic parish on the Near West Side has organized a nighttime vigil against "satanic activity" in the neighborhood. Fifty parishioners with candles, a priest with a bullhorn. The coterie's haven is two blocks away. The priest doesn't have True Faith, but he has a TV crew from WGN. | Haven |
| 9 | **The Coroner's Question.** A Cook County coroner has noticed that bodies drained of blood keep arriving from the same four neighborhoods. She's filed a report with the CPD. Lodin's police contacts should have intercepted it, but someone in the department passed it to the FBI instead. Shepard's name is on the routing. | Anywhere |
| 10 | **Blood in the Snow.** A blizzard blankets Chicago. The coterie feeds and leaves a trail of blood drops in the fresh snow leading directly to their haven. A morning jogger will find it in six hours. The city is still and white and everything is visible. | Haven |

#### NOSTALGIA

| d10 | Encounter | Location |
|---|---|---|
| 1-2 | **Maxwell Street Market.** The Sunday morning flea market where Darius used to buy secondhand suits before the Embrace. The blues musicians are still there, playing Elmore James licks on plywood stages. A vendor is selling something that belonged to someone Darius knew. The sun will rise in four hours and this is the closest he's felt to human since Gary. | Downtown |
| 3-4 | **The Old Neighborhood.** Sable passes through the Robert Taylor Homes, the South Side projects where she grew up. The hallways smell the same. A woman on the seventh floor looks like her mother. The elevator is still broken. Nothing has changed except that Sable feeds on the desperate now instead of living among them. | Barrens |
| 5-6 | **Critias Remembers.** At Elysium, Critias is in a rare mood. He talks about Athens, about the agora, about a philosopher he loved who drank hemlock on principle. The parallel to Chicago's political suicides is not subtle. He's speaking to the room but looking at the coterie. He's been alive 2,400 years and the same patterns still bore him. | Elysium |
| 7 | **The Jazz Club.** A basement bar on the South Side, playing the kind of jazz that doesn't exist above 47th Street. The band is all mortals, all old, and the trumpet player hasn't missed a beat since 1962. The music does something to the Beast, quiets it in a way that feeding doesn't. One of the musicians has a heart condition. His blood pressure is visible in his temples. | Anywhere |
| 8 | **Garfield Park Conservatory.** The greenhouse is open late for a charity event. Tropical heat, living green, the smell of soil and growing things. For five minutes the coterie can pretend the world isn't made of concrete and blood. Then a mortal cuts herself on a rosebush thorn, and the evening changes. | Anywhere |
| 9 | **Chuc Luc's Restaurant.** Darius sits alone in the back of the Vietnamese restaurant in New Chinatown. His sire isn't there. The waitress brings pho that Darius can't eat. The cellar door is locked. The restaurant smells like lemongrass and fish sauce and the life he had before the Embrace, when debts were measured in dollars instead of blood. | Downtown |
| 10 | **The Photograph.** At a thrift store in Pilsen, the coterie finds a framed photograph dated 1943. It shows a group of steelworkers outside U.S. Steel's South Works. In the back row, partially obscured, a face that might be Lodin. The photograph is $3.00. The implications are not. | Downtown |

#### PARANOIA

| d10 | Encounter | Location |
|---|---|---|
| 1-2 | **The Second Shadow.** Walking Michigan Avenue at 2 AM, one of the coterie notices a second shadow where there should only be one. It keeps pace. It turns when they turn. Auspex reveals nothing. The shadow disappears at a crosswalk and doesn't return. It was there. | The Hive |
| 3-4 | **The Familiar Car.** A dark blue Crown Victoria has been parked outside the coterie's haven for three consecutive nights. Illinois plates. No driver visible. On the fourth night, it's gone. In its place: a business card on the sidewalk. FBI Chicago Field Office. Agent William Shepard. | Haven |
| 5-6 | **Nicolai's Files.** Through a contact at the Tremere Chantry, the coterie learns that Nicolai maintains dossiers on every Kindred in Chicago. The contact will let them see their own file for a price. What the file contains is almost certainly incomplete, but what it does contain proves the Tremere have been watching them since Gary. | Downtown |
| 7-8 | **The Replaced Ghoul.** A ghoul the coterie has used as a daytime agent begins behaving differently. Subtle changes: word choice, route to work, a new cologne. Either the ghoul has been replaced, Dominated, or is feeding information to someone else. Investigation confirms at least one of these. Which one depends on who's asking. | Anywhere |
| 9-10 | **The Empty Room.** The coterie arrives at a meeting location to find the room prepared but abandoned. Two chairs, an ashtray with a still-warm cigarette, and a tape recorder running. The tape has forty minutes of silence followed by five seconds of a voice they recognize saying a name they shouldn't know. | Anywhere |

#### PREMONITIONS

| d10 | Encounter | Location |
|---|---|---|
| 1-2 | **The Red Sky.** Driving south on Lake Shore Drive, the coterie sees the sky over Chicago turn the color of arterial blood. It lasts thirty seconds. No mortal seems to notice. The radio plays static for the same duration. When it stops, the announcer is mid-sentence about a warehouse fire on the West Side. The fire won't actually happen for two weeks. | Anywhere |
| 3-4 | **The Malkavian Network.** A Malkavian ancilla corners a coterie member in a bathroom at the Succubus Club. She grabs their wrist and speaks in a voice that isn't hers, reciting a sequence of events that describe something that will happen to the coterie in the next three sessions. She releases the wrist, blinks, and asks what time it is. She remembers nothing. | The Rack |
| 5-6 | **Daysleep Vision.** During daysleep, the coterie member dreams of standing in a room they've never seen. A long table. Six chairs, five occupied. The faces are obscured but the voices are recognizable: the Primogen. They're voting on something. The dreamer's name is mentioned. The vote is three to two. The sixth chair is empty. Then the sun hits the window and the dream burns white. | Haven |
| 7-8 | **The Chess Piece.** Someone leaves a black king on the coterie's doorstep. It matches the set from Lodin's 107th-floor haven. It matches the chess motif from the Methuselah game. It was not there at midnight and it is there at 12:05. No one passed through the door. The piece is cold, colder than the night air. It doesn't warm up. | Haven |
| 9-10 | **Helena's Gaze.** At the Succubus Club, Portia fixes a coterie member with a stare that lasts too long. For a moment, the club falls away and there is only her face, her eyes, and a sensation of falling through two thousand years of accumulated memory. She looks away. She sips her wine. She says nothing. But the coterie member now knows, with absolute certainty, that something is buried beneath the Succubus Club. Something alive. | The Rack |

#### PURSUIT

| d10 | Encounter | Location |
|---|---|---|
| 1-2 | **Rooftop Chase.** A Sabbat scout spotted on a North Side roof. The coterie pursues across a five-block stretch of apartment buildings, jumping gaps, smashing through access doors, dodging clotheslines and pigeon coops. The scout is fast and knows the terrain. If caught, she carries intelligence documents that map Camarilla haven locations across the city. | Barrens |
| 3-4 | **The L Train Escape.** The coterie is cornered in a Rush Street alley by Belthazar's ghouls. The only exit is up, onto the elevated L tracks. An approaching train gives them thirty seconds to run the rails before it arrives. If they make the next platform, they disappear into the crowds. If they don't, the physics of a train are unkind even to Kindred. | The Rack |
| 5-6 | **Lake Michigan at Night.** Someone the coterie is tracking boards a cigarette boat at Burnham Harbor and guns it north into the lake. Pursuing means open water, exposure, and the horizon starting to lighten in the east. The target is heading toward a marina in Evanston. Dawn is in ninety minutes. | Anywhere |
| 7-8 | **The Sewer Pursuit.** Following an informant into the sewer system beneath the Loop. The tunnels branch and rebranch. The informant knows the way. The coterie doesn't. The Nosferatu who control these tunnels haven't given permission to enter. Khalid's people are aware of every footstep. The informant leads them deeper than anyone should go voluntarily. | Barrens |
| 9-10 | **Highway 41.** A car chase south on the Dan Ryan Expressway at 3 AM. Four lanes, light traffic, and the speedometer climbing past 100. The other car is a stolen ambulance and the driver is a ghoul running from a blood hunt. He has information the coterie needs. He also has a shotgun and nothing left to lose. | Anywhere |

#### ROMANCE

| d10 | Encounter | Location |
|---|---|---|
| 1-2 | **The Mortal from Before.** At a Loop restaurant, visible through the glass, someone from Darius's mortal life. An ex-girlfriend, a cousin, a friend from the neighborhood. She's having dinner with a man. She looks happy. She looks alive. Standing on the sidewalk in January, watching through condensation on the glass, the distance between human and Kindred becomes measureable. | The Hive |
| 3-4 | **Annabelle's Confession.** After a Toreador gathering, Annabelle Triabell stays behind. She's been Primogen for decades and the loneliness of office is eating her alive. She speaks about love, about the Embrace, about a mortal she almost saved once. She's looking for someone who still remembers what wanting felt like. She's looking at Sable. | Elysium |
| 5-6 | **The Blood Bond Pull.** A coterie member who has tasted an elder's blood (Lodin, Modius, Jefferson through Emily) feels the Bond stirring. Not compulsion, not yet. Warmth. The desire to be near the source. A pull like homesickness that has nothing to do with home. The elder didn't plan this. Or maybe they did. | Anywhere |
| 7-8 | **The Succubus Club Dance Floor.** 2 AM. The DJ drops something slow and heavy. The lights go low. Two Kindred who've been circling each other for weeks are finally in the same room with nowhere to pretend they haven't noticed. Roll Characters List twice. The attraction is inconvenient, politically dangerous, and entirely real. | The Rack |
| 9-10 | **Sharon Payne's Shadow.** A letter arrives at the coterie's haven addressed to Sable. No return address. The handwriting is precise, feminine, furious. The letter describes Sable's movements over the past week in detail. It ends with: "He chose you. I am going to show you why that was a mistake." Sharon Payne is in Chicago. Sharon Payne has Presence 5. | Haven |

#### SECRETS

| d10 | Encounter | Location |
|---|---|---|
| 1-2 | **The Arcanum File.** A break-in at a Near North academic office yields a file from the Arcanum, the mortal occult research society. The file documents three centuries of "unusual nocturnal activity" in Chicago with maps, dates, and descriptions that correspond exactly to known Kindred territories. Someone in the Arcanum has been doing serious fieldwork. The file names Lodin. | The Hive |
| 3-4 | **The Ledger.** Hidden in a wall safe in an abandoned Capone-era speakeasy on the South Side: a financial ledger. The entries are coded, but a Finance roll reveals they document blood money flowing from Chicago's organized crime families through three shell companies. One of those companies is connected to Chuc Luc's operation. The ledger was hidden in 1979. | Barrens |
| 5-6 | **The Second Childe.** Lodin's ban on new Embraces is absolute. Except it isn't. The coterie discovers that an elder has secretly Embraced a childe within the last year. The childe is hidden in a penthouse on the Gold Coast, educated by ghouls, and has never met another Kindred. Roll Characters List for the sire. The childe doesn't know the Embrace was illegal. | Haven |
| 7 | **Portia's True Name.** Through research at the Newberry Library or a slip from Sir Henry, the coterie pieces together that "Portia" at the Succubus Club is Helena, the 4th-generation Toreador Methuselah. The oldest vampire in Chicago. The one who has been watching them since their first night at the club. Knowing her name is dangerous. Not knowing was worse. | Elysium |
| 8 | **The Tunnel Map.** A Nosferatu trades information: a partial map of the tunnel network beneath Chicago. The map marks three locations with red circles. Two are known Kindred havens. The third is beneath the Succubus Club, at a depth that shouldn't be structurally possible. The Nosferatu wants a favor for the map. He won't say from whom. | Barrens |
| 9 | **Ballard's Weakness.** A source inside the Ventrue reveals that Ballard, Lodin's seemingly invulnerable lieutenant, is being blackmailed. The blackmailer has evidence of something Ballard did during the 1968 riots. The evidence is in a safety deposit box at First National Bank. The box number is included. The source wants the coterie to steal it. | The Hive |
| 10 | **The Unsent Letter.** Among the possessions of a destroyed Kindred: a letter to Modius in Gary, never mailed. The letter describes Chicago's true power structure with an accuracy that suggests the writer had centuries of observation. The letter warns Modius about something coming. The letter is dated six months ago. The writer was destroyed three months ago. Roll Characters List. | Anywhere |

#### THREATS

| d10 | Encounter | Location |
|---|---|---|
| 1-2 | **Bach's Riders.** The Sabbat biker gang rolls down Michigan Avenue at 2 AM, twelve Harleys in formation. They don't attack. They don't stop. They ride the full length of the Magnificent Mile, past the Water Tower, past the Drake Hotel, past every Elysium-adjacent location in the city. A declaration of presence. A promise. The Sheriff's ghouls watch from unmarked cars and do nothing. | The Hive |
| 3-4 | **The Marked Haven.** Someone has spray-painted a symbol on the building where the coterie sleeps. The symbol is the Sabbat sword-and-sun. Below it, a date. The date is three nights from now. The paint is fresh and the security cameras show static for the relevant fifteen minutes. | Haven |
| 5-6 | **Belthazar's Retribution.** If Damien staked Belthazar during Ashes to Ashes and he's free, he's hunting the coterie now. A ghoul delivers a package: a rat's skull with human teeth glued into the jaw. Belthazar's calling card. He knows where they sleep. He's older, stronger, and has the patience of centuries. He also has a sense of humor, which makes him worse. | Haven |
| 7-8 | **The Society of Leopold.** Sayles and Tomba, Society of Leopold operatives, have set up surveillance in a van outside the Succubus Club. They've been photographing everyone entering after midnight. Their van is parked in a legal space and they have legitimate press credentials. Destroying the photographs is easy. Destroying the negatives at their hotel requires breaking and entering. Destroying the operatives brings the full Society. | The Rack |
| 9 | **Lodin's Ultimatum.** The Prince sends word through Ballard: the coterie has seventy-two hours to declare formal allegiance. Swear a blood oath to Lodin, or be classified as unaffiliated. In Chicago, unaffiliated means unprotected. The oath includes a feeding, which means one step closer to a Blood Bond. The clock starts now. | Anywhere |
| 10 | **The Lupine Border.** Driving through the northern suburbs after a meeting, the coterie's car breaks down in forest preserve territory. The trees are old-growth and the silence is wrong. Something large moves in the underbrush. Lupine territory begins north of the city and the border is not marked on any map a Kindred would carry. Dawn is three hours away. The next gas station is a two-mile walk. | Anywhere |

#### VENGEANCE

| d10 | Encounter | Location |
|---|---|---|
| 1-2 | **Modius's Rage.** A letter arrives from Gary, delivered by a Kindred courier. Modius knows the coterie carried his message to Chicago and it was ignored. He blames them. The letter is formal, cold, and includes a demand: return to Gary within the month and answer for the insult, or Modius will send Lucian. Lucian is six hundred years old and he doesn't deliver messages. | Anywhere |
| 3-4 | **The Gary Anarchs in Chicago.** Juggler's people have followed the coterie to the city. They want to know what Modius's letter to Lodin actually said. They believe the coterie is working for the prince who kept them in a cage. The confrontation happens in a warehouse on the North Side, and Juggler's representative has Potence 3 and a grudge. | Barrens |
| 5-6 | **Ballard's Memory.** Ballard remembers an insult, real or imagined, from the coterie's first week in Chicago. He engineers a minor disaster, a permit violation at the haven, a ghoul arrested on a fabricated charge, a critical contact blacklisted. The damage is specific and surgical. Ballard doesn't need to throw a punch. He controls the machinery. | The Hive |
| 7-8 | **The Betrayed Contact.** A mortal the coterie used and discarded in Gary or early Chicago has found them. He's sober, furious, and carrying a tape recorder with conversations the coterie assumed were private. He wants money. He wants an apology. He'll settle for revenge. He doesn't know what the coterie is, but he knows where they live. | Haven |
| 9-10 | **Blood Hunt.** Lodin declares a Blood Hunt on a Kindred the coterie has ties to. Roll Characters List. The target is now fair game for any Kindred in Chicago. Helping them means defying the Prince. Abandoning them means losing an ally, and trust, and possibly the last person in the city who would have done the same for them. | Anywhere |

#### WEIRDNESS

| d10 | Encounter | Location |
|---|---|---|
| 1-2 | **Mass Frenzy at the Succubus Club.** Every Kindred in the building simultaneously enters Frenzy. No visible trigger. The mortals on the dance floor become prey. Gengis, the oldest and strongest, is the last to lose control. It lasts ninety seconds. When it stops, six Blood Dolls are dead and no one can explain what happened. The subsonic pulse from the basement is louder than before. | The Rack |
| 3-4 | **The Dead Bird Migration.** Thousands of starlings fall dead from the sky over Grant Park at midnight. They land in a rough circle two hundred feet in diameter. The center of the circle is warm, ten degrees warmer than the surrounding air. The warmth fades by dawn. The Park District will find the birds in the morning. The news will call it environmental poisoning. It isn't. | Anywhere |
| 5-6 | **Chinatown Exorcism.** In Bridgeport, near Chuc Luc's territory, a Taoist priest is conducting a street-corner exorcism on a storefront. The ritual works. Something leaves the building, something visible only to Kindred with Auspex, and it moves through the crowd like smoke through a grate. It pauses near the coterie. It recognizes them as dead things. Then it moves on. | Downtown |
| 7 | **The Stopped Clock.** Every clock in the coterie's haven stops at the same time: 3:17 AM. Watches, wall clocks, the VCR, the microwave. They resume ten minutes later, all synchronized, as if nothing happened. The next night, it happens again. Same time. A newspaper from 1929 mentions a fire at this address at 3:17 AM. Everyone inside died. | Haven |
| 8 | **The Sears Tower Whisper.** At the top of the Sears Tower observation deck, alone after hours, a coterie member hears whispering. Not from the vents, not from below. From the glass. The words are indistinct but the tone is instructional, as if someone is explaining how the city works to someone who isn't there yet. The whispering stops when a second person enters the room. | The Hive |
| 9 | **The Awakened Gargoyle.** A stone gargoyle on the facade of the Tribune Tower blinks. Not a trick of light. Not a pigeon. It blinks, turns its head two inches to the left, and resumes its original position. A Tremere creation, escaped or abandoned. It's been watching Michigan Avenue for decades. It may be reporting to Nicolai. It may have stopped reporting to anyone. | The Hive |
| 10 | **The Woman on the Lake.** At 4 AM, from the lakeshore path, the coterie sees a woman standing on the surface of Lake Michigan, fifty feet from the breakwall. She's wearing a white dress. She's looking at the city. She's dry. The water doesn't move around her feet because her feet don't touch it. She turns, sees the coterie, and walks toward the horizon. She does not sink. She does not return. Nothing about this fits any Kindred, Lupine, or mortal explanation the coterie possesses. | Anywhere |

---

## Chicago City Oracle (d10)

| d10 | District |
|---|---|
| 1 | The Loop / State Street (financial district, skyscrapers, daytime power) |
| 2 | Rush Street / Near North (nightlife strip, Succubus Club, The Cave) |
| 3 | Magnificent Mile / Gold Coast (wealth, Elysium, elder havens) |
| 4 | Cabrini Green / Near West (projects, gangs, Kevin Jackson's domain) |
| 5 | Chinatown / Bridgeport (Chuc Luc's territory, ethnic neighborhoods) |
| 6 | South Side / Hyde Park (university area, residential, feeding grounds) |
| 7 | Lakefront / Grant Park (open exposure, dawn danger, scenic meetings) |
| 8 | North Side / Lincoln Park (Anarch territory, Brewery, suburban interface) |
| 9 | Industrial corridors / Stockyards (abandoned factories, Nosferatu tunnels) |
| 10 | Suburbs / Outskirts (Hell's Pasture, rural compounds, Lupine border) |

---

## Key Chicago Locations

Brief reference for locations that appear repeatedly in the encounter
tables. Full dossiers should be created in `Locations/Chicago/` as
they come into play.

**The Succubus Club.** Nightclub at the center of Kindred social life.
Three levels: the main floor (dance music, mortals and Kindred mixing,
feeding happens openly if you know where to look), the balcony
(reserved for elders, Portia's permanent table), and the Labyrinth
(underground, Blood Dolls, drug-adjacent Vitae culture, and deeper
still the entrance to Helena's vault). Gengis tends bar and enforces
the peace. The subsonic pulse from below has been getting louder. The
club is simultaneously the safest and most dangerous place in Chicago:
everyone is watching, and everyone has something to hide.

**The Cave.** Horace's Malkavian bar. Dark, strange, performance-art
atmosphere. Houdini does escape acts. The clientele skews Malkavian
and the conversations are difficult to follow. Useful for weird
encounters, information that arrives in riddled form, and the feeling
that reality is thinner than usual.

**The Prudential Building.** Lodin's base of operations. Top floors.
Glass and steel and the view of a city he owns. Security is layered:
mortal guards, ghouled police, Dominated building staff. Getting an
audience with the Prince requires an invitation. Getting out requires
his permission.

**Sears Tower, 107th Floor.** Lodin's former haven. Sealed since the
events of Ashes to Ashes. The seven-ton vault door was ripped open by
someone with Potence 7+. The crime scene is technically cold, but
whatever happened there left a psychic residue that Auspex-sensitive
Kindred can feel in the elevator.

**The Anarch Brewery.** Abandoned brewery on the North Side. Damien
and the Brujah anarchs use it as a headquarters. Fortified, watched,
and full of Kindred who remember what Lodin did in 1968. The
architecture is industrial and the politics are revolutionary.

**Cabrini Green.** The Robert Taylor Homes and surrounding projects.
Kevin Jackson's domain. The Bloods gang is his mortal army.
Feeding is easy here. Getting out with your conscience intact is harder.
The poverty is real and the desperation makes every mortal a potential
meal for Darius's Ventrue restriction.

**The Tremere Chantry.** Nicolai's headquarters. Location shifts
depending on the source, but functionally: a secured building in the
Loop or Near North with warded rooms, bound spirits, and Gargoyle
sentries. The Tremere don't invite visitors. They summon subjects.

**The Art Institute / Opera House.** Elysium locations. The Traditions
apply here with extra force. No violence, no feeding, no politics
conducted above a whisper. In practice, everything is politics, and
the whispers carry more weight than the shouting outside.

**The Stockyards / Industrial Corridors.** South Side. The old Union
Stockyards, meatpacking plants, abandoned factories. Nosferatu tunnels
connect to the sewer network beneath. This is where bodies are hidden,
where the Nosferatu trade information, and where things that don't
belong in polite Kindred society get done. The smell of old blood never
quite fades.

---

## Chicago NPC Quick Reference

Voice and roleplaying notes for NPCs who appear in the encounter tables.
Full dossiers should be created in `NPCs/Chicago/` as they become
active in play.

| # | Character | Quick Profile | How to Voice |
|---|---|---|---|
| 1 | **Lodin** | Ventrue 7th. Prince of Chicago. Rules through Dominate 6 and the police department. Paranoid, effective, aging out of relevance. | Corporate authority. Every sentence is an instruction, even when it sounds like a question. Never raises his voice. The anger is in what he doesn't say. |
| 2 | **Ballard** | Ventrue 8th. Lodin's lieutenant. 500 pounds, wheezing, brilliant. Controls the city's bureaucratic machinery. | Heavy breathing between sentences. Jovial surface, calculating underneath. Orders food for other people. Talks about loyalty the way a butcher talks about livestock. |
| 3 | **Critias** | Brujah Primogen. 2,400 years old. Blood Bound to Menele. Classical philosopher trapped in a modern city. | Weary intellectual. References Athens the way old men reference the war. Every political observation is also a lament. Speaks to the coterie like students he hasn't decided to fail yet. |
| 4 | **Tyler** | Brujah Primogen. Ancient, charming, secretly dealing with the Sabbat. | Warm, measured, motherly. Never in a hurry. Plants ideas like seeds and walks away. Ask about Juggler to see her mask slip for half a second. |
| 5 | **Annabelle Triabell** | Toreador Primogen. Art patron. Lonely at the top. | Generous hostess. The warmth is real, which makes it dangerous. She wants to be loved and she's powerful enough that her desire reshapes the room. |
| 6 | **Nicolai** | Tremere Primogen. Runs the Chantry. Uses everyone as test subjects. | Clinical. Precise. Never explains himself. Asks questions he already knows the answer to. The silence after you answer tells you whether you passed. |
| 7 | **Kevin Jackson** | Ventrue 8th. Controls Cabrini Green through the Bloods gang. | Street general. Code-switches between boardroom and block. The smile is a weapon. He already has what he wants; the meeting is about letting you know. |
| 8 | **Capone** | Ventrue 8th. Organized crime. Chuc Luc's sire. Rumored to seek Golconda. | Old Chicago. Italian accent smoothed by decades. Speaks quietly because everyone is already listening. Mentions loyalty to his people and means it in a way that excludes you. |
| 9 | **Helena / Portia** | Toreador 4th gen. Methuselah. 2,000+ years old. Watches from the Succubus Club balcony. | Ancient stillness. Speaks rarely. When she does, every word has been chosen over centuries of practice. Her attention feels like sunlight through a magnifying glass. |
| 10 | **Gengis** | Succubus Club bartender/enforcer. Scarred. Ancient. Knows everything. | Monosyllabic. Slides things across the bar. Communicates through what he pours and what he withholds. A nod from Gengis is worth more than a speech from anyone else. |
| 11 | **Sir Henry** | Ancient Toreador. Succubus Club fixture. Powdered, pathetic, surprisingly informed. | Faded grandeur. Speaks in elaborate courtesies that haven't been fashionable since the 18th century. Grasps at sleeves. The desperation is real, and so is the memory. |
| 12 | **Damien** | Brujah 6th gen. Apparent age 14. Phenomenally strong. Protects Neon. | Teenager's vocabulary, tactician's mind. Sizes people up in seconds. Loyal to exactly three people and will kill anyone who threatens them. Speaks in short, flat sentences when he's angry, which is often. |
| 13 | **Khalid al-Rashid** | Nosferatu. Controls the sewer network. Information broker. | Rarely seen. Communicates through intermediaries. When he does appear, speaks formally in a voice that echoes as if the tunnels are still around him. The price for passage is always information, never money. |
| 14 | **Drummond** | Ventrue. Eccentric railroad baron. Rich, strange, possibly senile. | Victorian diction. Introduces furniture by name. Throws lavish parties for imaginary guests. Accidentally brilliant twice a night. The madness might be an act. Nobody has tested the theory. |
| 15 | **Jefferson Foster** | Ventrue 9th. Sabbat. Acts II-III background, then foreground. | Calm preacher. Speaks about the Sabbat with the certainty of a convert. Never threatens. Offers. The offer is always worse than the threat would have been. |

---

## Notes on Chicago Encounters

**Scale:** Gary had one prince, one nightclub, and seven Kindred
fighting over scraps. Chicago has a Prince who rules through the
police department, six Primogen who scheme behind his back, two
Methuselahs older than Christianity, a Sabbat infiltration in
progress, and nightlife venues where Kindred feed openly on willing
mortals. Encounters should reflect this scale. A conspiracy in Gary
was two vampires whispering. A conspiracy in Chicago involves shell
companies, wiretaps, and the federal government.

**The Succubus Club:** Chicago's social center. Three levels: the
dance floor (mortals and Kindred, loud music, feeding opportunities),
the balcony (elders watching, Portia/Helena in her usual seat), and
the Labyrinth (underground, Blood Dolls, the entrance to something
beneath). Most Rack encounters default here unless specified otherwise.
Gengis tends bar and knows everything. Sir Henry haunts the corners.
The music covers the screaming.

**Act II vs. Act III tone:** Act II encounters trend toward investigation,
political maneuvering, and the coterie establishing themselves. Act III
encounters grow more violent as the Sabbat announce themselves. When
running Act III, weight the d10 rolls: on a result of 9-10 in any theme,
consider adding a Sabbat element. Bach's bikers, Jefferson's influence
through Emily, the Creation Rite's shadow over every encounter.

**The Ventrue feeding restriction in Chicago:** Darius can only feed
on people who owe debts they can't pay. In Gary, the entire city
qualified. In Chicago, the Gold Coast and Magnificent Mile are full of
solvent professionals. Darius's hunting grounds narrow to Cabrini Green,
the South Side, Chinatown's gambling debts, and the service workers
crushed between rent and the wrong end of the L line. This restriction
should make hunting scenes feel different in Chicago: harder, more
targeted, requiring Streetwise or Empathy rolls to identify valid prey.

**Cross-referencing with Gary tables:** If the coterie returns to Gary
for any reason, use the encounter tables from Forged-in-Steel-Mythic-
GME-Setup-v3. If a Chicago encounter generates a Gary-connected NPC
(Modius, Lucian, Juggler), the scene occurs in Chicago but the NPC's
presence raises immediate questions about what's happening back home.

---

## Supplemental Oracles

### Threat Oracle (d10)

| d10 | Threat Source |
|---|---|
| 1 | Sabbat (scouts, bikers, embedded agents) |
| 2 | Society of Leopold (Sayles, Tomba, new operatives) |
| 3 | FBI (Shepard, federal investigation) |
| 4 | Lupines (border incursion, territorial response) |
| 5 | Anarch factions (Brewery, Damien's network) |
| 6 | Tremere internal politics (Nicolai's tests) |
| 7 | Ventrue power struggle (Ballard, Capone, Jackson) |
| 8 | Methuselah interference (Helena or Menele's proxies) |
| 9 | Chicago PD (Lodin's police contacts, or rogue cops) |
| 10 | Unknown (something new, generate via Mythic) |

### Clan Oracle (d10)

| d10 | Clan |
|---|---|
| 1 | Ventrue |
| 2 | Brujah |
| 3 | Toreador |
| 4 | Tremere |
| 5 | Nosferatu |
| 6 | Malkavian |
| 7 | Gangrel |
| 8 | Caitiff |
| 9 | Giovanni / Independent |
| 10 | Sabbat clan (Lasombra, Tzimisce, or antitribu) |

### Reason Oracle (d10)

When the encounter calls for a motive and none is obvious, roll d10.

| d10 | Reason |
|---|---|
| 1 | Hunger (blood, Vitae, resources) |
| 2 | Fear (exposure, destruction, loss of status) |
| 3 | Ambition (power, territory, generation) |
| 4 | Loyalty (sire, coterie, faction, Blood Bond) |
| 5 | Vengeance (old grudge, recent betrayal) |
| 6 | Curiosity (forbidden knowledge, the occult) |
| 7 | Love (mortal attachment, Kindred obsession) |
| 8 | Duty (Traditions, clan obligations, boons owed) |
| 9 | Survival (immediate threat, dawn approaching) |
| 10 | Madness (the Beast, Malkavian insight, broken mind) |

---

## Source Material

- [[Chicago by Night]] — Encounter system adapted from Chapter 5
- [[Ashes to Ashes]] — Scene locations
- [[V20]] — Mechanics reference

---

## Unchanged Sections

The following sections from **Forged-in-Steel-Mythic-GME-Setup-v3**
are unchanged and should be used as-is with the Chicago encounter
system. They are not repeated here:

- **VTM Solo Rules** (player-facing rolls, resisted actions, combat,
  Quick NPC generation, experience, Humanity tracking)
- **The Scale** (-10 to +10, Trouble/Grace charts)
- **Mythic GME Cheat Sheet** (Fate Chart, CF adjustment, Random Event
  Focus, Scene Check)
- **Replacing Overlapping Systems** table
- **Play Loop** flowchart
- **Darius's Story Oracle** (d10)
- **Sable's Story Oracle** (reference her PC file)

## Chicago City Oracle (d10)

| d10 | District |
|---|---|
| 1 | The Loop / State Street (financial district, skyscrapers, daytime power) |
| 2 | Rush Street / Near North (nightlife strip, Succubus Club, The Cave) |
| 3 | Magnificent Mile / Gold Coast (wealth, Elysium, elder havens) |
| 4 | Cabrini Green / Near West (projects, gangs, Kevin Jackson's domain) |
| 5 | Chinatown / Bridgeport (Chuc Luc's territory, ethnic neighborhoods) |
| 6 | South Side / Hyde Park (university area, residential, feeding grounds) |
| 7 | Lakefront / Grant Park (open exposure, dawn danger, scenic meetings) |
| 8 | North Side / Lincoln Park (Anarch territory, Brewery, suburban interface) |
| 9 | Industrial corridors / Stockyards (abandoned factories, Nosferatu tunnels) |
| 10 | Suburbs / Outskirts (Hell's Pasture, rural compounds, Lupine border) |

---

## Mortal Noise

# Chicago 1991 Headlines

Use one headline at scene open to add mortal friction unrelated to the Jyhad. The city should keep moving even when Kindred politics are quiet.

| Roll | Headline | Street Effect | Pressure |
|---|---|---|---|
| 1 | Drive-by on the South Side | Blue lights, crime tape, and Channel 7 vans clog two blocks. Witnesses scatter before cops arrive. | Sirens, helicopters, jumpy patrol cars on every cross street. |
| 2 | CTA service disruption | L trains stopped between stations, buses rerouted. Commuters spill into the cold, angry and stranded. | Crowds on platforms, taxi shortages, foot traffic in unexpected places. |
| 3 | Aldermanic corruption indictment | Federal courthouse swarming with press. City Hall staff making calls they don't want overheard. | More suits downtown, more nervousness in ward offices, more paper shredders running. |
| 4 | Cabrini-Green shooting | Projects locked down. Police flood the high-rises. Mothers pull children off the gallery walkways. | Checkpoints, hostile cops, residents who've stopped talking to strangers. |
| 5 | Lake-effect snow warning | Six inches expected by morning. Salt trucks out early. The Dan Ryan slows to a crawl. | Reduced visibility, abandoned cars, empty streets after midnight. |
| 6 | Union rally at McCormick Place | Teamsters, SEIU, and building trades march for contract renewal. Traffic diverts through the Loop. | Picket noise, rerouted buses, off-duty cops earning overtime. |
| 7 | House fire in Pilsen | Three-flat gutted. Two families displaced. Arson suspected but unconfirmed. | Smoke smell carries six blocks. Fire trucks, onlookers, Red Cross van. |
| 8 | Crack bust on West Madison | Tactical unit raids a known house. Dealers scatter. Customers too. Everything within four blocks goes quiet. | Empty corners, nervous foot traffic, squad cars parked with engines running. |
| 9 | Bulls game at the Stadium | 18,000 people pouring onto Madison after the final buzzer. Bars overflowing. Traffic impossible. | Crowds, noise, easy cover, drunk pedestrians, scalpers and pickpockets working the exits. |
| 10 | Factory closing in Back of the Yards | Third plant this year. Two hundred jobs gone. The bar on Ashland is full by five PM. | Anger without a target. Men drinking on a Tuesday. Hiring signs that aren't there. |
| 11 | GD-BD turf war flare-up | Shots fired near 63rd and Halsted. Four wounded, none dead. Retaliation expected by morning. | Gang activity, corner lookouts, cars moving too slow or too fast. |
| 12 | Homeless camp cleared under Wacker | City crews with dump trucks. Forty people scattered into the cold. Some drift toward shelters. Some don't. | Displaced people in doorways, under viaducts, in L stations. Cops pushing them along. |
| 13 | Water main break in the Loop | Jackson Boulevard flooded curb to curb. Steam rising. ComEd cutting power to the block. | Detours, darkness, utility crews with flashlights, impatient taxi drivers. |
| 14 | Mayoral press conference on crime stats | Daley at City Hall, cameras rolling. Numbers down on paper, up on the street. Nobody believes either. | More patrol presence for 48 hours. Then back to normal. |
| 15 | El Rukn trial coverage | Federal building security doubled. Spectators line up at 6 AM. Jeff Fort's name on every newscast. | Courthouse district crawling with feds, marshals, reporters. Everyone being watched. |
| 16 | Cold snap advisory | Wind chill below zero. Warming centers open. The lakefront is empty and dangerous. | Fewer pedestrians, faster walks, nobody lingering. Cars won't start. |
| 17 | Restaurant health code scandal | Tribune runs an expose. Three Gold Coast restaurants closed. The owner knows an alderman. | Health inspectors visible. Kitchen staff nervous. Reservations cancelled. |
| 18 | CHA maintenance protest | Robert Taylor Homes residents block State Street with signs. Broken elevators, no heat, rats. | Traffic diversion, TV cameras, police keeping distance. Politicians absent. |
| 19 | Jazz funeral procession on the South Side | Second-line parade for a beloved musician. Brass band, two hundred people, streets closed for an hour. | Music, crowds, genuine grief. A neighborhood remembering someone who mattered. |
| 20 | Stockyards methane leak | Industrial corridor evacuated three blocks. Hazmat trucks. The smell is worse than the danger. | Closed streets, emergency lights, residents in bathrobes on the sidewalk. |

## Live Mythic Lists

### Darius Threads

|Slot|Thread|Progress|
|---|---|---|
|1-2|Cover story under scrutiny (2x)|OPEN. Warren Birch built for Gary. Chicago has 100 Kindred with Auspex. Critias now aware.|
|3-4|Chuc Luc's pipeline (2x)|OPEN. Sire operates from Chinatown. Capone's territory. Conflict of interest.|
|5-6|Chicago court politics (2x)|OPEN. Succubus Club as nexus. Annabelle collects neonates. Lodin's return reshapes board.|
|7-8|Blood Bond steps (2x)|ACTIVE. Darius Step 1 Menele (D031 frenzy). Lodin forced bond pending. Allicia carryover.|
|9|Anarch unrest|OPEN. Gengis/Damien. Brewery. Reform vs revolution. Gengis intel channel open.|
|10-11|Ballard's frame job (2x)|ADVANCING. Drummond testified with ledger. Ballard exposed. Walt counter-op in reserve. 48-hr counterattack window.|
|12|Railroad leverage|NEW S035. Drummond's ledger maps unauthorized freight. Pipeline implications for Chuc Luc.|
|13-14|Lodin's return (2x)|ACTIVE. Appeared Jan 16 (7-night absence). Damaged, furious. Major boon owed. Blood bond demand likely. Menele's body in cedar closet.|
|15|Hunter pressure|OPEN. Dane 5/6 (active hunt, may follow to Chicago). Shepard (FBI, dormant). Society of Leopold (Chicago chapter).|
|16|The Methuselah War|HIDDEN but ACTIVE. Helena vs Menele. Darius bonded Step 1. Three Jyhad pieces (Darius, Lodin, Critias).|
|17|Sabbat infiltration|LATENT. Rigaud and Wade embedded. Activates Act III.|
|18|Damien and Neon|Anarch allies (strained). Rescued coterie. Debt owed. Belthazar staked on Wacker — when unstaked, hunt.|
|19|Tremere breach|NEW. Tomás found Walt's walkup Jan 10. Counter-op transparent to Tremere.|
|20|Lodin's siring ban|OPEN. 18 years, no new Embraces. Lodin broke his own rule.|

### Sable Threads

|Thread|Weight|Status|
|---|---|---|
|Payne family threat|3x|ESCALATED. Sharon IN CHICAGO (proxy: Halloran → Warwick → law firm). Michael absent — in Gary or Chicago? Blood bonded to Sharon. Mutual feud but mutual vengeance.|
|Annabelle's patronage|2x|ADVANCING. Private haven number. Minor boon. Positioned as asset. Wants Sable's Auspex. Teaching reflex. Ballard targeting her — coterie may need to defend ally.|
|Succubus Club politics|2x|OPEN. Natural habitat for Toreador. Helena's basement. Every thread crosses here.|
|Blood Bond steps|2x|ACTIVE. Darius Step 1 Menele. Lodin forced bond pending. Allicia carryover.|
|Allicia bond-breaking (remote)|2x|ACTIVE. Erichtho evaluation done. Carna path. Months in Milwaukee needed.|
|Ballard's frame job|2x|ADVANCING. Drummond testified with ledger. Ballard exposed. Walt in reserve. 48-hr counterattack.|
|Lodin's return|2x|ACTIVE. Appeared Jan 16. Damaged, furious, primed. Major boon owed. Blood bond demand likely.|
|Denise Price — the mother|1x|ESCALATED. In Chicago (Robert Taylor Homes). Thirty miles south.|
|Ghoul management (remote)|1x|ACTIVE. DeShawn, Pete at Kendrick's. Coop on call. Spoon home. 3 BP/month. Distance = decay risk.|
|Cover story under scrutiny|1x|OPEN. App 5 memorable. Critias aware of Auspex 3.|
|Anarch unrest|1x|OPEN. Gengis/Damien. Brewery. Damien staked Belthazar — when unstaked, hunt.|
|Hunter pressure|1x|ADVANCED. Standdown encountered + wiped. Shepard (FBI) connected. Dane may follow.|
|Drummond's gratitude + railroad|1x|NEW S035. Elder Ventrue owes Sable. Ledger maps Ballard's freight. Pipeline implications for Chuc Luc.|
|Sir Henry alliance|1x|DEEPENED S034. Coaching Sable. Fully invested. +3 disposition.|
|Tamoszius alliance|1x|NEW S034. 90yr Ballard-watcher. Info exchange deal. Independent Toreador intel channel.|
|Tomás Navarro — Tremere contact|1x|Met S033. Operational potential. Analyst, not operator.|
|Methuselah War|HIDDEN|Helena vs Menele. Coterie = unwitting Menele proxies. Portia at Succubus Club.|
|Sabbat infiltration|LATENT|Activates Act III.|

### Shared Characters

|Slot|Character|
|---|---|
|1-3|Lodin (3x)|
|4-5|Ballard (2x)|
|6-7|Annabelle Triabell (2x)|
|8|Critias|
|9|Nicolai|
|10-11|Chuc Luc (2x)|
|12|Gengis|
|13|Damien|
|14|Belthazar|
|15|Tyler|
|16|Edward Neally|
|17|Sir Henry Johnson|
|18|Maldavis|
|19|Capone|
|20|Sullivan Dane|
|21|SA William Shepard|
|22|Helena / "Portia" (HIDDEN)|
|23|Horace Turnbull|
|24|Inyanga|
|25|Roarke (DEAD: aged to dust D031. Lodin's Dominate. Hell's Pasture.)|
|26|Neon (Jimmy Holcomb)|
|27|Scottie Cartwright|
|28|Michael Standdown|
|29|Ghoul driver (Belthazar's)|
|30|Tomás Navarro|
|31|Drummond|
|32|Walt Gryzinski|
|33|Tamoszius|
|34|Lucina (Milwaukee)|
|35|Sophia Ayes|
|36|Anonymous Elder / "Bus Stop" (Khalid in persona, unknown to Tomás)|

## Live Story Oracles

### Darius

|d10|Prompt|
|---|---|
|1|I build systems. Chicago's system is bigger than I thought.|
|2|Keep your head down. Play the game. There are a hundred Kindred here who could end me.|
|3|Chuc Luc wants a Chicago pipeline. His sire Capone owns this territory. I'm caught between them.|
|4|The underground economy is different here. Bigger money, better security, more eyes.|
|5|I read people. In Chicago, the people I'm reading have been playing this game for centuries.|
|6|My cover story was built for seven Kindred in a dying city. Chicago has a hundred, and they have Auspex.|
|7|The Succubus Club is where every thread crosses. I need to be there without being noticed.|
|8|I saw what they did to Neally. I saw what the Camarilla did to make him vulnerable.|
|9|The Primogen run the city and the Methuselahs run the Primogen. The game has more layers than I knew.|
|10|I drank something I didn't choose to drink. It healed me. It tasted like the bottom of the world. I don't know whose leash I'm on now.|

### Sable

|d10|Prompt|
|---|---|
|1|My face is my business. Chicago has a thousand faces and none of them are looking at mine yet.|
|2|The Succubus Club is where I belong. The problem is everything else that belongs there too.|
|3|Sharon is here. Not offscreen. Not a name on a clock. Here.|
|4|I can make anyone want me. In this city, everyone is already wanted by someone more dangerous.|
|5|Michael painted me like I was already dead. He painted me in Chicago.|
|6|Allicia is in Gary. I'm here. The distance is the point.|
|7|Denise is thirty miles south. I could drive there in an hour.|
|8|The smile is load-bearing. If it cracks in front of these people, they'll eat me alive.|
|9|Annabelle walked into a room and the room rearranged itself around her. That's what I do. She's been doing it for three hundred years.|
|10|I fed three times because I could and tried to be human with a woman I threw out at dawn. The distance between those two things is where I live now.|
