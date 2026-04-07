---
title: "Fate Chart"
description: "The d100 oracle. Setting odds, thresholds, result types, doubles triggers, and the Quick Yes/No alternative."
weight: 10
---

## The Chart

Roll d100. Result ≤ threshold = **Yes**. Threshold is set by the intersection of narrative odds and current Chaos Factor (CF).

| Odds | CF 1 | CF 2 | CF 3 | CF 4 | CF 5 | CF 6 | CF 7 | CF 8 | CF 9 |
|------|------|------|------|------|------|------|------|------|------|
| Certain | 85 | 90 | 90 | 90 | 90 | 95 | 95 | 95 | 95 |
| Nearly Certain | 75 | 80 | 80 | 85 | 85 | 85 | 90 | 90 | 95 |
| Very Likely | 55 | 60 | 65 | 70 | 75 | 80 | 85 | 90 | 90 |
| Likely | 35 | 45 | 50 | 55 | 65 | 70 | 75 | 80 | 85 |
| 50/50 | 20 | 25 | 35 | 45 | 50 | 55 | 65 | 70 | 75 |
| Unlikely | 10 | 15 | 20 | 25 | 35 | 45 | 50 | 55 | 65 |
| Very Unlikely | 5 | 8 | 10 | 15 | 25 | 30 | 35 | 40 | 50 |
| Nearly Impossible | 2 | 3 | 5 | 10 | 15 | 20 | 25 | 30 | 35 |
| Impossible | — | 1 | 2 | 5 | 10 | 12 | 15 | 18 | 25 |

## Result Types

| Roll vs threshold | Result |
|-------------------|--------|
| ≤ threshold ÷ 5 | **Exceptional Yes** — intensified to the next logical level |
| ≤ threshold | **Yes** — expectation confirmed |
| > threshold | **No** — next most expected outcome |
| ≥ 100 − floor((100 − threshold) ÷ 5) | **Exceptional No** — intensified opposite of Yes |

**Lore Validation on Exceptional Results:** Before narrating any Exceptional Yes or No, pause. Does the outcome contradict established source material — NPC timelines, faction politics, canon events? If yes, find a lore-consistent version that preserves the *quality* of the exceptional result. The oracle says WHAT happens; the GM validates HOW it happens against known canon. Never narrate first and retcon later.

## Doubles → Random Events

When the d100 roll shows doubles (11, 22, 33, 44, 55, 66, 77, 88, 99) **and** the single digit ≤ current CF, a Random Event fires **in addition to** the normal Fate answer.

> **Example:** CF 5. Roll 33. Single digit = 3. 3 ≤ 5 → Random Event fires. The roll still answers the Fate Question normally.

See [Scene Mechanics](../scene-mechanics/) for the Random Event Focus table.

## When to Ask

Ask a Fate Question when:

- A binary outcome genuinely matters and is uncertain
- An NPC's action, knowledge, or reaction is unclear
- Coincidence or luck is a real factor
- Consequences of an event are ambiguous

**Do not ask** about PC actions (those roll V20 dice) or narrative elements the GM controls.

## Fate Questions as RPG Rules Lookups

When a Fate Question concerns a rule resolution rather than story direction, treat CF as 5 regardless of actual CF. Treat Exceptional results as regular Yes/No unless the rule specifically uses degrees of success.

## Recording Format

```
Fate: [Question]? Odds: [odds label]. CF: [n]. Threshold: [T]. d100: [roll]. [Answer]. [+Random Event if doubles ≤ CF.]
```

## Quick Yes/No Oracle

For low-stakes checks where triggering a Random Event would be disruptive: roll 1d10 + modifier. **6+ = Yes.**

| Odds | Modifier |
|------|----------|
| Slim to none | −4 |
| Not Likely | −2 |
| Don't Know | 0 |
| Likely | +2 |
| Very Likely | +4 |

| Total | Result |
|-------|--------|
| 0 or below | No, and further bad news |
| 1–3 | No |
| 4–5 | Yes, but... |
| 6–8 | Yes |
| 9–10 | Yes, and... |
