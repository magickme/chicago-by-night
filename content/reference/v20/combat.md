---
title: "Combat"
description: "Complete combat rules — initiative, attack pools, damage types, maneuvers, weapons, armor, cover, and special situations."
weight: 35
---

Each combat **turn is approximately 3 seconds** and has three stages. Initiative is declared before actions; damage resolves after.

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

---

## Close Combat Maneuvers

| Maneuver | Pool | Accuracy | Diff | Damage | Notes |
|----------|------|----------|------|--------|-------|
| **Bite** | Dex + Brawl | +1 | Normal | Str +1 Agg | Requires prior clinch, hold, or tackle |
| **Block** | Dex + Brawl | Special | Normal | None | Reduces attacker's successes; bashing only (unless Fortitude/armor) |
| **Claw** | Dex + Brawl | Normal | Normal | Str +1 Agg | Requires Feral Claws or Vicissitude |
| **Clinch** | Str + Brawl | Normal | Normal | Str | Carries over; Str damage each subsequent turn; escape = resisted Str + Brawl |
| **Disarm** | Dex + Melee | Normal | +1 | Special | If successes exceed opponent's Str, weapon drops (no damage) |
| **Dodge** | Dex + Athletics | Special | Normal | None | Works vs. all attack types |
| **Hold** | Str + Brawl | Normal | Normal | None | Carries over; immobilizes; escape = resisted Str + Brawl |
| **Kick** | Dex + Brawl | Normal | +1 | Str +1 | Complex kicks may have higher difficulty |
| **Parry** | Dex + Melee | Special | Normal | None | May damage Brawl attacker if defender wins |
| **Strike** | Dex + Brawl | Normal | Normal | Str | Standard punch; bashing |
| **Sweep** | Dex + Brawl/Melee | Normal | +1 | Str | Knockdown: target rolls Dex + Athletics (diff 8) or falls |
| **Tackle** | Str + Brawl | Normal | +1 | Str +1 | Both roll Dex + Athletics (diff 7) or fall; target +1 diff next turn |
| **Weapon Strike** | Dex + Melee | Normal | Normal | Weapon | Damage type per weapon |

**Weapon length:** Being fended off with a longer weapon costs **–1 die** to attack until you close the distance.

**Unarmed damage:** Always bashing unless noted (claws, bite are aggravated).

---

## Defensive Maneuvers

Defensive actions are resisted rolls. Unless the attacker gets more total successes than the defender, the attack misses. Excess attacker successes above the defender's determine the hit.

**Block (Dex + Brawl):** Deflects bashing only. Cannot block lethal or aggravated unless the defender has Fortitude or wears armor.

**Dodge (Dex + Athletics):** Works against all attack types. In gunfights, the character moves at least 1 yard and ends up behind cover.

**Parry (Dex + Melee):** Uses a weapon to block. If the defender rolls more successes than an unarmed attacker, the attacker takes the weapon's base damage + extra successes as a damage pool.

**Full Defense:** Spend the entire turn defending. Use full dice pool for the first defense; lose **–1 die cumulatively** for each subsequent defense in the same turn.

**Multiple Opponents:** +1 difficulty per additional opponent to all attacks and defenses (maximum +4).

---

## Ranged Combat Maneuvers

| Maneuver | Pool | Accuracy | Diff | Notes |
|----------|------|----------|------|-------|
| **Standard Shot** | Dex + Firearms | Normal | Normal | One target |
| **Aimed Shot** | Dex + Firearms | +1 die/turn aiming | Normal | Max bonus dice = Perception; scope +2 first turn |
| **Three-Round Burst** | Dex + Firearms | +2 dice | +1 | Expends 3 rounds; damage = single bullet |
| **Automatic Fire** | Dex + Firearms | +10 dice | +2 | Empties clip at one target; cannot target body parts |
| **Strafing** | Dex + Firearms | +10 dice | +2 | Empties clip across 3-yard area; divide successes among targets |
| **Multiple Shots** | Dex + Firearms | Special | Normal | Divide pool by shots (up to weapon rate); different targets |
| **Two Weapons** | Dex + Firearms | Normal | +1 off-hand | Multiple action rules apply; each rolled separately |

**Range:** Short = diff **6**. Long (twice short range) = diff **8**. Point blank (within 2 meters) = diff **4**.

**Reloading:** Takes **1 full turn**. May be part of a multiple action.

---

