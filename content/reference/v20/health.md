---
title: "Health, Damage & Healing"
description: "Health levels, damage types, vampire healing, torpor, fire, sunlight, and environmental hazards."
weight: 35
---

## Health Levels

Every character has seven health levels. Each represents a threshold of physical damage:

| Health Level | Dice Pool Penalty | Movement |
|---|---|---|
| Bruised | 0 | No hindrance |
| Hurt | –1 | No movement hindrance |
| Injured | –1 | Half maximum running speed |
| Wounded | –2 | Cannot run (may walk); moving + attacking always costs dice |
| Mauled | –2 | May only hobble (3 yards/meters per turn) |
| Crippled | –5 | May only crawl (1 yard/meter per turn) |
| Incapacitated | — | Cannot move; likely unconscious |

Below Incapacitated: vampires enter **torpor** (from bashing/lethal) or suffer **Final Death** (from aggravated).

---

## Damage Types

### Bashing
Blunt force: punches, kicks, clubs, explosions. All unarmed combat deals bashing unless using Feral Claws or supernatural powers.

**Firearms vs. vampires:** Bullets deal **bashing** to vampires (the body absorbs and closes around the wound). Head shots deal lethal.

- **Vampire soak:** Stamina (+ Fortitude). After soak, bashing damage to vampires is **halved** (round down).
- **At Incapacitated + 1 more bashing:** vampire enters torpor.

### Lethal
Edged and piercing weapons, bullets against mortals, head shots against vampires.

- **Vampire soak:** Stamina (+ Fortitude). Lethal is treated as standard damage for vampires and heals normally with blood.
- **At Incapacitated + 1 more lethal:** vampire enters torpor.

### Aggravated
Fire, sunlight, claws/fangs of supernatural beings (vampires, werewolves, some others).

- **Vampire soak:** Fortitude **only**. Vampires without Fortitude cannot soak aggravated damage.
- **Healing:** One full day of rest + 5 blood points per aggravated level healed. Healing additional aggravated levels on the same day costs 5 blood points + 1 Willpower point each.
- **At Incapacitated + aggravated:** **Final Death**.

---

## Applying Damage

Damage fills health boxes from top (Bruised) to bottom (Incapacitated). All damage types coexist, but they are tracked separately:

