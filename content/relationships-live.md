---
title: "Relationship Maps (Live)"
description: "Generated obligations and disposition map from canonical tables."
layout: "page"
slug: "relationships-live"
---

*Generated from `session-state.md` and `Boon Ledger.md`. This is the drift-resistant operational map; the handcrafted public map remains archival/curated.*

## Obligations

```mermaid
graph LR
    DariusCole["Darius Cole"]
    SablePrice["Sable Price"]
    Juggler["Juggler"]
    SablePrice -->|"owes One Minor"| Juggler
    Modius["Modius"]
    SablePrice -->|"owes Unclosed Gary service, not a boon"| Modius
    GordonKeaton["Gordon Keaton"]
    DariusCole -->|"owes One Minor"| GordonKeaton
    Danov["Danov"]
    DariusCole -->|"owes One future unspecified service"| Danov
    BrennonThornhill["Brennon Thornhill"]
    DariusCole -->|"owes Promised Modius debrief"| BrennonThornhill
    JeffersonFoster["Jefferson Foster"]
    DariusCole -->|"owes Conditional mediated Denver introduction"| JeffersonFoster
    ChucLuc["Chuc Luc"]
    DariusCole -->|"owes Accepted private reporting/work"| ChucLuc
    DariusCole -->|"owes Unclosed Gary service, not a boon"| Modius
    Lodin["Lodin"]
    DariusSable["Darius + Sable"]
    Lodin -->|"owes One rescue claim, Major/Life grade disputed"| DariusSable
    Critias["Critias"]
    Critias -->|"owes One Major"| DariusCole
    AnnabelleTriabell["Annabelle Triabell"]
    AnnabelleTriabell -->|"owes Four Minor"| SablePrice
    BrennonThornhill -->|"owes One Minor"| DariusCole
    EdgarDrummond["Edgar Drummond"]
    EdgarDrummond -->|"owes One Minor"| SablePrice
    HoraceTurnbull["Horace Turnbull"]
    HoraceTurnbull -->|"owes One Minor"| DariusCole
    RaymondFalcon["Raymond Falcon"]
    RaymondFalcon -->|"owes One Minor, informally witnessed"| DariusCole
    Gengis["Gengis"]
    Gengis -->|"owes One Minor, informal acknowledgment"| DariusCole
    LorraineMatthews["Lorraine Matthews"]
    LorraineMatthews -->|"owes One Minor"| DariusSable
    TremereChantryNicolai["Tremere Chantry / Nicolai"]
    BrennonThornhill -->|"One favor, former Tomás claim"| TremereChantryNicolai
    Lucian["Lucian"]
    Juggler -->|"Unspecified obligation"| Lucian
    Allicia["Allicia"]
    Allicia -->|"Full blood bond, treatment ongoing"| Modius
    VictorSalonika["Victor Salonika"]
    VictorSalonika -->|"Ghoul service"| Modius
```

## Disposition Heat

```mermaid
graph TD
    Coterie["Darius + Sable"]
```

## Chicago Standing

- Court 2/5 (Recognized): Critias consolidated +5 as of D066. Brennon +3 (Fundamental Differences, promised formal advocacy). Annabelle +1 (private line, dead drop gift). Primogen session Wed Feb 12: Ballard reprimanded 3-2-1. Inyanga abstained.
- Society 2/5 (Established): Succubus Club explored including Labyrinth. Brennon met. Falcon boon. Sir Henry +3. Toreador social infrastructure mapped.
- Underworld 0/5 (Unknown): No standing yet with Capone, Chuc Luc's Chicago operators, or the city's criminal brokers
- Street 1/5 (Emerging): Gengis +2 (Brewery access Thursdays). Maldavis +1 (shared intel, task accepted). Anarch channel open.
