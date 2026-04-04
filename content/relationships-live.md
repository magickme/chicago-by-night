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
    Allicia["Allicia"]
    Coterie -->|"5"| Allicia
    SharonPayne["Sharon Payne"]
    Coterie -->|"-4"| SharonPayne
    SirHenryJohnson["Sir Henry Johnson"]
    Coterie -->|"3"| SirHenryJohnson
    Modius["Modius"]
    Coterie -->|"3"| Modius
    SullivanDane["Sullivan Dane"]
    Coterie -->|"-3"| SullivanDane
    Lodin["Lodin"]
    Coterie -->|"2"| Lodin
    AnnabelleTriabell["Annabelle Triabell"]
    Coterie -->|"2"| AnnabelleTriabell
    Gengis["Gengis"]
    Coterie -->|"2"| Gengis
    Lucian["Lucian"]
    Coterie -->|"2"| Lucian
    Danov["Danov"]
    Coterie -->|"2"| Danov
```

## Chicago Standing

- Court 1/5 (Known): Arriving as Modius's emissaries with letters. Status comes from purpose, not trust
- Society 1/5 (Known): Sir Henry referral gives them one soft entry point into Toreador / Succubus space
- Underworld 0/5 (Unknown): No standing yet with Capone, Chuc Luc's Chicago operators, or the city's criminal brokers
- Street 0/5 (Unknown): No established footing yet with Anarchs, Brewery traffic, or district-level crews
