---
title: "In-Game Calendar"
description: "Timeline of Forged in Steel scenes — Darius and Sable's chronicle, day by day"
---

<style>
.calendar-timeline {
  max-width: 100%;
  margin: 2rem 0;
}

.calendar-entry {
  display: flex;
  align-items: flex-start;
  gap: 1rem;
  padding: 1rem;
  margin-bottom: 1rem;
  border-left: 4px solid #ccc;
  background: #fafafa;
  border-radius: 4px;
}

.calendar-entry.darius {
  border-left-color: #1e40af;
  background: rgba(30, 64, 175, 0.05);
}

.calendar-entry.sable {
  border-left-color: #8B0000;
  background: rgba(139, 0, 0, 0.05);
}

.calendar-badge {
  display: inline-block;
  padding: 0.4rem 1rem;
  border-radius: 20px;
  font-size: 1.05rem; line-height: 1.5;
  font-weight: 700;
  white-space: nowrap;
  margin-bottom: 0.75rem;
  letter-spacing: 0.5px;
}

.calendar-badge.darius {
  background: #1e40af;
  color: #fff;
}

.calendar-badge.sable {
  background: #8B0000;
  color: #fff;
}

.calendar-date {
  font-size: 1.1rem;
  color: #666;
  margin-bottom: 0.75rem;
  font-weight: 500;
}

.calendar-title {
  font-size: 1.75rem;
  font-weight: 700;
  color: #1A1A1A;
  margin-bottom: 0.5rem;
}

.calendar-link {
  color: #8B0000;
  text-decoration: underline;
  font-size: 1.5rem;
  font-weight: 600;
}

.calendar-link:hover {
  color: #A52A2A;
}

.calendar-filters {
  display: flex;
  gap: 1rem;
  margin-bottom: 2rem;
  flex-wrap: wrap;
}

.filter-btn {
  padding: 0.5rem 1rem;
  border: 2px solid #ccc;
  background: #fff;
  border-radius: 4px;
  cursor: pointer;
  font-size: 1.05rem; line-height: 1.5;
  font-weight: 500;
  transition: all 0.2s;
}

.filter-btn:hover {
  border-color: #8B0000;
}

.filter-btn.active.darius {
  background: #1e40af;
  color: #fff;
  border-color: #1e40af;
}

.filter-btn.active.sable {
  background: #8B0000;
  color: #fff;
  border-color: #8B0000;
}

.filter-btn.active.all {
  background: #666;
  color: #fff;
  border-color: #666;
}
</style>

<div class="calendar-filters">
  <button class="filter-btn active all" onclick="filterCalendar('all')">All Scenes</button>
  <button class="filter-btn darius" onclick="filterCalendar('darius')">Darius Only</button>
  <button class="filter-btn sable" onclick="filterCalendar('sable')">Sable Only</button>
</div>

<div class="calendar-timeline">

<div class="calendar-entry darius" data-pc="darius" data-date="1989-12-31">
<div>
<span class="calendar-badge darius">DARIUS</span>
<div class="calendar-date">December 31, 1989 — 11:47 PM</div>
<div class="calendar-title"><a href="/posts/chapter-01-new-years-eve/" class="calendar-link">Chapter 01: New Year's Eve</a></div>
<p style="margin: 0; color: #666; font-size: 1.05rem; line-height: 1.5;">The docks of Gary. A Ventrue's first night as one of the Kindred. Everything changes at midnight.</p>
</div>
</div>

<div class="calendar-entry sable" data-pc="sable" data-date="1990-01-01">
<div>
<span class="calendar-badge sable">SABLE</span>
<div class="calendar-date">January 1, 1990 — 1:00 AM</div>
<div class="calendar-title"><a href="/posts/chapter-02-the-torch/" class="calendar-link">Chapter 02: The Torch</a></div>
<p style="margin: 0; color: #666; font-size: 1.05rem; line-height: 1.5;">A Toreador enters Elysium for the first time. The bar called The Torch. Beauty and blood and danger.</p>
</div>
</div>

<div class="calendar-entry sable" data-pc="sable" data-date="1990-01-04">
<div>
<span class="calendar-badge sable">SABLE</span>
<div class="calendar-date">January 4, 1990 — 9:00 PM</div>
<div class="calendar-title"><a href="/posts/haven/" class="calendar-link">Haven</a></div>
<p style="margin: 0; color: #666; font-size: 1.05rem; line-height: 1.5;">A place to rest. A place to hide. Gary offers shelter to those who understand the dead city.</p>
</div>
</div>

<div class="calendar-entry darius" data-pc="darius" data-date="1990-01-05">
<div>
<span class="calendar-badge darius">DARIUS</span>
<div class="calendar-date">January 5, 1990 — 10:15 PM</div>
<div class="calendar-title"><a href="/posts/chapter-03-the-bookie/" class="calendar-link">Chapter 03: The Bookie</a></div>
<p style="margin: 0; color: #666; font-size: 1.05rem; line-height: 1.5;">Sal's office. Numbers and blood. A Ventrue learns how power flows through Gary's underworld.</p>
</div>
</div>

<div class="calendar-entry sable" data-pc="sable" data-date="1990-01-05">
<div>
<span class="calendar-badge sable">SABLE</span>
<div class="calendar-date">January 5, 1990 — 8:00 PM</div>
<div class="calendar-title"><a href="/posts/elysium/" class="calendar-link">Elysium</a></div>
<p style="margin: 0; color: #666; font-size: 1.05rem; line-height: 1.5;">Modius holds court. The Camarilla's rules of engagement. A Toreador navigates the political waters.</p>
</div>
</div>

