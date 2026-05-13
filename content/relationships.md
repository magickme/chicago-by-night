---
title: "Relationship Maps (Act I Historical)"
description: "Gary's Kindred power structure and the coterie's personal networks as of July 1990 — historical reference for Act I: Forged in Steel."
layout: "page"
slug: "relationships"
---

> **Historical — Act I, July 21, 1990.** For current Chicago relationships (Act II: Ashes and Blood, 1991+), see [Live Relationships](/relationships-live/).

*Solid lines = active relationships. Dashed lines = hidden, latent, or threatened.*

---

## Gary Kindred Power Structure

The political map of Gary, Indiana. Eight Kindred, twelve blocks, and every one of them watching the others.

```mermaid
graph TD
    subgraph COURT["Modius's Court"]
        Modius["<b>MODIUS</b><br>Toreador 7th<br><i>Prince of Gary</i>"]
        Allicia["<b>ALLICIA</b><br>Toreador 8th<br><i>Modius's childe</i>"]
        Victor["<b>Victor Salonika</b><br>Ghoul — Bar manager"]
    end

    subgraph DOCKS["The Docks"]
        Lucian["<b>LUCIAN</b><br>Gangrel 8th<br><i>~600 years — Controls waterfront</i>"]
    end

    subgraph TORCH["The Torch"]
        Juggler["<b>JUGGLER</b><br>Brujah 8th<br><i>Fixer — Runs the Rack</i>"]
        Evelyn["<b>EVELYN</b><br>Brujah?<br><i>Secret childe</i>"]
    end

    subgraph SHADOWS["The Shadows"]
        Danov["<b>DANOV</b><br>Nosferatu 7th<br><i>~600 years — Info broker</i>"]
        Dane["<b>SULLIVAN DANE</b><br>Mortal — True Faith 5<br><i>Inquisitor</i>"]
    end

    subgraph COTERIE["The Coterie"]
        Darius["<b>DARIUS COLE</b><br>Ventrue 10th (cover: 12th)<br><i>Street broker</i>"]
        Sable["<b>SABLE PRICE</b><br>Toreador 9th<br><i>Femme fatale</i>"]
    end

    subgraph CHICAGO["Chicago — Offscreen"]
        ChucLuc["<b>CHUC LUC</b><br>Ventrue 9th<br><i>Darius's sire</i>"]
        Sharon["<b>SHARON PAYNE</b><br>Toreador 7th<br><i>Presence 5 — Nemesis</i>"]
        Michael["<b>MICHAEL</b><br>Malkavian 9th<br><i>Sable's sire — MISSING</i>"]
        Annabelle["<b>ANNABELLE</b><br>Brujah<br><i>Primogen — Chicago</i>"]
    end

    %% Prince's Court relationships
    Modius -->|"sire — childe<br>freezing out"| Allicia
    Modius -->|"trusts +3 — handshake"| Darius
    Modius -->|"spy assignment<br>leash 4/6"| Sable
    Victor -->|"serves"| Modius

    %% Allicia-Sable alliance
    Sable -->|"alliance — protecting"| Allicia
    Allicia -.->|"Blood Bond Step 2"| Sable
    Sable -.->|"Blood Bond Step 1"| Allicia

    %% Docks
    Lucian -->|"feeding rights<br>cautious respect"| Darius
    Juggler -.->|"owes"| Lucian

    %% Torch
    Juggler -->|"partnership"| Darius
    Juggler -.->|"secret childe"| Evelyn

    %% Coterie
    Darius <-->|"coterie"| Sable

    %% Chicago connections
    ChucLuc -->|"sire — orders"| Darius
    Michael -.->|"sire — absent"| Sable
    Sharon -.->|"vendetta"| Sable
    Sharon -.->|"feud"| Michael

    %% Threats
    Dane -.->|"hunting 2/6"| Darius
    Danov -.->|"observes everyone"| Modius

    %% Styling
    classDef prince fill:#7c3aed,stroke:#5b21b6,color:#fff
    classDef toreador fill:#be185d,stroke:#9d174d,color:#fff
    classDef ventrue fill:#1d4ed8,stroke:#1e40af,color:#fff
    classDef brujah fill:#b91c1c,stroke:#991b1b,color:#fff
    classDef gangrel fill:#15803d,stroke:#166534,color:#fff
    classDef nosferatu fill:#78716c,stroke:#57534e,color:#fff
    classDef malkavian fill:#7e22ce,stroke:#6b21a8,color:#fff
    classDef mortal fill:#f5f5f4,stroke:#78716c,color:#1c1917
    classDef ghoul fill:#d6d3d1,stroke:#78716c,color:#1c1917
    classDef removed fill:#e7e5e4,stroke:#a8a29e,color:#a8a29e

    class Modius prince
    class Allicia,Sable,Sharon toreador
    class Darius,ChucLuc ventrue
    class Juggler,Evelyn,Annabelle brujah
    class Lucian gangrel
    class Danov nosferatu
    class Michael malkavian
    class Dane mortal
    class Victor ghoul
```

