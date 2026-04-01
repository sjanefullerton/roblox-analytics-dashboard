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

If your zip contains more than one experience ID folder, the dashboard opens in **All Experiences** mode by default, with four cross-experience comparison tabs. An experience bar appears just below the header — click any individual experience ID to switch into a single-experience deep-dive, or click **All Experiences** to return to the comparison view.

---

## All Experiences mode

When multiple experiences are present, these four tabs appear and let you compare data across all of them at once. Each chart shows one line or bar per experience, colour-coded consistently throughout.

### Summary

The first tab in All Experiences mode. A flexible comparison view for any standard metric across experiences.

- **Stat cards** — Peak DAU and average session length for every experience
- **Metric dropdown** — Choose what to compare: DAU, average session length, sessions per day, unique players, Day 1 / Day 7 / Day 30 retention, DAU/MAU stickiness, playtime, revenue, paying users, and more. Only metrics present in your data appear
- **Experience pills** — Each experience gets a colour-coded pill. Click to deselect any you don't want on the chart; click again to re-add them. Any combination works
- **Line / Bar toggle:**
  - **Line** — Plots the selected metric over time, one line per experience. Best for spotting trends and seeing where experiences diverge
  - **Bar** — Shows each experience's period average as a single bar. Best for a clean snapshot comparison
- **Benchmark** — When Roblox provides a platform average for the selected metric, it appears as a dashed grey line. In bar mode it shows as a flat dashed line across the bars so you can see how each experience compares to the platform norm

### Event Comparison

The most flexible cross-experience view. Pick any custom event and any breakdown dimension.

- **Event dropdown** — Selects which custom event to compare across experiences
- **Breakdown dropdown** — If your data includes dimension breakdowns (session number, level/night, player count, weapon type, reason), you can split the charts by that dimension. Selecting a dimension adds per-experience mini bar charts showing how that breakdown looks for each experience individually
- **Daily trend chart** — One line per experience showing the event over time
- **All-time total and daily average charts** — Quick volume comparison across experiences

### Retention

Compare player retention and engagement metrics across experiences on the same chart.

- **Metric dropdown** — Choose from Day 1 / Day 7 / Day 30 retention, DAU/MAU stickiness, daily active users, session length, playtime, or unique players
- **Stat cards** — Recent 30-day average and all-time peak for each experience for the selected metric
- **Trend chart** — All experiences on the same timeline
- **Recent average and peak charts** — Bar charts summarising each experience's performance at a glance

### Stats Overview

Side-by-side tables and chart visualisers for all available standard metrics and custom event totals.

- **Standard metrics table** — Peak DAU, average session length, total sessions, unique players, average retention rates, revenue figures — one column per experience
- **Custom event totals table** — All-time total for every custom event, one column per experience
- **Metric chart** — Dropdown to pick any standard metric and plot all experiences over time
- **Event chart** — Dropdown to pick any custom event and plot all experiences over time

---

## Single-experience mode

Click any experience ID in the experience bar to switch into a per-experience deep-dive. Which tabs appear depends on what data is in your zip. The **Overview**, **Players**, and **Game Stats** tabs are always present. All other tabs are driven by your custom event data and only appear if the relevant breakdowns were included in your export. Nothing breaks if data is missing — charts are simply skipped.

The tab order is:

**Overview → Event Trends → Level / Night → Session Curve → Player Count → Weapons & Tools → Reason Breakdown → Players → Game Stats**

---

### Overview

The first thing you see after uploading (or after selecting a single experience). Gives you the big picture before diving into specifics.

- **Stat cards** — Key numbers at a glance: peak daily active users, recent average session length, and all-time totals for your top custom events
- **Daily Active Users** — Player count over time, showing the full arc of your experience's traffic

---

### Event Trends

A flexible explorer for your custom event data. Shows daily totals over time.

- **Metric pills** — Click any event name to load it onto the chart. Select multiple to compare them side by side on the same axis
- Useful for spotting spikes, drops, or correlations between different in-game actions over time

Only appears if your export includes custom events.

---

### Level / Night

How each tracked metric distributes across progression stages — nights, levels, waves, or whatever your experience uses.

- **All-time total bar chart** — The primary view. Each bar is one stage, so you can immediately see which are hardest or have the most activity
- **Daily trend line chart** — Shows how each stage's numbers changed over time as the game evolved or the player base shifted

Only appears if your export includes level or night-number breakdowns.

---

### Session Curve

Compares player activity across their 1st, 2nd, and 3rd+ sessions. The key view for understanding whether players are getting better at your game over time.

- **Main line chart** — Shows one metric across all three session groups as a daily trend. Select different metrics using the pills above
- **Snapshot bar charts** — Six of your top metrics shown side by side for the most recent day, each split by 1st / 2nd / 3rd+ session

What to look for: if a metric rises from 1st → 2nd → 3rd+ session, players are learning and improving. If values are flat or falling, the game may need clearer onboarding or earlier payoff.

Only appears if your export includes session-number breakdowns.

---

### Player Count

How each metric scales depending on how many players are in a session together. Useful for spotting whether your game plays very differently solo vs. in a group.

- **All-time total bar chart** — The primary view. Each bar is a player count (1 player, 2 players, etc.), so you can immediately compare activity levels across group sizes
- **Daily trend line chart** — Shows how each group size's numbers changed over time

Only appears if your export includes player-count breakdowns.

---

### Weapons & Tools

Which weapons or tools players use most, and how that shifts over time. Useful for spotting dominant strategies and underused options that may need rebalancing.

- **All-time total bar chart** — Each bar is one weapon or tool type, ranked by total usage. Immediately shows what players gravitate toward
- **Daily line chart** — Shows each weapon's daily usage trend so you can see if preferences shift after updates

Only appears if your export includes weapon or tool breakdowns.

---

### Reason Breakdown

How each tracked metric splits by reason category — for example why sessions ended, how events were triggered, or how outcomes were classified.

- **All-time total bar chart** — Each bar is one reason category
- **Daily trend line chart** — Shows how each reason's numbers changed over time

Only appears if your export includes reason breakdowns.

---

### Players

Engagement and demographic data. Available for any experience.

- **Session Retention Curve** — Of new players who started a session, what percentage were still playing at each minute mark. Shows current period vs previous period so you can track whether onboarding is improving. A steep early drop means players are leaving in the first few minutes — the critical window
- **Day 1 Retention** — Percentage of new players who returned the next day
- **Day 7 Retention** — Percentage of new players still playing a week later. A stronger signal of whether the core loop is sticky
- **Age Group breakdown** — Horizontal bar chart showing share of monthly active users by age bracket
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
