---
title: "Scene Boot Checklist"
description: "Pre-flight sequence for every scene. Eleven checks that must pass before play begins."
weight: 10
---

Run this checklist at the start of every scene, in order. If any check fails, resolve it before play begins.

| # | Check | How |
|---|-------|-----|
| 1 | **Canon + runtime current?** | Run `python3 scripts/sync_state_json.py --check --check-generated`, or rerun `sync_chicago_chronicles.py` after any `session-state.md` edit |
| 2 | **Blood deducted for elapsed days?** | 1 BP per in-game day since last scene. Note in session-state blood field. |
| 3 | **Weather looked up?** | Grep `Weather and Astronomy 1990.md` for in-game date (covers 1990–1991). |
| 4 | **Mortal noise generated?** | Gary: `python3.11 scripts/gary_daily.py --date YYYY-MM-DD` / Chicago: `chicago_daily.py` |
| 5 | **All 9 keyed triggers checked?** | Feeding Timer, Dane, Modius, Masquerade, Pipeline, Dawn, Sharon, Entrancement, Sable Feeding. See GAME-REFERENCE KEYED SCENES. |
| 6 | **Hot clocks noted?** | Any clock at 4/6 or above = active scene pressure. List in scene frontmatter. |
| 7 | **Style lens chosen?** | Roll 2d10 or choose from 25 Lenses (WOD-VOICE-REFERENCE). Record in frontmatter. |
| 8 | **Theme / Mood set?** | Pull from location note or improvise. Theme = meaning. Mood = lens. Scale = narrative focus. |
| 9 | **Active NPCs identified?** | Who is in this scene? Check voice cards or run `vtm_rag.py --type npc`. |
| 10 | **Beast voice active?** | If BP ≤ half max: write one italicized blockquote per substantial response. |
| 11 | **Hunting heat checked?** | If feeding scene: check territory heat in Gary/Chicago Territory Atlas. |

## Runtime Loading Order

When starting from scratch or after a gap:

1. Read `vampire/PLAY-REFERENCE.md` and `Scene Boot Packet.md`
2. Read `Session-Retro.md` lines 1–46 (Active Patterns + Graduated list only — skip session log)
3. Read `Faction Engine.md`
4. If more situational context needed: `Tonight Brief.md` → `Chicago Chronicles Runtime Brief.md`
5. Read `session-state.md` only on contradiction, staleness, or Full Cold Start
6. For scene-specific rules, lore, voice: `vtm_rag.py query "topic" --type <class>`

## End-of-Scene Bookkeeping

Update `session-state.md` with all changes from play:

- Blood pool (both PCs)
- Willpower (both PCs)
- Humanity (if check triggered)
- Scale (reset if Burn fired)
- Chaos Factor (apply end-of-scene adjustment)
- Hot clocks (increment any that triggered)
- NPC dispositions (any shifts from scene)
- Thread progress (new threads, resolved threads)
- Story Oracle (remove resolved entries, fill empties)
- Boon Ledger (any new prestation)
- Relationship Map notes (new connections, changed relationships)

Then run `python3.11 scripts/sync_chicago_chronicles.py` to regenerate all derived surfaces.