**Key:**
<span style="color:#1d4ed8">Ventrue</span> |
<span style="color:#be185d">Toreador</span> |
<span style="color:#b91c1c">Brujah</span> |
<span style="color:#15803d">Gangrel</span> |
<span style="color:#78716c">Nosferatu</span> |
<span style="color:#7e22ce">Malkavian</span>

---

## Darius Cole — Personal Network

The Architect's machine. Everyone has a function. Everyone has a price.

```mermaid
graph LR
    Darius["<b>DARIUS COLE</b><br>Ventrue 10th"]

    subgraph KINDRED["Kindred"]
        Modius["Modius +3<br><i>Prince — trusts</i>"]
        Juggler["Juggler +2<br><i>Torch partner</i>"]
        Lucian["Lucian +2<br><i>Docks — deal struck</i>"]
        Danov["Danov +1<br><i>Info broker — paper deal</i>"]
    end

    subgraph SIRE["The Sire"]
        ChucLuc["Chuc Luc -1<br><i>Cold. Transactional.</i>"]
    end

    subgraph MORTALS["Mortal Assets"]
        Ray["Ray Pulaski +2<br><i>Dock foreman</i>"]
        Marcus["Marcus Webb +2<br><i>Conditioning 3/14 — PROXY</i>"]
        Fisk["Gerald Fisk +3<br><i>Mesmerized — feeding stock</i>"]
        Eddie["Eddie Fells<br><i>DOMINATED — Berth 7</i>"]
        Marlene["Marlene Voss<br><i>Pawnshop</i>"]
        Victor["Victor +1<br><i>Bar manager — Modius's ghoul</i>"]
    end

    subgraph THREATS["Threats"]
        Dane["Sullivan Dane -3<br><i>True Faith 5 — hunting</i>"]
        Shepard["SA Shepard 0<br><i>FBI — has Warren Birch name</i>"]
        Cantone["Sal Cantone<br><i>Chicago outfit — stolen op</i>"]
    end

    %% Connections
    ChucLuc ==>|"sire — pipeline orders"| Darius
    Darius -->|"handshake"| Modius
    Darius -->|"partnership — Torch"| Juggler
    Darius -->|"feeding rights delivered"| Lucian
    Darius -.->|"next contact"| Danov
    Darius -->|"dock intel"| Ray
    Darius -->|"mortal front — HANDLE"| Marcus
    Darius -->|"feeding stock"| Fisk
    Darius -->|"Dominated"| Eddie
    Darius -->|"pawnshop"| Marlene
    Darius -->|"bar — kept ignorant"| Victor
    Dane -.->|"hunting 2/6"| Darius
    Shepard -.->|"investigating"| Darius
    Cantone -.->|"will retaliate"| Darius

    %% Styling
    classDef pc fill:#1d4ed8,stroke:#1e40af,color:#fff,font-weight:bold
    classDef kindred fill:#312e81,stroke:#1e1b4b,color:#fff
    classDef sire fill:#581c87,stroke:#3b0764,color:#fff
    classDef asset fill:#065f46,stroke:#064e3b,color:#fff
    classDef threat fill:#991b1b,stroke:#7f1d1d,color:#fff
    classDef dominated fill:#064e3b,stroke:#022c22,color:#fff

    class Darius pc
    class Modius,Juggler,Lucian,Danov kindred
    class ChucLuc sire
    class Ray,Marcus,Fisk,Marlene,Victor asset
    class Eddie dominated
    class Dane,Shepard,Cantone threat
```

