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

Which charts appear depends entirely on what data is in your zip — if a metric wasn't exported, that chart is simply skipped. Nothing breaks if data is missing.

The **Overview** and **Players & Retention** tabs show standard Roblox metrics available for any experience. Any additional tabs are driven by custom event data specific to your experience and will only appear if your export includes those events.

---

### Overview tab
A high-level snapshot of the experience's health.

- **Stat cards** — Key numbers at a glance: peak daily active users, total custom event counts, and recent average session length. Pulls from whatever data is available in your export
- **Daily Active Users** — Player count over time, showing the full arc from pre-launch to present
- **Custom event totals** — Daily charts for any top-level custom events present in your export, giving a quick read on core activity volume
- **Session Length Over Time** — Average minutes per session by day, useful for spotting onboarding improvements or drop-off
- **Session Retention Curve** — Of new players who started a session, what percentage were still playing at each minute mark. Shows current period vs previous period so you can track whether onboarding is improving

---

### Custom event tabs
Any tabs beyond Overview and Players & Retention are built from your experience's custom events. Which tabs appear and what they contain will vary depending on what your experience tracks. Examples of what these tabs can show:

- **Metric selector cards** — Click any card to load its daily chart. Each card shows the all-time total and peak day
- **Activity comparisons** — Multiple related metrics plotted side by side per day, showing how different systems interact over time
- **Economy tracking** — For each tracked resource: how much was created, spent, and left unspent at end of day
- **Efficiency metrics** — Average output per action over time, useful for spotting whether players are improving or whether balance has shifted
- **Event counts per day** — Bar charts of key in-game actions, useful for spotting sessions or time periods that are overtuned or undertuned
- **Player health and progression** — Tracks events like players being downed or revived, structures placed, or objectives completed

---

### Players & Retention tab
Engagement and demographic data. Available for any experience.

- **Session Retention Curve** — Full view of the new-player drop-off curve, current vs previous period. The steeper the early drop, the faster players are leaving in the first few minutes — the critical window for onboarding
- **Day 1 Retention** — Percentage of new players who returned the next day. Industry baseline for casual games is typically 25–40%
- **Day 7 Retention** — Percentage of new players still playing a week later. A stronger signal of whether the core loop is sticky
- **Age Group breakdown** — Share of monthly active users by age bracket
- **Gender breakdown** — Share of monthly active users by gender

---

## Notes

- **Nothing is stored** — All processing happens in your browser. Closing or refreshing the tab clears everything. Upload again to reload
- **Missing charts** — If a tab looks sparse or empty, it just means that data wasn't included in your export. No action needed
- **Partial exports work fine** — You don't need every possible CSV. Upload whatever you have and the dashboard will visualize what it can