- Mark bashing: **/**
- Mark lethal: **X**
- Mark aggravated: **✦** (or asterisk **\***)

Aggravated is always marked in the highest available box. If an aggravated wound is added when lower-severity damage already occupies that box, all lower-severity boxes shift down one level.

**Overflow:** Lethal or bashing damage taken while Incapacitated converts to the next severity level. Bashing → lethal at Incapacitated; lethal at Incapacitated with more damage → torpor.

---

## Vampire Healing

### Bashing and Lethal
- Spend **1 blood point** to heal **1 health level** of bashing or lethal damage.
- Requires rest (not usable in the same turn as physical combat actions, unless the vampire has high enough Generation to spend multiple blood points per turn).
- Multiple health levels can be healed simultaneously if Generation allows multiple blood expenditures per turn.

### Aggravated
- Requires **one full day of rest** and **5 blood points** per level.
- Additional aggravated levels healed on the same day: 5 blood points + **1 Willpower point** each.
- Cannot be healed in combat.

### Healing Summary

| Damage Type | Cost | Time |
|------------|------|------|
| Bashing | 1 blood point | Instantaneous (while resting) |
| Lethal | 1 blood point | Instantaneous (while resting) |
| Aggravated | 5 blood points | 1 full day per level |

---

## Mortal Healing

Mortals heal much slower and cannot regenerate through blood expenditure.

| Damage Type | Health Level | Recovery Time |
|------------|-------------|---------------|
| Bashing | Bruised–Wounded | 1 hour |
| Bashing | Mauled | 3 hours |
| Bashing | Crippled | 6 hours |
| Bashing | Incapacitated | 12 hours |
| Lethal | Bruised | 1 day |
| Lethal | Hurt | 3 days |
| Lethal | Injured | 1 week |
| Lethal | Wounded | 1 month |
| Lethal | Mauled | 2 months |
| Lethal | Crippled | 3 months |
| Lethal | Incapacitated | 5 months |

Untreated lethal wounds worsen by **1 lethal level per day**. Past Mauled, recovery requires medical treatment. Past Crippled, no recovery is possible without professional medical care.

---

## Torpor

Torpor is a deathlike trance — complete shutdown of the vampiric condition.

### Entering Torpor

**From wounds:** Taking damage past Incapacitated (bashing or lethal) sends the vampire into torpor.

**From blood loss:** When a vampire's blood pool drops to 0 through nightly expenditure, they deteriorate:
- 1 health level per day from desiccation
- By the seventh day (at Incapacitated), they enter torpor
- A staked or paralyzed vampire continues burning 1 blood point per night

**Voluntary torpor:** A vampire may choose to enter torpor deliberately.

### Duration

| Humanity/Path | Length of Torpor |
|--------------|-----------------|
| 10 | 1 day |
| 9 | 3 days |
| 8 | 1 week |
| 7 | 2 weeks |
| 6 | 1 month |
| 5 | 1 year |
| 4 | 1 decade |
| 3 | 5 decades |
| 2 | 1 century |
| 1 | 5 centuries |
| 0 | Millennium or more |

### Awakening from Torpor

After the mandatory rest period:
1. Spend **1 blood point** and roll an **Awakening roll** (Humanity or Path, difficulty 8)
2. If blood pool is empty, cannot rise until fed
3. Failed roll: try again the next night
4. Success: rise at **Crippled** (lowest functional health level)

**Voluntary torpor:** May rise after **half** the mandatory period; still requires an Awakening roll.

**Torpor state:** A torpid vampire ignores the nightly blood expenditure. They are in genuine hibernation.

### Torpor and Memory

A vampire in torpor has no sensory awareness. They may have dreams — particularly if blood-bonded, if they have Auspex, or if specific Disciplines or rituals are used on them.

---

## Final Death

**Triggers:**
- Taking 1 more level of aggravated damage while Incapacitated or in torpor
- Decapitation, explosion, total bodily destruction
- Complete incineration

When a vampire suffers Final Death, the body crumbles: an old vampire turns to ash, a young vampire might simply fall dead. The speed of dissolution correlates roughly with age and blood potency.

---

## Fire

Fire damage is **aggravated** and **automatic** (no attack roll required — contact is sufficient). Only **Fortitude** can soak fire damage.

### Fire Soak Difficulty

| Soak Difficulty | Heat Source |
|-----------------|-------------|
| 3 | Candle |
| 5 | Torch |
| 7 | Bunsen burner / industrial heat |
| 8 | Electrical fire |
| 9 | Chemical fire |
| 10 | Molten metal |

### Fire Damage per Turn

| Health Levels/Turn | Exposure |
|--------------------|----------|
| 1 | Torch; small part of body exposed |
| 2 | Bonfire; half of body exposed |
| 3 | Raging inferno; entire body engulfed |

**Appearance damage:** At Mauled from fire, reduce Appearance by 1 (until healed to Bruised). At Crippled or Incapacitated, reduce Appearance by 2.

**Rotschreck:** Fire always triggers Rotschreck. See [Frenzy & Rotschreck](/reference/v20/frenzy/).

---

## Sunlight

Sunlight is **more dangerous than fire** — it is the most primal of the vampiric vulnerabilities. Damage is **aggravated** and **automatic**. Only **Fortitude** can soak it.

### Sunlight Soak Difficulty

| Soak Difficulty | Intensity |
|-----------------|-----------|
| 3 | Faint light through closed curtain; very heavy cloud cover; twilight |
| 5 | Fully protected by heavy clothes, gloves, sunglasses, wide-brimmed hat |
| 7 | Indirect light through window or light curtains |
| 9 | Outside on overcast day; single ray of direct sun |
| 10 | Direct unobscured sunlight |

### Sunlight Damage per Turn

| Health Levels/Turn | Exposure |
|--------------------|----------|
| 1 | Small part of body (a hand or part of the face) |
| 2 | Large part of body (leg, arm, whole head) |
| 3 | 50% or more of the body |

**Blindness:** Looking directly into sunlight **blinds immediately** (retinas burned).

**Moonlight:** Not dangerous. A full moon may cause mild discomfort or difficulty without protective clothing, at Storyteller discretion.

**Rotschreck:** Sunlight exposure triggers Rotschreck.

---

## Other Environmental Hazards

### Staking
A vampire staked through the heart is **paralyzed** (not destroyed). The vampire remains conscious and can use perception-based powers (Auspex) but cannot move, take physical actions, or spend blood points. A staked vampire still burns 1 blood point per night.

**Mechanics:** Targeting the heart is difficulty **9**. Success requires at least **3 health levels of damage** to reach and penetrate the heart. Fortitude applies normally to the damage roll, but staking still paralyzes if the damage threshold is reached.

**Removing the stake:** Requires the vampire to be held still and someone to physically pull it out (Strength roll, difficulty 6). The paralysis ends immediately.

### Electrocution

| Health Levels/Turn | Source |
|--------------------|--------|
| 1 | Wall socket |
| 2 | Protective fence |
| 3 | Vehicle battery, junction box |
| 4 | Main feed line, subway rail |

- Lethal damage each turn until contact is broken (Strength roll, difficulty 5 for vampires, 9 for mortals)
- A **botched soak roll** converts the damage to aggravated
- Armor does not protect against electricity

### Falling
- **1 die of bashing damage per 10 feet / 3 meters** fallen
- Soak normally
- Landing on sharp objects may convert to lethal
- At 100 feet / 30 meters (terminal velocity): maximum **10 dice, lethal damage**, armor at half rating

### Drowning
Vampires do not breathe — they do not drown in the conventional sense. However:
- Complete immobilization in water prevents any action
- Running water affects some vampires supernaturally (Storyteller discretion; not in V20 core)
- Trapped underwater requires escaping the water; the vampire is not harmed by lack of air

### Temperature Extremes
- Cold: Severe cold may impose –1 or more to Dexterity-based pools; frostbite is possible with extended exposure
- Heat: Temperatures above 200°F / 100°C may produce fire-equivalent effects
- Vampires otherwise suffer little from temperature variation
