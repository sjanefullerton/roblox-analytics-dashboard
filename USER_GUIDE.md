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

Which tabs appear depends entirely on what data is in your zip. The **Overview**, **Players**, and **Game Stats** tabs are always present. All other tabs are driven by your custom event data and only appear if the relevant breakdowns were included in your export. Nothing breaks if data is missing — charts are simply skipped.

The tab order is:

**Overview → Event Trends → Night by Night → Learning Curve → Player Count → Weapons & Tools → Players → Game Stats**

---

### Overview

The first thing you see after uploading. Gives you the big picture before diving into specifics.

- **Stat cards** — Key numbers at a glance: peak daily active users, recent average session length, and all-time totals for your top custom events
- **Daily Active Users** — Player count over time, showing the full arc of your experience's traffic

---

### Event Trends

A flexible explorer for your custom event data. Shows daily totals over time.

- **Metric pills** — Click any event name to load it onto the chart. Select multiple to compare them side by side on the same axis
- Useful for spotting spikes, drops, or correlations between different in-game actions over time

Only appears if your export includes custom events.

---

### Night by Night

How each tracked metric distributes across night numbers (or equivalent progression stages in your experience).

- **All-time total bar chart** — The primary view. Each bar is one night number, so you can immediately see which nights have the most or least activity. Taller bars = more of that metric happening on that night
- **Daily trend line chart** — Below the bar chart, shows how each night's numbers changed over time as the game evolved or the player base shifted

Only appears if your export includes night-number breakdowns.

---

### Learning Curve

Compares player activity across their 1st, 2nd, and 3rd+ sessions. This is the key view for understanding whether players are getting better at your game over time.

- **Main line chart** — Shows one metric across all three session groups as a daily trend. Select different metrics using the pills above
- **Snapshot bar charts** — Six of your top metrics shown side by side for the most recent day, each split by 1st / 2nd / 3rd+ session

What to look for: if a metric rises from 1st → 2nd → 3rd+ session, players are learning and improving. If values are flat or falling, the game may need clearer onboarding or earlier payoff.

Only appears if your export includes session-number breakdowns.

---

### Player Count

How each metric scales depending on how many players are in a session together. Useful for spotting whether your game plays very differently solo vs. in a group.

- **All-time total bar chart** — The primary view. Each bar is a player count (1 player, 2 players, etc.), so you can immediately compare activity levels across group sizes
- **Daily trend line chart** — Below the bar chart, shows how each group size's numbers changed over time

Only appears if your export includes player-count breakdowns.

---

### Weapons & Tools

Which weapons or tools players use most, and how that shifts over time. Useful for spotting dominant strategies and underused options that may need rebalancing.

- **All-time total bar chart** — Each bar is one weapon or tool type, ranked by total usage. Immediately shows what players gravitate toward
- **Daily line chart** — Shows each weapon's daily usage trend so you can see if preferences shift after updates

Only appears if your export includes weapon or tool breakdowns.

---

### Players

Engagement and demographic data. Available for any experience.

- **Session Retention Curve** — Of new players who started a session, what percentage were still playing at each minute mark. Shows current period vs previous period so you can track whether onboarding is improving over time. A steep early drop means players are leaving in the first few minutes — the critical window
- **Day 1 Retention** — Percentage of new players who returned the next day
- **Day 7 Retention** — Percentage of new players still playing a week later. A stronger signal of whether the core loop is sticky
- **Age Group breakdown** — Horizontal bar chart showing share of monthly active users by age bracket. Easier to compare group sizes than a pie chart
- **Gender breakdown** — Horizontal bar chart showing share of monthly active users by gender

---

### Game Stats

Standard Roblox platform metrics. This tab is intentionally last since most of this data is also visible directly in the Roblox Creator Dashboard.

- **Stat cards** — Peak DAU, average session length, total sessions
- **Daily Active Users** — Full time-series of player count
- **Session Length Over Time** — Average minutes per session by day
- **Sessions Per Day** — Total daily session count

---

## Notes

- **Nothing is stored** — All processing happens in your browser. Closing or refreshing the tab clears everything. Upload again to reload
- **Missing charts** — If a tab looks sparse or a chart is missing, it just means that data wasn't included in your export. No action needed
- **Partial exports work fine** — You don't need every possible CSV. Upload whatever you have and the dashboard will visualize what it can
