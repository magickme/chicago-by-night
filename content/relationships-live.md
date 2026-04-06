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
    SablePrice -->|"owes Minor (2)"| Juggler
    Modius["Modius"]
    SablePrice -->|"owes Fealty (ongoing)"| Modius
    DariusCole -->|"owes Minor (2)"| Juggler
    DariusCole -->|"owes Fealty (ongoing)"| Modius
    ChucLuc["Chuc Luc"]
    DariusCole -->|"owes Filial obligation"| ChucLuc
    Danov["Danov"]
    Danov -->|"owes —"| DariusCole
    Allicia["Allicia"]
    Allicia -->|"owes Moderate (3)?"| SablePrice
    HoraceTurnbull["Horace Turnbull"]
    HoraceTurnbull -->|"owes Minor (2)"| DariusCole
    Lucian["Lucian"]
    Juggler -->|"Unknown"| Lucian
    Allicia -->|"Blood Bond (3 steps)"| Modius
    VictorSalonika["Victor Salonika"]
    VictorSalonika -->|"Ghoul bond"| Modius
```

## Disposition Heat

```mermaid
graph TD
    Coterie["Darius + Sable"]
```

## Chicago Standing

- Court 2/5 (Recognized): Critias +2 (faculty club invitation). Brennon +1 (office line). Annabelle +3 (property warning). Wednesday session = next formal step.
- Society 2/5 (Established): Succubus Club explored including Labyrinth. Brennon met. Falcon boon. Sir Henry +3. Toreador social infrastructure mapped.
- Underworld 0/5 (Unknown): No standing yet with Capone, Chuc Luc's Chicago operators, or the city's criminal brokers
- Street 1/5 (Emerging): Gengis +1 (Brewery confirmed Thursdays). Maldavis +1 (shared intel, task accepted). Anarch channel open.
