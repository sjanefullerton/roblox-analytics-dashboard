# Roblox Analytics Dashboard

A browser-based analytics dashboard for Roblox game data. Upload your exported data and instantly see charts for player activity, combat, resources, retention, and more — all processed locally in your browser. Nothing is uploaded to a server or saved between sessions.

---

## How to use it

### Step 1 — Export your data from Roblox

Use the browser extension to download your CSVs from the Roblox Creator Dashboard. This will produce a folder called `roblox-exports` on your computer.

### Step 2 — Compress it into a zip

- **Mac:** Right-click the `roblox-exports` folder → **Compress**
- **Windows:** Right-click the `roblox-exports` folder → **Send to** → **Compressed (zipped) folder**

### Step 3 — Upload it to the dashboard

Go to the dashboard URL, drop your zip file onto the page (or click to browse), and your charts will appear in a few seconds.

That's it. Every time you want fresh data, repeat these steps. What you upload is what gets visualized — nothing carries over between sessions.

---

## Multiple experiences

If your zip contains more than one experience ID folder, a switcher appears at the top of the dashboard so you can flip between them. Each experience is processed independently.

---

## What the dashboard shows

The dashboard has five tabs. Which charts appear in each tab depends entirely on what data is in your zip — if a particular metric wasn't exported, that chart is simply skipped. Nothing will break if data is missing.

The **Overview** and **Players & Retention** tabs show standard Roblox metrics that are available for any experience. The **Combat**, **Farming & Resources**, and **Cow Pressure** tabs are driven by custom event data, so they will only populate if your experience tracks those events.

---

### Overview tab
A high-level snapshot of the experience's health.

- **Stat cards** — Peak daily active users, total nights survived, total aliens killed, and recent average session length at a glance. These pull from whatever standard and custom event data is available
- **Daily Active Users** — Player count over time, showing the full arc from pre-launch to present
- **Aliens Killed Per Day** — Total combat volume as a proxy for engagement (shows if your experience tracks this event)
- **Nights Survived Per Day** — How many players are completing full nights, a signal of progression depth (shows if your experience tracks this event)
- **Session Length Over Time** — Average minutes per session by day, useful for spotting onboarding improvements or drop-off
- **Session Retention Curve** — Of new players who started a session, what percentage were still playing at each minute mark. Shows current period vs previous period so you can see if onboarding is improving

---

### Combat tab
Detailed breakdown of combat and weapon activity. Only appears if your experience exports custom combat events.

- **Metric selector cards** — Click any card to pull up its daily chart. Cards show all-time total and peak day. Available metrics depend on what your experience tracks — may include aliens killed, turret kills, grenade kills, landmine kills, damage sustained, turret damage, players downed, players revived
- **Kill Source Comparison** — Weapon kill types side by side per day. Shows which weapon players lean on most and whether that shifts over time
- **Player Health Events** — Times downed vs times revived per day. A high downed-to-revived ratio means players aren't helping each other — useful for co-op balance tuning
- **Weapon Efficiency** — Average kills per grenade and per landmine over time. Rising efficiency can mean players are getting better, or that enemy density is increasing

---

### Farming & Resources tab
Everything related to the game's economy and resource loop. Only appears if your experience exports custom resource events.

- **Hay Grown vs Fed Per Day** — Are players growing enough hay to keep up with feeding demand? A persistent gap is a balance signal
- **Total Hay Fed to Cow (Cumulative)** — Running total of all hay fed, useful for comparing across days and spotting outlier sessions
- **Resource Economy (Timber / Stone / Gloop)** — For each resource: how much was created, spent, and left unspent at end of day. A large growing "remaining" stack means players aren't finding uses for it; a shrinking one under spend pressure may indicate a bottleneck
- **Trees Planted vs Harvested** — Tracks the forestry loop. If harvesting far outpaces planting, players may be depleting their tree stock
- **Turrets Placed Per Day** — Defense deployment volume. Spikes often correlate with harder nights or larger player counts

---

### Players & Retention tab
Engagement and demographic data. Available for any experience.

- **Session Retention Curve** — Full view of the new-player drop-off curve, current vs previous period. The steeper the early drop, the faster players are leaving in the first few minutes — the key window for onboarding hooks
- **Day 1 Retention** — What percentage of new players came back the next day. Industry baseline for casual games is typically 25–40%
- **Day 7 Retention** — What percentage of new players were still playing a week later. A stronger signal of whether the core loop is sticky
- **Age Group breakdown** — Share of monthly active users by age bracket
- **Gender breakdown** — Share of monthly active users by gender

---

### Cow Pressure tab
Tracks alien threat intensity and defensive performance. Only appears if your experience exports custom cow and combat events.

- **Stat cards** — Total abduction attempts, highest single-day cow drag sum, and all-time turret damage output
- **Alien Pressure Index** — Three metrics on one chart: how many times aliens grabbed the cow, cumulative cow drag distance, and total player damage sustained. Together these show how hard each night is hitting
- **Turret Performance** — Turret kills and turret damage on the same chart. If damage climbs but kills don't keep pace, enemies may be getting tankier or turret placement is less effective
- **Abduction Attempts Per Day** — Daily bar chart of how often aliens picked up the cow, useful for spotting nights that are overtuned or undertuned

---

## Notes

- **Nothing is stored** — All processing happens in your browser. Closing or refreshing the tab clears everything. Upload again to reload
- **Missing charts** — If a tab looks sparse or empty, it just means that data wasn't included in your export. No action needed
- **Partial exports work fine** — You don't need every possible CSV. Upload whatever you have and the dashboard will visualize what it can
