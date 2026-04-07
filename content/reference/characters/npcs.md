---
title: "NPCs"
description: "NPC Quick Score table, active voice cards for Chicago and Gary, and solo opposed roll procedure."
weight: 30
---

## Quick Score Table

In solo play, NPCs oppose PC rolls using a flat **Quick Score** as the difficulty. Select based on the NPC's approximate power level.

| Score | Tier | Examples |
|-------|------|---------|
| 4 | Weak mortal | Random bar patron, low-level errand runner |
| 6 | Competent mortal | Dock worker, beat cop, mid-level criminal |
| 8 | Exceptional mortal / weak vampire | Dane (mortal + True Faith 5), detective, corporate fixer |
| 10 | Neonate vampire / skilled professional | Danov, Juggler, Michael Unther |
| 12 | Ancilla / powerful NPC | Modius, Allicia, Erichtho |
| 14 | Elder | Lucian, Annabelle, Sharon |

**Social rule:** Roll the PC's social pool vs the NPC's Quick Score as difficulty. Failure = NPC gets what they want. NPC disposition (see session-state.md) sets the *odds* for Fate Chart questions about cooperation, not the mechanical difficulty of the roll.

---

## Chicago NPCs (Act II Active)

| NPC | Disp | Voice | Sample |
|-----|------|-------|--------|
| Lodin | 0 | Imperious. Every sentence is a command or judgment. Presence behind each word. | "You will present yourselves. This is not a request." |
| Ballard | 0 | Greasy charm over cold calculation. Hospitality weaponized. | "Please, sit. Eat something. I insist." |
| Annabelle | 0 | Compliments containing rankings. Eyes measuring while the body laughs. | "You look wonderful tonight. Gary agrees with you." |
| Critias | 0 | Measured, erudite. Every sentence considered for centuries. | "The question is not whether you will be used. The question is by whom." |
| Sir Henry | +1 | Warm, genuine, but watching. Toreador grace without the blade showing. | "Lucian sent you? Good. The Club can be... overwhelming at first." |
| Gengis | 0 | Direct. Political but honest about it. Street philosophy. | "The Camarilla works fine. For the people at the top." |
| Damien | 0 | Angry. Righteous. Wants action, not speeches. | "Talk. That's all anyone does in this city." |
| Brennon | 0 | Nightclub owner. Smooth, transactional, protective of domain. | "Welcome to the Succubus Club. Try not to embarrass anyone." |
| Capone | 0 | Old-world mob boss. Formal. Dangerous under the manners. (Voice TBD — not yet met.) | — |
| Neally | 0 | Polished surface, rotting core. Increasingly desperate. | "The Prince is... indisposed. I can help you." |

---

## Gary NPCs (Act I, Offscreen)

| NPC | Disp | Voice | Sample |
|-----|------|-------|--------|
| Modius | +3 | Implications, never orders. Paranoid. Gracious theater. | "I trust your accommodations are... adequate." |
| Allicia | +5 | SILENT. Piano, gaze, distance, touch. Presence speaks. | *(Nocturne stops. She looks at you. Resumes.)* |
| Lucian | +2 | Short declaratives. Ancient patience. Capability assessment. | "Sit." |
| Danov | +2 | Soft, rare, already knows the answer. Judge, not predator. | "Do you believe a man can build something and not become it?" |
| Juggler | +2 | Loud, dramatic, Italian anger. Arms wide. Performative. | "You're a bastard, Birch. I mean that with respect." |
| Dane | −3 | Outside. Notebook. Stillness. Pity, not hatred. True Faith 5. | *(Does not speak. His presence is felt.)* |

---

## Using Voice Cards

Before writing any NPC dialogue: identify (1) sentence length, (2) pronoun-dropping or full subject, (3) active vs. discursive rhythm, (4) characteristic deflection move.

Every NPC line should be attributable to that specific NPC without a dialogue tag. If a line could belong to any character, it belongs to none.

For extended NPC interactions or unfamiliar NPCs, run: `python3.11 scripts/vtm_rag.py query "NPC name" --type npc`
