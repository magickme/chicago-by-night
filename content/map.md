---
title: "Gary — 1990 Territory Map (Act I, Historical)"
description: "Interactive map of Gary, Indiana, July 1990. Act I historical reference. The chronicle's current setting is Chicago, 1991+."
layout: "page"
slug: "map"
---

> **Historical — Act I: Forged in Steel.** The coterie left Gary for Chicago in January 1991. This map documents the seven Kindred and the killing ground as they stood at the close of Act I. For current Chicago operations, see [Locations](/locations/) and the [Dashboard](/dashboard/).

<link rel="stylesheet" href="https://unpkg.com/leaflet@1.9.4/dist/leaflet.css" />
<script src="https://unpkg.com/leaflet@1.9.4/dist/leaflet.js"></script>

<style>
#gary-map { width: 100%; height: 700px; border-radius: 8px; border: 2px solid #292524; margin: 1.5rem 0; }
.leaflet-popup-content-wrapper { background: #1c1917 !important; color: #e7e5e4 !important; border-radius: 6px !important; }
.leaflet-popup-tip { background: #1c1917 !important; }
.leaflet-popup-content { font-size: 14px !important; line-height: 1.5 !important; }
.leaflet-popup-content strong { color: #fbbf24; }
.leaflet-popup-content .pop-controller { color: #a78bfa; font-size: 12px; }
.leaflet-popup-content .pop-heat { color: #f87171; font-size: 12px; }
.leaflet-popup-content .pop-desc { margin-top: 6px; color: #d6d3d1; }
.map-legend { background: #1c1917; color: #e7e5e4; padding: 1rem 1.25rem; border-radius: 8px; margin-top: 1rem; font-size: 14px; line-height: 1.8; }
.map-legend span { display: inline-block; width: 14px; height: 14px; border-radius: 3px; margin-right: 6px; vertical-align: middle; }
@media (max-width: 768px) { #gary-map { height: 450px; } }
</style>

*Gary, Indiana. July 1990. Click any marker for details. Colored zones show Kindred territorial claims.*

<div id="gary-map"></div>

<div class="map-legend">
<strong>Territories</strong><br>
<span style="background:rgba(220,38,38,0.25);border:1px solid #dc2626"></span> Modius's Court<br>
<span style="background:rgba(234,179,8,0.25);border:1px solid #eab308"></span> The Rack / The Torch<br>
<span style="background:rgba(37,99,235,0.25);border:1px solid #2563eb"></span> Darius's West Side<br>
<span style="background:rgba(22,163,74,0.25);border:1px solid #16a34a"></span> Lucian's Docks<br>
<span style="background:rgba(249,115,22,0.25);border:1px solid #f97316"></span> Juggler's Wasteland<br>
<span style="background:rgba(168,85,247,0.25);border:1px solid #a855f7"></span> Telton Cemetery (Michael)<br>
<span style="background:rgba(120,113,108,0.25);border:1px solid #78716c"></span> Williams's Church (CLOSED)<br>
</div>

<script>
var map = L.map('gary-map', {
    center: [41.600, -87.345],
    zoom: 13,
    zoomControl: true,
    attributionControl: true
});

L.tileLayer('https://{s}.basemaps.cartocdn.com/dark_all/{z}/{x}/{y}{r}.png', {
    attribution: '&copy; <a href="https://www.openstreetmap.org/copyright">OSM</a> &copy; <a href="https://carto.com/attributions">CARTO</a>',
    maxZoom: 18,
}).addTo(map);

// -- TERRITORY OVERLAYS --

// Modius's Court (red)
L.polygon([
    [41.600, -87.358], [41.600, -87.338], [41.590, -87.335], [41.590, -87.355]
], {color: '#dc2626', fillColor: '#dc2626', fillOpacity: 0.15, weight: 1}).addTo(map)
    .bindPopup("<strong>Modius's Court</strong><br><span class='pop-controller'>Prince of Gary — Toreador 7th</span>");

// The Rack / Torch strip (yellow)
L.polygon([
    [41.600, -87.350], [41.600, -87.338], [41.592, -87.335], [41.592, -87.348]
], {color: '#eab308', fillColor: '#eab308', fillOpacity: 0.15, weight: 1}).addTo(map)
    .bindPopup("<strong>The Rack</strong><br><span class='pop-controller'>The Torch + Broadway strip — feeding ground</span>");

// Darius's West Side (blue)
L.polygon([
    [41.593, -87.390], [41.593, -87.360], [41.575, -87.358], [41.575, -87.388]
], {color: '#2563eb', fillColor: '#2563eb', fillOpacity: 0.12, weight: 1}).addTo(map)
    .bindPopup("<strong>Darius's West Side</strong><br><span class='pop-controller'>Ventrue 10th — haven, feeding, pipeline staging</span>");

// Lucian's Docks (green)
L.polygon([
    [41.645, -87.455], [41.645, -87.425], [41.630, -87.420], [41.630, -87.450]
], {color: '#16a34a', fillColor: '#16a34a', fillOpacity: 0.15, weight: 1}).addTo(map)
    .bindPopup("<strong>Lucian's Docks</strong><br><span class='pop-controller'>Gangrel 8th, ~600 years — controls the waterfront</span>");

// Juggler's Wasteland (orange)
L.polygon([
    [41.635, -87.370], [41.635, -87.310], [41.618, -87.305], [41.618, -87.365]
], {color: '#f97316', fillColor: '#f97316', fillOpacity: 0.12, weight: 1}).addTo(map)
    .bindPopup("<strong>Juggler's Wasteland</strong><br><span class='pop-controller'>Brujah 8th — lakefront mill belt, anarch territory</span>");

// Telton Cemetery (purple)
L.polygon([
    [41.590, -87.338], [41.590, -87.322], [41.582, -87.320], [41.582, -87.336]
], {color: '#a855f7', fillColor: '#a855f7', fillOpacity: 0.12, weight: 1}).addTo(map)
    .bindPopup("<strong>Telton Cemetery</strong><br><span class='pop-controller'>Michael — Malkavian 9th (MISSING)</span>");

// Williams's Church district (grey, closed)
L.polygon([
    [41.582, -87.350], [41.582, -87.336], [41.574, -87.334], [41.574, -87.348]
], {color: '#78716c', fillColor: '#78716c', fillOpacity: 0.08, weight: 1, dashArray: '5,5'}).addTo(map)
    .bindPopup("<strong>Williams's Church District</strong><br><span class='pop-heat'>CLOSED — Operation burned. Williams destroyed.</span>");

// -- LOCATION MARKERS --

var iconRed = L.divIcon({className:'', html:'<div style="background:#dc2626;width:14px;height:14px;border-radius:50%;border:2px solid #fef2f2;box-shadow:0 0 6px rgba(220,38,38,0.6)"></div>', iconSize:[18,18], iconAnchor:[9,9]});
var iconBlue = L.divIcon({className:'', html:'<div style="background:#2563eb;width:14px;height:14px;border-radius:50%;border:2px solid #eff6ff;box-shadow:0 0 6px rgba(37,99,235,0.6)"></div>', iconSize:[18,18], iconAnchor:[9,9]});
var iconGreen = L.divIcon({className:'', html:'<div style="background:#16a34a;width:14px;height:14px;border-radius:50%;border:2px solid #f0fdf4;box-shadow:0 0 6px rgba(22,163,74,0.6)"></div>', iconSize:[18,18], iconAnchor:[9,9]});
var iconAmber = L.divIcon({className:'', html:'<div style="background:#d97706;width:14px;height:14px;border-radius:50%;border:2px solid #fffbeb;box-shadow:0 0 6px rgba(217,119,6,0.6)"></div>', iconSize:[18,18], iconAnchor:[9,9]});
var iconPurple = L.divIcon({className:'', html:'<div style="background:#a855f7;width:14px;height:14px;border-radius:50%;border:2px solid #faf5ff;box-shadow:0 0 6px rgba(168,85,247,0.6)"></div>', iconSize:[18,18], iconAnchor:[9,9]});
var iconGrey = L.divIcon({className:'', html:'<div style="background:#78716c;width:12px;height:12px;border-radius:50%;border:2px solid #d6d3d1;opacity:0.5"></div>', iconSize:[16,16], iconAnchor:[8,8]});
var iconWhite = L.divIcon({className:'', html:'<div style="background:#fafaf9;width:12px;height:12px;border-radius:50%;border:2px solid #78716c"></div>', iconSize:[16,16], iconAnchor:[8,8]});

// The Torch
L.marker([41.5940, -87.3450], {icon: iconAmber}).addTo(map)
    .bindPopup("<strong>The Torch</strong><br><span class='pop-controller'>Juggler (Kindred ops) / Victor (bar) / Darius (mortgage)</span><br><span class='pop-heat'>Torch Heat: 5/6 — FBI visited</span><br><div class='pop-desc'>Gary's only real nightclub. The Rack. Where predators and prey share a room.</div>");

// Modius's Mansion
L.marker([41.6120, -87.2570], {icon: iconRed}).addTo(map)
    .bindPopup("<strong>Modius's Mansion</strong><br><span class='pop-controller'>Modius — Prince of Gary, Toreador 7th</span><br><div class='pop-desc'>Miller Beach. Decaying steel-baron mansion. Elysium. The study with the self-portrait and the Auspex searchlight.</div>");

// Darius's Haven
L.marker([41.5830, -87.3720], {icon: iconBlue}).addTo(map)
    .bindPopup("<strong>Darius's West-Side Haven</strong><br><span class='pop-controller'>Darius Cole — Ventrue 10th (cover: 12th)</span><br><span class='pop-heat'>West Side Heat: 0/6</span><br><div class='pop-desc'>Ground-floor apartment. Check-cashing front. The architecture starts here.</div>");

// Lucian's Docks
L.marker([41.6380, -87.4400], {icon: iconGreen}).addTo(map)
    .bindPopup("<strong>Lucian's Docks / Gary Exports Co.</strong><br><span class='pop-controller'>Lucian — Gangrel 8th, ~600 years</span><br><span class='pop-heat'>Dock Pipeline: 3/6 — KEYED</span><br><div class='pop-desc'>Berth 7. Eddie Fells on night shift. The warehouse behind Gary Exports. The pipeline.</div>");

// Juggler's Ore Smelter
L.marker([41.6200, -87.3400], {icon: iconAmber}).addTo(map)
    .bindPopup("<strong>Juggler's Ore Smelter</strong><br><span class='pop-controller'>Juggler — Brujah 8th, Gary's fixer</span><br><span class='pop-heat'>Wasteland Heat: 1/6</span><br><div class='pop-desc'>Abandoned smelter. Catwalks, rust, slag. Where anarch energy meets industrial decay.</div>");

// Taconite Plant
L.marker([41.6230, -87.2950], {icon: iconRed}).addTo(map)
    .bindPopup("<strong>Modius's Taconite Plant</strong><br><span class='pop-controller'>Modius — fallback haven</span><br><div class='pop-desc'>Emergency bolt-hole. Proof the prince expects to lose the mansion someday.</div>");

// Telton Cemetery
L.marker([41.5850, -87.3300], {icon: iconPurple}).addTo(map)
    .bindPopup("<strong>Telton Cemetery</strong><br><span class='pop-controller'>Michael — Malkavian 9th (MISSING)</span><br><div class='pop-desc'>The quietest node. Danov drinks here. Dane watches from outside. Where Darius goes to visit Danov next.</div>");

// Williams's Church
L.marker([41.5780, -87.3430], {icon: iconGrey}).addTo(map)
    .bindPopup("<strong>Williams's Abandoned Church</strong><br><span class='pop-heat'>CLOSED — Williams destroyed, operation burned</span><br><div class='pop-desc'>Polk & 13th. Sable's secondary haven (basement). 43 entries in a dead man's notebook. The chain and the floor ring.</div>");

// City Methodist
L.marker([41.5937, -87.3464], {icon: iconWhite}).addTo(map)
    .bindPopup("<strong>City Methodist Church</strong><br><span class='pop-controller'>577 Washington Street — no controller</span><br><div class='pop-desc'>Largest Methodist church in the Midwest, built 1925, closed 1975. Roof gone, altar standing. Gary's most iconic ruin.</div>");

// Marlene Voss
L.marker([41.5810, -87.3900], {icon: iconBlue}).addTo(map)
    .bindPopup("<strong>Marlene Voss — Pawnshop</strong><br><span class='pop-controller'>Darius's fence / contact</span><br><div class='pop-desc'>West side. First real income. Deeply in debt.</div>");

// Warehouse (pipeline)
L.marker([41.6360, -87.4350], {icon: iconGreen}).addTo(map)
    .bindPopup("<strong>The Warehouse</strong><br><span class='pop-controller'>Darius — pipeline storage</span><br><span class='pop-heat'>Dock Pipeline: 3/6</span><br><div class='pop-desc'>Behind Gary Exports. Corrugated metal. 24 sacks of Sal Cantone's stolen product. Eddie Fells receives at Berth 7, walks it here.</div>");

</script>
