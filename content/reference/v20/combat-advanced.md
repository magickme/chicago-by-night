---
title: "Combat — Advanced Rules"
description: "Full combat maneuvers table, weapons charts, initiative, staging, and special combat rules."
weight: 38
---

## Combat Sequence

Each combat **turn is approximately 3 seconds** and proceeds through three stages.

### Stage 1: Initiative

1. Roll **1d10 + Dexterity + Wits** (or use static initiative: **Dexterity + Wits + 6**)
2. Highest result acts first; ties broken by initiative rating, then simultaneously
3. **Wound penalties** subtract from initiative
4. **Celerity** dots *not* used for extra actions add to initiative
5. Declare actions in **reverse** initiative order (slowest first, fastest last)
6. Declare multiple actions, Discipline activation, and Willpower expenditure now
7. A character may **delay** to act later, even interrupting a slower character
8. **Defensive actions** (block, dodge, parry) may be performed at any time a character has an action remaining
9. All **Celerity extra actions** occur at the **end of the turn**, in initiative order

### Stage 2: Attack

| Attack Type | Dice Pool |
|-------------|-----------|
| Unarmed | Dexterity + Brawl |
| Melee weapon | Dexterity + Melee |
| Firearms | Dexterity + Firearms |
| Thrown weapon | Dexterity + Athletics |

- Default attack difficulty: **6**, modified by circumstances
- No successes = miss; botch = weapon jam, broken blade, hitting an ally

**Aborting:** A character may abort their declared action to a defensive action before acting, requiring a Willpower roll (difficulty 6) or spending 1 Willpower point.

### Stage 3: Resolution

- Each extra success on the attack roll adds **+1 die** to the damage pool
- Damage pool rolls vs. difficulty 6; each success = 1 health level of damage
- Damage rolls **cannot botch** (a botch = glancing blow, no damage)
- Defender soaks with Stamina (+ Fortitude)

---

## Multiple Actions

Declare total number of actions at initiative. Find the **smallest dice pool** among all intended actions. Divide that pool equally among all actions (round down). Each action uses the divided pool.

Example: A vampire wants to attack twice. Brawl pool = 6, Firearms pool = 5. Smallest = 5. Each action gets 2 dice (5 ÷ 2 = 2, round down).

---

## Close Combat Maneuvers

| Maneuver | Pool | Accuracy | Difficulty | Damage | Notes |
|----------|------|----------|-----------|--------|-------|
| **Bite** | Dex + Brawl | +1 | Normal | Str +1 Aggravated | Requires prior clinch, hold, or tackle |
| **Block** | Dex + Brawl | Special | Normal | None | Reduces attacker's successes; bashing only unless Fortitude/armor |
| **Claw** | Dex + Brawl | Normal | Normal | Str +1 Aggravated | Requires Feral Claws or Vicissitude |
| **Clinch** | Str + Brawl | Normal | Normal | Str | Carries over; Str damage each subsequent turn; escape = resisted Str + Brawl |
| **Disarm** | Dex + Melee | Normal | +1 | Special | If successes exceed opponent's Str, they are disarmed (no damage) |
| **Dodge** | Dex + Athletics | Special | Normal | None | Works vs. all attack types |
| **Hold** | Str + Brawl | Normal | Normal | None | Carries over; immobilizes; escape = resisted Str + Brawl |
| **Kick** | Dex + Brawl | Normal | +1 | Str +1 | Complex kicks may have higher difficulty |
| **Parry** | Dex + Melee | Special | Normal | None | May damage Brawl attacker if defender wins |
| **Strike** | Dex + Brawl | Normal | Normal | Str | Standard punch; bashing |
| **Sweep** | Dex + Brawl/Melee | Normal | +1 | Str | Knockdown attempt; target rolls Dex + Athletics (diff 8) or falls |
| **Tackle** | Str + Brawl | Normal | +1 | Str +1 | Knockdown; both roll Dex + Athletics (diff 7) or fall; target +1 diff next turn |
| **Weapon Strike** | Dex + Melee | Normal | Normal | Weapon | Damage type per weapon |

**Weapon Length:** A character being fended off with a longer weapon must close 1 yard before striking, losing **1 die** from their attack roll.

**Unarmed damage:** Always bashing unless noted (claws, bite).

---

## Defensive Maneuvers

Defensive actions are resisted rolls. Unless the attacker gets more total successes than the defender, the attack misses. Excess attacker successes above the defender's determine the hit.

**Block:** Dex + Brawl. Deflects bashing only. Cannot block lethal or aggravated unless the defender has Fortitude or wears armor.

**Dodge:** Dex + Athletics. Works against all attack types. In gunfights, the character moves at least 1 yard and ends behind cover (cover rules then apply to further ranged attacks).

**Parry:** Dex + Melee. Uses a weapon to block Brawl or Melee attacks. If the defender rolls more successes than a Brawl attacker, the Brawl attacker takes the weapon's base damage + extra successes as a damage pool.

**Full Defense:** Spend the entire turn defending. Use full dice pool for the first defense; lose **1 die cumulatively** for each subsequent defense in the same turn.

**Multiple Opponents:** Attacks and defenses vs. multiple opponents suffer **+1 difficulty per additional opponent** (cumulative, maximum +4).

---

## Ranged Combat Maneuvers

