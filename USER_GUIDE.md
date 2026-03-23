# Roblox Analytics Dashboard — User Guide

A browser-based analytics dashboard for Roblox game data. Upload your exported data and instantly see charts for player activity, engagement, retention, and custom game events — all processed locally in your browser. Nothing is uploaded to a server or saved between sessions.

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

If your zip contains more than one experience ID folder, a switcher appears just below the header so you can flip between them. Each experience is processed independently.

---

## What the dashboard shows

The dashboard has five tabs. Which charts appear depends entirely on what data is in your zip — if a metric wasn't exported, that chart is simply skipped. Nothing breaks if data is missing.

The **Overview** and **Players & Retention** tabs show standard Roblox metrics available for any experience. The **Combat**, **Farming & Resources**, and **Pressure** tabs are driven by custom event data and will only populate if your experience tracks those events.

---

### Overview tab
A high-level snapshot of the experience's health.

- **Stat cards** — Key numbers at a glance: peak daily active users, total custom event counts, and recent average session length. Pulls from whatever data is available in your export
- **Daily Active Users** — Player count over time, showing the full arc from pre-launch to present
- **Custom event totals** — Daily charts for any top-level custom events present in your export, giving a quick read on core activity volume
- **Session Length Over Time** — Average minutes per session by day, useful for spotting onboarding improvements or drop-off
- **Session Retention Curve** — Of new players who started a session, what percentage were still playing at each minute mark. Shows current period vs previous period so you can track whether onboarding is improving

---

### Combat tab
Detailed breakdown of combat and weapon-related custom events. Only appears if your experience exports combat events.

- **Metric selector cards** — Click any card to load its daily chart below. Each card shows the all-time total and peak day. Which metrics appear depends on what your experience tracks
- **Kill Source Comparison** — Compares kill counts from different weapon or ability types side by side per day, showing which players lean on most and whether that shifts over time
- **Player Health Events** — Tracks times players were downed vs revived per day — useful for co-op balance tuning
- **Weapon Efficiency** — Average kills per use for throwable or deployable weapons over time. Rising efficiency can mean players are improving or that enemy density has changed

---

### Farming & Resources tab
Tracks resource economy and progression loops. Only appears if your experience exports resource events.

- **Resource production vs consumption** — For each tracked resource: how much was created, how much was spent, and how much is left unspent at end of day. A growing unspent stack means players aren't finding uses for it; a depleting one may signal a bottleneck
- **Cumulative totals** — Running totals for key feeding or crafting actions, useful for comparing output across days
- **Planting and harvesting loops** — If your experience tracks plant/harvest cycles, this shows whether players are sustaining or depleting their resource sources
- **Deployable structures** — Daily counts of any structures or defenses placed, useful for spotting correlations with difficulty spikes or player count changes

---

### Players & Retention tab
Engagement and demographic data. Available for any experience.

- **Session Retention Curve** — Full view of the new-player drop-off curve, current vs previous period. The steeper the early drop, the faster players are leaving in the first few minutes — the critical window for onboarding
- **Day 1 Retention** — Percentage of new players who returned the next day. Industry baseline for casual games is typically 25–40%
- **Day 7 Retention** — Percentage of new players still playing a week later. A stronger signal of whether the core loop is sticky
- **Age Group breakdown** — Share of monthly active users by age bracket
- **Gender breakdown** — Share of monthly active users by gender

---

### Pressure tab
Tracks threat intensity and defensive performance for experiences with enemy pressure mechanics. Only appears if your experience exports relevant custom events.

- **Stat cards** — Quick totals for key pressure indicators: enemy actions, peak threat values, and defensive output
- **Pressure Index** — Multiple threat and damage metrics on one chart, showing how hard the game is hitting players over time and whether difficulty is increasing
- **Defensive Performance** — Compares defensive structure kills and damage output over time, useful for evaluating whether defenses are keeping pace with incoming threat
- **Threat Events Per Day** — Daily bar chart of a key enemy action (e.g. objective grabs, boss spawns), useful for spotting nights or sessions that are overtuned or undertuned

---

## Notes

- **Nothing is stored** — All processing happens in your browser. Closing or refreshing the tab clears everything. Upload again to reload
- **Missing charts** — If a tab looks sparse or empty, it just means that data wasn't included in your export. No action needed
- **Partial exports work fine** — You don't need every possible CSV. Upload whatever you have and the dashboard will visualize what it can
