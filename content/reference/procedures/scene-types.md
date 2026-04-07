---
title: "Scene Type Loading Guide"
description: "What to load for each scene type beyond the boot packet. RAG-first retrieval protocol."
weight: 20
---

## Loading by Scene Type

Beyond the standard boot packet, load these additional resources based on what the scene involves.

| Scene Type | Load These |
|------------|-----------|
| **Feeding** | Boot packet pools + feeding quick-ref. Victim table (V5-BACKPORT). Territory Atlas hunting heat. |
| **Court / Politics** | NPC files for attendees. Boon Ledger. WOD-VOICE-REFERENCE dialogue registers + clan voices. Dialogue Quick-Ref or full WRITING-TECHNIQUE-REFERENCE for deep retrieval. |
| **Investigation / Surveillance** | Faction Engine. Payphone Registry (if calls involved). GAME-REFERENCE investigation/discovery rules. |
| **Combat** | GAME-REFERENCE-EXTENDED combat tables. NPC stats for opponents. |
| **Dane / Hunter** | Hunter-Vigil-Backport. Dane NPC file. True Faith rules (GAME-REFERENCE). GAME-REFERENCE-EXTENDED hunter pipeline. |
| **BbF Party** | Baptism by Fire — GM Prep (`Overview/Acts/`). All NPC voice cards in that doc. Published beat map. |
| **Coterie Planning** | Both PC stats (PLAY-REFERENCE pools section). Session-state threads. BbF Planning Checklist. |
| **Timeskip** | Session-state full. Threat Clocks.md full. Faction Engine. |

## RAG-First Retrieval Protocol

For any item in the table above: **run RAG before opening full reference files.**

```bash
python3.11 scripts/vtm_rag.py query "topic" --type <class>
```

RAG returns targeted chunks (typically 3–8 paragraphs) without loading 900-line documents into context. Use it for:

- NPC details: `--type npc`
- Rules lookups: `--type rules`
- Voice patterns: `--type voice-technique` or `--type npc-voice`
- Scene history: `--type scene`
- Location data: `--type location`
- Published WoD lore: `--type source-material`
- Runtime state: `--type mutable-canon`

Full files only when RAG returns insufficient context for the specific need.

## Joint Scene Protocol

When both PCs are in the same scene:

- **POV:** Whoever declared the scene's agenda holds narrative POV. Switch on significant Fate Question result or when the other PC takes a decisive action.
- **Scale:** One shared Scale track. Active POV's rolls determine delta. Supporting PC's rolls contribute delta only if directly aiding the POV action.
- **Three-PC scenes:** Two active + one observer until the observer acts. Don't track three simultaneous threads.
- **Dialogue:** Both PCs speak in their own voice (V/T matrix). Tag switches clearly.
- **File:** One scene file in POV PC's folder. Other PC(s) get a stub with cross-reference, BP/WP changes, and key beats.

## Session-State and File Relationships

```
session-state.md              ← authoritative mutable canon
    ↓ sync_chicago_chronicles.py
Scene Boot Packet.md          ← derived, regenerated each session
Tonight Brief.md              ← derived, regenerated each session
PC dashboards                 ← derived, regenerated each session
Faction Engine.md             ← partially derived, partially manual
```

Never edit derived files directly. Edit session-state.md then regenerate.