| Maneuver | Dice Pool | Accuracy | Difficulty | Notes |
|----------|-----------|----------|-----------|-------|
| **Standard Shot** | Dex + Firearms | Normal | Normal | One target |
| **Aimed Shot** | Dex + Firearms | +1 die/turn aiming | Normal | Max aiming dice = Perception; scope = +2 first turn |
| **Three-Round Burst** | Dex + Firearms | +2 dice | +1 | Expends 3 rounds; damage based on single bullet |
| **Automatic Fire** | Dex + Firearms | +10 dice | +2 | Empties clip at one target; half successes apply if only one target; cannot target body part |
| **Strafing** | Dex + Firearms | +10 dice | +2 | Empties clip across area (max 3 yards); divide successes among targets; dodge at +1 diff |
| **Multiple Shots** | Dex + Firearms | Special | Normal | Divide pool among shots (up to weapon rate of fire), different targets |
| **Two Weapons** | Dex + Firearms | Normal | +1 off-hand | Multiple action rules apply; each rolled separately |

**Range:** Short = difficulty **6**. Long (twice short) = difficulty **8**. Point blank (within 2 meters) = difficulty **4**.

**Reloading:** Takes **1 full turn**. May be declared as part of a multiple action.

---

## Cover

| Cover Type | Difficulty Increase to Hit | Defender's Attack Penalty |
|-----------|--------------------------|--------------------------|
| Light (prone) | +1 | None |
| Good (behind wall) | +2 | +1 |
| Superior (head only exposed) | +3 | +2 |

Penalties are cumulative when both parties are under cover.

---

## Melee Weapons

| Weapon | Damage | Conceal |
|--------|--------|---------|
| Sap (blunt) | Str +1 | Pocket |
| Club (blunt) | Str +2 | Trenchcoat |
| Knife | Str +1 | Jacket |
| Sword | Str +2 | Trenchcoat |
| Axe | Str +3 | None |
| Stake | Str +1 | Trenchcoat |

- Blunt weapons deal **bashing** (lethal if targeting the head)
- Stake to the heart requires targeting at difficulty 9 with 3+ damage successes

---

## Ranged Weapons

| Weapon | Damage | Range (short) | Rate | Capacity | Conceal |
|--------|--------|---------------|------|----------|---------|
| Revolver, light (.38) | 4 | 12m | 3 | 6 | Pocket |
| Revolver, heavy (.44 Mag) | 6 | 35m | 2 | 6 | Jacket |
| Pistol, light (9mm) | 4 | 20m | 4 | 15+1 | Pocket |
| Pistol, heavy (.45 ACP) | 5 | 25m | 3 | 13+1 | Jacket |
| Rifle (.30-06) | 8 | 200m | 1 | 5+1 | None |
| SMG, small (9mm)* | 4 | 20m | 3 | 17+1 | Jacket |
| SMG, large (MP5)* | 4 | 50m | 3 | 30+1 | Trenchcoat |
| Assault Rifle*  | 7 | 150m | 3 | 30+1 | None |
| Shotgun (12ga) | 8 | 20m | 1 | 5+1 | Trenchcoat |
| Shotgun, semi-auto* | 8 | 20m | 3 | 8+1 | Trenchcoat |
| Crossbow | 5 | 20m | 1 | 1 | Trenchcoat |

*Capable of 3-round bursts, full auto, and strafing.

- Firearms deal **lethal** vs. mortals, **bashing** vs. vampires (head shots = lethal vs. vampires)
- **Crossbow:** 5 turns to reload. Bashing vs. Kindred unless targeting head or heart; lethal vs. mortals.

---

## Maneuver Complications

### Ambush
Attacker rolls Dex + Stealth vs. Perception + Alertness (resisted). If attacker wins: one free attack, adding extra successes to the attack pool. Tie: attacker strikes first, defender may still respond. Defender wins: normal initiative.

### Blind Fighting
Attacks in total darkness or while blinded: +2 difficulty. Ranged attacks cannot be accurately made at all. Heightened Senses and Eyes of the Beast mitigate this.

### Flank and Rear Attacks
Flank: +1 attack die. Rear: +2 attack dice.

### Targeting
| Target Size | Difficulty | Damage Modifier |
|------------|-----------|-----------------|
| Medium (limb, briefcase) | +1 | None |
| Small (hand, head, cellphone) | +2 | +1 damage die |
| Precise (eye, heart, lock) | +3 | +2 damage dice |

### Dazed
If damage successes (after soak) exceed the target's Stamina (mortals) or Stamina +2 (supernaturals), the target must spend the next turn recovering.

### Knockdown
Target falls. May roll Dexterity + Athletics (difficulty varies) to recover immediately (with –2 initiative next turn). Failed roll = spend next action standing up. Botch = 1 automatic bashing health level.

### Immobilization
+2 attack dice against an immobilized but struggling target. Attacks hit **automatically** if the target is completely immobilized (tied, staked, paralyzed).

### Stake Through Heart
Target heart at difficulty **9**. If the attack inflicts at least **3 health levels of damage**, the target is paralyzed: conscious, may use perception-based Disciplines, but cannot move or spend blood points. Further damage still applies.

---

## Armor

| Class | Armor Rating | Dexterity Penalty |
|-------|-------------|------------------|
| Reinforced clothing | 1 | 0 |
| Armor T-shirt | 2 | 1 |
| Kevlar vest | 3 | 1 |
| Flak jacket | 4 | 2 |
| Full riot gear | 5 | 3 |

- Armor adds to soak vs. bashing, lethal, and aggravated from **fangs and claws**
- Does **not** protect against fire or sunlight
- Dexterity Penalty subtracts from all Dexterity-based dice pools
- Targeting unprotected areas bypasses armor (difficulty +1 or +2)
- If a single attack deals damage equal to **twice the armor's rating**, the armor is destroyed