<div class="calendar-entry sable" data-pc="sable" data-date="1990-01-08">
<div>
<span class="calendar-badge sable">SABLE</span>
<div class="calendar-date">January 8, 1990 — 10:00 PM</div>
<div class="calendar-title"><a href="/posts/the-accommodation/" class="calendar-link">The Accommodation</a></div>
<p style="margin: 0; color: #666; font-size: 1.05rem; line-height: 1.5;">A studio apartment. A choice. A Toreador's night of reckoning and survival.</p>
</div>
</div>

<div class="calendar-entry darius" data-pc="darius" data-date="1990-01-11">
<div>
<span class="calendar-badge darius">DARIUS</span>
<div class="calendar-date">January 11, 1990 — 9:30 PM</div>
<div class="calendar-title"><a href="/posts/chapter-04-thursdays/" class="calendar-link">Chapter 04: Thursdays</a></div>
<p style="margin: 0; color: #666; font-size: 1.05rem; line-height: 1.5;">The cemetery. Surveillance. A Ventrue watches and learns. Some nights, you hunt. Some nights, you watch.</p>
</div>
</div>

<div class="calendar-entry darius" data-pc="darius" data-date="1990-01-14">
<div>
<span class="calendar-badge darius">DARIUS</span>
<div class="calendar-date">January 14, 1990 — 11:30 PM</div>
<div class="calendar-title"><a href="/posts/chapter-05-the-shipment/" class="calendar-link">Chapter 05: The Shipment</a></div>
<p style="margin: 0; color: #666; font-size: 1.05rem; line-height: 1.5;">Dock 7. The weight of Gary. A Ventrue's second move in the game of power.</p>
</div>
</div>

<div class="calendar-entry sable" data-pc="sable" data-date="1990-01-12">
<div>
<span class="calendar-badge sable">SABLE</span>
<div class="calendar-date">January 12, 1990 — 10:00 PM</div>
<div class="calendar-title"><a href="/posts/the-mirror/" class="calendar-link">The Mirror</a></div>
<p style="margin: 0; color: #666; font-size: 1.05rem; line-height: 1.5;">Allicia's studio on Fifth Avenue. Pointe shoes on a barre. The woman who came before.</p>
</div>
</div>

<div class="calendar-entry sable" data-pc="sable" data-date="1990-01-13">
<div>
<span class="calendar-badge sable">SABLE</span>
<div class="calendar-date">January 13, 1990 — 11:50 PM</div>
<div class="calendar-title"><a href="/posts/the-oasis/" class="calendar-link">The Oasis</a></div>
<p style="margin: 0; color: #666; font-size: 1.05rem; line-height: 1.5;">The strip club on 75th Street. A meeting with Allicia. A warning about blood and love and the distance between them.</p>
</div>
</div>

<div class="calendar-entry darius" data-pc="darius" data-date="1990-01-17">
<div>
<span class="calendar-badge darius">DARIUS</span>
<div class="calendar-date">January 17, 1990 — 10:00 PM</div>
<div class="calendar-title"><a href="/posts/chapter-06-aftermath/" class="calendar-link">Chapter 06: Aftermath</a></div>
<p style="margin: 0; color: #666; font-size: 1.05rem; line-height: 1.5;">A detective's memory erased. A gift delivered. Two new faces planted. The architecture holds.</p>
</div>
</div>

<div class="calendar-entry darius" data-pc="darius" data-date="1990-02-02">
<div>
<span class="calendar-badge darius">DARIUS</span> <span class="calendar-badge sable">SABLE</span>
<div class="calendar-date">February 2, 1990 — 9:00 PM</div>
<div class="calendar-title"><a href="/posts/february-elysium/" class="calendar-link">Elysium (Convergence)</a></div>
<p style="margin: 0; color: #666; font-size: 1.05rem; line-height: 1.5;">February court at Modius's mansion. Two neonates meet for the first time. The game changes.</p>
</div>
</div>

<div class="calendar-entry darius" data-pc="darius" data-date="1990-06-15">
<div>
<span class="calendar-badge darius">DARIUS</span> <span class="calendar-badge sable">SABLE</span>
<div class="calendar-date">February — June 1990</div>
<div class="calendar-title"><a href="/posts/bluebooking-the-distance/" class="calendar-link">The Distance (Bluebooking)</a></div>
<p style="margin: 0; color: #666; font-size: 1.05rem; line-height: 1.5;">Four months between scenes. Two neonates circle each other in a dying city. Neither blinks first.</p>
</div>
</div>

</div>

<script>
function filterCalendar(pc) {
  const entries = document.querySelectorAll('.calendar-entry');
  const buttons = document.querySelectorAll('.filter-btn');

  // Update button states
  buttons.forEach(btn => btn.classList.remove('active'));
  event.target.classList.add('active');

  // Filter entries
  entries.forEach(entry => {
    if (pc === 'all') {
      entry.style.display = 'flex';
    } else if (entry.dataset.pc === pc) {
      entry.style.display = 'flex';
    } else {
      entry.style.display = 'none';
    }
  });
}
</script>

---

## Overview

The chronicle began on **New Year's Eve 1989** and continues into **January 1990**. Each scene is timestamped and linked to the full narrative posts.

**Darius Cole** (Ventrue, male) — scenes marked in **blue**
**Sable Price** (Toreador, female) — scenes marked in **blood red**

Use the filters above to view scenes by character, or scroll through the full timeline to see how the two chronicles interweave across Gary's nights.