**Clock Pressure:** Cover Story 3/6 | Torch Heat 5/6 | Dock Exposure 3/6 | Dane 2/6

---

## Sable Price — Personal Network

The Survivor's web. Everyone sees something different. None of them see her.

```mermaid
graph LR
    Sable["<b>SABLE PRICE</b><br>Toreador 9th"]

    subgraph ALLIANCE["The Alliance"]
        Allicia["Allicia +4<br><i>Blood Bond Step 2 ↔ Step 1<br>Counting words (9)</i>"]
    end

    subgraph COURT["Court"]
        Modius["Modius +3<br><i>Leash 4/6 — spy assignment</i>"]
        Victor["Victor +1<br><i>Modius's ghoul — monitors</i>"]
    end

    subgraph SIRES["Sires and Enemies"]
        Michael["Michael +1<br><i>Malkavian sire — MISSING</i>"]
        Sharon["Sharon -4<br><i>Presence 5 — vendetta 1/6</i>"]
    end

    subgraph GHOULS["Kendrick's Auto — Secret Haven"]
        DeShawn["DeShawn<br><i>Soldier — Bond Step 2</i>"]
        LittlePete["Little Pete<br><i>19 — Bond Step 2</i>"]
        Coop["Coop<br><i>Driver — Bond Step 1</i>"]
    end

    subgraph MORTALWORLD["Mortal World"]
        Denise["Denise Price 0<br><i>Mother — found the number</i>"]
        Keisha["Keisha<br><i>PLACED — Englewood</i>"]
        Amy["Amy<br><i>PLACED — Englewood</i>"]
    end

    subgraph COTERIE_S["Coterie"]
        Darius["Darius Cole<br><i>Ventrue — the systems guy</i>"]
    end

    %% Connections
    Sable -->|"protecting — feeding"| Allicia
    Allicia -.->|"Blood Bond Step 2"| Sable
    Sable -.->|"Blood Bond Step 1"| Allicia
    Sable -->|"domitor"| DeShawn
    Sable -->|"domitor — primary target"| LittlePete
    Sable -->|"domitor"| Coop
    Modius -->|"spy assignment<br>leash 4/6"| Sable
    Sable -->|"false reports"| Modius
    Victor -.->|"monitors"| Sable
    Michael -.->|"absent sire"| Sable
    Sharon -.->|"vendetta — letter to Denise?"| Sable
    Denise -.->|"called the studio"| Sable
    Sable -.->|"placed"| Keisha
    Sable -.->|"placed"| Amy
    Sable <-->|"coterie"| Darius

    %% Styling
    classDef pc fill:#be185d,stroke:#9d174d,color:#fff,font-weight:bold
    classDef ally fill:#7c3aed,stroke:#6d28d9,color:#fff
    classDef court fill:#312e81,stroke:#1e1b4b,color:#fff
    classDef threat fill:#991b1b,stroke:#7f1d1d,color:#fff
    classDef mortal fill:#f5f5f4,stroke:#78716c,color:#1c1917
    classDef coterie fill:#1d4ed8,stroke:#1e40af,color:#fff

    class Sable pc
    class Allicia ally
    class Modius,Victor court
    class Sharon,Michael threat
    classDef ghouled fill:#064e3b,stroke:#022c22,color:#fff
    class DeShawn,LittlePete,Coop ghouled
    class Denise,Keisha,Amy mortal
    class Darius coterie
```

**Clock Pressure:** Modius Leash 4/6 | Sharon Vendetta 1/6 | West Side Heat 1/6 | Humanity 5

---

*These maps reflect the state of play as of July 21, 1990 — midway through Act I. By Baptism by Fire (NYE 1990), every line on these charts will have been tested, broken, or redrawn.*