## Cover

| Cover | Difficulty Increase to Hit | Attacker's Penalty |
|-------|---------------------------|-------------------|
| Light (prone) | +1 | None |
| Good (behind wall) | +2 | +1 |
| Superior (head only exposed) | +3 | +2 |

---

## Melee Weapons

| Weapon | Damage | Conceal |
|--------|--------|---------|
| Sap (blunt) | Str +1 B | Pocket |
| Club | Str +2 B | Trenchcoat |
| Knife | Str +1 L | Jacket |
| Sword | Str +2 L | Trenchcoat |
| Axe | Str +3 L | None |
| Stake | Str +1 L | Trenchcoat |

B = bashing. L = lethal. Blunt weapons deal bashing (lethal if targeting the head).

**Staking:** Target the heart at difficulty 9. Requires **3+ damage successes past soak**. Result: paralysis (conscious, can use Perception-based Disciplines, cannot move or spend blood). Not Final Death — remove the stake to end paralysis.

---

## Ranged Weapons

| Weapon | Damage | Range (short) | Rate | Capacity | Conceal |
|--------|--------|---------------|------|----------|---------|
| Revolver, light (.38) | 4 L | 12m | 3 | 6 | Pocket |
| Revolver, heavy (.44) | 6 L | 35m | 2 | 6 | Jacket |
| Pistol, light (9mm) | 4 L | 20m | 4 | 15+1 | Pocket |
| Pistol, heavy (.45) | 5 L | 25m | 3 | 13+1 | Jacket |
| Rifle (.30-06) | 8 L | 200m | 1 | 5+1 | None |
| SMG, small (9mm)* | 4 L | 20m | 3 | 17+1 | Jacket |
| SMG, large (MP5)* | 4 L | 50m | 3 | 30+1 | Trenchcoat |
| Assault Rifle* | 7 L | 150m | 3 | 30+1 | None |
| Shotgun (12ga) | 8 L | 20m | 1 | 5+1 | Trenchcoat |
| Crossbow | 5 L | 20m | 1 | 1 | Trenchcoat |

\* Capable of 3-round bursts, full auto, and strafing.

**Firearms vs. vampires:** Bullets deal **bashing** damage to vampires (body absorbs the wound). **Head shots = lethal** vs. vampires.

**Crossbow:** 5 turns to reload. Deals bashing vs. Kindred unless targeting head or heart; lethal vs. mortals.

---

## Armor

| Class | Armor Rating | Dexterity Penalty |
|-------|-------------|------------------|
| Reinforced clothing | 1 | 0 |
| Armor T-shirt | 2 | 1 |
| Kevlar vest | 3 | 1 |
| Flak jacket | 4 | 2 |
| Full riot gear | 5 | 3 |

- Armor adds soak vs. bashing, lethal, and aggravated **from fangs and claws only**
- Does **not** protect against fire or sunlight
- Dexterity Penalty applies to all Dexterity-based pools
- Targeting unprotected areas bypasses armor (+1 or +2 difficulty)
- A single attack dealing damage equal to **twice the armor rating** destroys it

---

## Targeting

| Target Size | Difficulty | Damage |
|------------|-----------|--------|
| Medium (limb, briefcase) | +1 | Normal |
| Small (hand, head, cellphone) | +2 | +1 die |
| Precise (eye, heart, lock) | +3 | +2 dice |

---

## Special Situations

### Ambush
Attacker rolls Dex + Stealth vs. defender's Perception + Alertness (resisted). Attacker wins: free attack, extra successes add to attack pool. Tie: attacker goes first, defender may respond. Defender wins: normal initiative.

### Blind Fighting
+2 difficulty in total darkness. Ranged attacks are inaccurate. Heightened Senses (Auspex ●) and Eyes of the Beast (Protean ●) mitigate this.

### Flank and Rear Attacks
Flank: +1 attack die. Rear: +2 attack dice.

### Dazed
If damage successes (after soak) exceed the target's Stamina (mortals) or Stamina +2 (supernaturals), the target must spend their next turn recovering.

### Knockdown
Target falls. May roll Dexterity + Athletics (difficulty varies) to immediately recover (with –2 initiative). Failed roll = spend next action standing. Botch = 1 automatic bashing damage.

### Immobilization
+2 attack dice vs. a struggling but immobilized target. Attacks hit **automatically** against a completely immobilized target (bound, staked, paralyzed).
