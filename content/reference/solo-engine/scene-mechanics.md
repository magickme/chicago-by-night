---
title: "Scene Mechanics"
description: "Scene Check, Chaos Factor adjustments, Random Events, Altered/Interrupted scenes, and the Scene Adjustment Table."
weight: 20
---

## Chaos Factor

**Starting value:** 5. **Range:** 1–9. Tracks how out of control the overall situation is — not whether the PC succeeded at their immediate task.

### End-of-Scene Adjustment

Ask: *"Is the overall situation more or less chaotic than when this scene started?"*

| Outcome | CF Change |
|---------|-----------|
| PC drove the scene AND no significant external pressure accumulated | CF −1 |
| Mixed — goals achieved but at cost, new obligations, ticking clocks, reactive to NPC agendas | CF +0 |
| PC was reactive, failed at goals, or the situation deteriorated | CF +1 |

> **The most common result is CF +0.** A scene where the PC completes a mission but gains two new obligations and a clock ticks is *mixed*, not in control. Tactical success alone does not mean situational control.

CF affects Fate Chart thresholds (higher CF = more Yes answers), Random Event frequency, and Scene Check intensity.

---

## Scene Check

Before every scene (except the first scene of a new adventure): roll 1d10 vs current CF.

| Roll | Result |
|------|--------|
| Odd AND ≤ CF | **Altered** — scene happens but one element changes |
| Even AND ≤ CF | **Interrupted** — scene does not happen; something else occurs instead |
| > CF | **Normal** — scene plays as expected |

**Automatic Interrupt:** When you have no idea what happens next, skip the CF roll and declare the next scene an automatic Interrupt. Then generate the scene from the Random Event tables.

### Scene Adjustment Table (for Altered Scenes)

Roll d10 to determine what changes:

| d10 | Adjustment |
|-----|-----------|
| 1 | Remove a character |
| 2 | Add a character |
| 3 | Reduce or remove an activity |
| 4 | Increase an activity |
| 5 | Remove an object |
| 6 | Add an object |
| 7–8 | Make two adjustments (roll twice, reroll 7–8) |
| 9–10 | Reroll or choose contextually |

Alternative Altered Scene methods: (1) play the next most expected scene, (2) tweak one element via Fate Question, (3) use the table above.

---

## Random Events

**Trigger:** Doubles on d100 Fate roll where single digit ≤ CF, or any Interrupted Scene.

Generates an event *in addition to* the Fate answer.

### Event Focus Table

Roll d100 to determine what kind of random event occurs:

| d100 | Focus |
|------|-------|
| 1–7 | Remote Event — something offscreen; PC learns about it now |
| 8–28 | NPC Action — an existing NPC does something; roll Characters List |
| 29–35 | New NPC — a new character enters the situation |
| 36–45 | Move Toward Thread — progress on existing thread; roll Threads List |
| 46–52 | Move Away from Thread — setback on existing thread; roll Threads List |
| 53–55 | Close Thread — resolved or nullified; roll Threads List |
| 56–67 | PC Negative — something bad for the PC |
| 68–75 | PC Positive — something good for the PC |
| 76–83 | Ambiguous — unclear, may be foreshadowing |
| 84–92 | NPC Negative — bad for an NPC; roll Characters List |
| 93–100 | NPC Positive — good for an NPC; roll Characters List |

If the rolled Focus references an empty List, use Current Context instead.

---

## Lists (Mythic GME)

Two tracking structures with 25 slots each (5 sections of 5):

**Threads List:** Goals, missions, objectives, pending situations.
**Characters List:** Active NPCs, organizations, significant objects.

**Adding:** When an element becomes active in a scene, add it. If already listed, add another entry (creates weighted probability). Maximum 3 entries per element.

**Rolling a List:** Roll 2d10. First die = section block (1–2 = top, 3–4 = second, 5–6 = third, 7–8 = fourth, 9–10 = bottom). Second die = entry within block (1–2 = first, 3–4 = second, 5–6 = third, 7–8 = fourth, 9–10 = fifth). If slot is empty, use next occupied slot.

**Removing:** Completed threads, defeated or irrelevant NPCs. When full, consolidate — triple-weighted entries drop to double.

---

## Oracles

### Story Oracle (d10)

A custom 10-entry table maintained in `session-state.md`. Roll before any Trouble or Grace Burn to tie narrative events to current personal storylines. Entry 10 is always "(something new)." Remove resolved entries; fill empty slots from play or roll Reason Oracle.

### Reason Oracle (d10)

Generates the source behind an event or NPC motivation:

| Roll | Source |
|------|--------|
| 1 | Concept (character's core idea) |
| 2 | Nature (innate personality) |
| 3 | Demeanor (presented face) |
| 4 | Sire (blood lineage obligation) |
| 5 | Clan (faction membership) |
| 6 | Attribute (dominant trait) |
| 7 | Ability (specialized skill) |
| 8 | Background (resources, contacts, haven) |
| 9 | Merit or Flaw (exceptional factor) |
| 10 | Humanity or Path (moral framework) |
