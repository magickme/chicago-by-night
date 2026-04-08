---
title: "Combat"
description: "Complete V20 combat rules — initiative, attack, damage, multiple actions, and combat maneuvers."
weight: 35
---

Each combat **turn is approximately 3 seconds** and has three stages. Initiative is declared before actions; damage resolves after.

## Pages

| Page | Contents |
|------|----------|
| [Maneuvers](maneuvers/) | Close combat, defensive, and ranged maneuvers — full tables with pools, accuracy, difficulty, and damage |
| [Weapons & Armor](weapons-armor/) | Melee weapons, ranged weapons, cover, armor classes, and targeting rules |
| [Special Situations](special-situations/) | Ambush, blind fighting, flanking, dazed, knockdown, and immobilization |

---

## Stage 1: Initiative

1. Roll **1d10 + Dexterity + Wits** (or use static: **Dex + Wits + 6**)
2. Highest result acts first; ties broken by Wits, then simultaneously
3. **Wound penalties** subtract from initiative
4. **Celerity** dots *not* used for extra actions add to initiative
5. Declare actions in **reverse** order (slowest first, fastest last)
6. Declare multiple actions, Discipline activations, and Willpower spends at this stage
7. A character may **delay** their action to interrupt a slower character
8. **Defensive actions** (block, dodge, parry) may be taken any time while the character has an action remaining
9. All **Celerity extra actions** happen at the **end of the turn**, in initiative order

---

## Stage 2: Attack

| Attack Type | Dice Pool |
|-------------|-----------|
| Unarmed | Dexterity + Brawl |
| Melee weapon | Dexterity + Melee |
| Firearms | Dexterity + Firearms |
| Thrown weapon | Dexterity + Athletics |

Default difficulty: **6**, modified by circumstances. No successes = miss. Botch = fumble (jam, broken weapon, hit an ally).

**Aborting:** Before acting, a character may abort their declared action to a defensive action with a Willpower roll (diff 6) or by spending 1 Willpower.

---

## Stage 3: Damage & Soak

Each extra success on the attack roll adds **+1 die** to the damage pool.

**Damage:** Roll damage pool vs. difficulty 6. Each success = 1 health level. Damage rolls cannot botch.

**Soak:** Defender rolls Stamina (+ Fortitude) vs. difficulty 6. Each success absorbs 1 health level.

| Damage Type | Can Soak With |
|-------------|---------------|
| Bashing | Stamina (+ Fortitude). After soak, bashing is **halved** (round down) for vampires. |
| Lethal | Stamina (+ Fortitude). |
| Aggravated | **Fortitude only.** Vampires without Fortitude cannot soak aggravated. |

---

## Multiple Actions

Declare total number of actions at initiative. Find the **smallest dice pool** among all intended actions. Divide that pool by the number of actions (round down). Each action uses the divided pool.

*Example: Brawl pool 6, Firearms pool 5. Want 2 actions. Smallest = 5. Each action gets 2 dice.*
