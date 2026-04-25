# 🎵 Spotify Global Top 50 — Power BI Dashboard

A 4-page interactive Power BI dashboard built on **18 months of daily Spotify Global Top 50 chart data** (May 2023 – November 2024). The project explores chart dominance, artist trajectory, song longevity, and content trends across 343 artists and 794 unique songs.

---

## 📌 Table of Contents

- [Project Overview](#project-overview)
- [Dashboard Pages](#dashboard-pages)
  - [Page 1 — Indexing](#page-1--indexing)
  - [Page 2 — Overview](#page-2--overview)
  - [Page 3 — Artist](#page-3--artist)
  - [Page 4 — Songs](#page-4--songs)
- [Key Insights](#key-insights)
- [DAX Measures Used](#dax-measures-used)
- [Dataset](#dataset)
- [Tools Used](#tools-used)
- [Author](#author)

---

## Project Overview

| Detail | Value |
|--------|-------|
| **Tool** | Microsoft Power BI Desktop |
| **Dataset rows** | 27,800 |
| **Date range** | 18 May 2023 → 27 November 2024 |
| **Total pages** | 4 |
| **Total visuals** | 40+ |
| **Unique artists** | 343 |
| **Unique songs** | 794 |

The goal was to go beyond basic "who has the most songs" charts and build insights that answer real questions — who *consistently ranks highest*, which artists are *growing vs fading*, which songs *dominated the longest*, and whether *explicit content* performs differently from clean songs.

---

## Dashboard Pages

---

### Page 1 — Indexing

> **Purpose:** Navigation home page

The landing page of the dashboard. Contains 4 navigation buttons that take the viewer directly to any section — Overview, Artist, or Songs. Keeps the report clean and professional without dumping all content on one page.

📸 *Screenshot: `screenshots(300).png`*

---

### Page 2 — Overview

> **Purpose:** High-level snapshot of the entire dataset

This page answers: *What does the Spotify Top 50 look like as a whole?*

**Visuals on this page:**

| Visual | Type | What it shows |
|--------|------|---------------|
| Songs by Artist | Bar Chart | Which artists appeared most frequently on the chart |
| Top Songs by Avg Popularity | Bar Chart | Highest popularity songs (ranked by average score) |
| Avg Popularity by Month | Area Chart | How chart popularity trended month by month |
| Songs by Album Type | Donut Chart | Split between Albums (71%), Singles (35%), Compilations |
| Explicit vs Non-Explicit | Donut Chart | 40% of charting songs carry explicit content |
| Avg Popularity by Album Type | Donut Chart | Whether album tracks or singles score higher |
| Songs per Artist by Month | Column Chart | Volume of new artists entering the chart each month |
| Avg Duration | KPI Card | Average song length — 3.28 minutes |
| Avg Popularity | KPI Card | Overall average popularity score — 89.6 / 100 |
| Distinct Songs | KPI Card | 794 unique songs charted across the period |
| Song & Artist Slicer | Slicer | Filter all visuals by song or artist name |

**Page story:**
The Overview reveals that album tracks dominate volume (71%) but singles punch above their weight in popularity. The monthly trend shows popularity fluctuates — summer months trend slightly higher. Taylor Swift leads appearances by a significant margin but the average popularity gap between top artists is narrow — competition for chart real estate is fierce.

📸 *Screenshot: `screenshots(297).png`*

---

### Page 3 — Artist

> **Purpose:** Deep dive into artist-level performance and trajectory

This is the strongest page of the dashboard. It answers a question most music dashboards miss: **not just who charted, but who ranked well, who stayed long, and who is growing or declining.**

**Visuals on this page:**

| Visual | Type | What it shows |
|--------|------|---------------|
| Top Artists by Avg Chart Position | Bar Chart | Artists ranked by average chart position — lower = consistently closer to #1 |
| Artist Weeks on Chart | Bar Chart | How many unique days each artist maintained a chart presence |
| Artists with Most Top 5 Finishes | Bar Chart | Count of times each artist ranked inside the Top 5 |
| Artist Trajectory: 2023 vs 2024 | Stacked Bar Chart | Days on chart split by year — reveals rising, fading, and breakout artists |
| Total Artists | KPI Card | 343 unique artists charted across the full period |
| Top Artist | KPI Card | Taylor Swift — 1,871 chart appearances |
| Song & Artist Slicer | Slicer | Filter all visuals by individual artist |

**Page story:**

**Avg Chart Position** reveals that Jung Kook & Latto (avg position 2.0) and Lady Gaga & Bruno Mars (avg position 1.6) rank higher on average than Taylor Swift (avg position ~18) — despite Swift having nearly 5× more appearances. More appearances does not equal better ranking.

**Artist Trajectory** is the standout visual of the entire dashboard. By splitting days on chart into 2023 vs 2024 segments, four artist categories emerge naturally:

- 🟢 **Rising** — Billie Eilish (143 → 277 days), Arctic Monkeys (224 → 324 days)
- 🔴 **Fading** — Bad Bunny (222 → 108 days), Harry Styles (217 → 158 days)
- 🟣 **2024 Breakouts** — Teddy Swims (0 → 324 days), Benson Boone (0 → 308 days), Sabrina Carpenter (0 → 267 days)
- 🔵 **Stable Legends** — Taylor Swift (225 → 292 days), KAROL G (217 → 251 days)

This single chart tells a story that no basic "songs by artist" count could reveal.

📸 *Screenshot: `screenshots(298).png`*

---

### Page 4 — Songs

> **Purpose:** Song-level analysis — prestige, longevity, and content type

This page answers: *Which songs matter the most, lasted the longest, and what type of content dominates?*

**Visuals on this page:**

| Visual | Type | What it shows |
|--------|------|---------------|
| Songs That Owned #1 the Longest | Bar Chart | Songs ranked by number of days they held the #1 position |
| Top Artists: Explicit vs Clean Songs | Stacked Bar Chart | Each artist's charting songs split by explicit vs clean content |
| Songs That Lasted: 2023 vs 2024 | Stacked Bar Chart | Song chart days split by year — shows longevity vs one-season hits |
| Song details table | Table | Song, release date, album type, avg popularity, duration |
| Song & Artist Slicer | Slicer | Filter all visuals by song name |

**Page story:**

**Songs That Owned #1 the Longest** shows that only 37 songs ever reached position #1 across 550+ days of data. *Die With A Smile* by Lady Gaga & Bruno Mars dominated the top spot for 77 days — nearly 3 months at #1. *Seven (feat. Latto)* by Jung Kook followed at 69 days.

**Explicit vs Clean Songs** reveals a sharp divide in artist strategies. Travis Scott, Drake, and Eminem chart 100% on explicit content. Taylor Swift charts 84% clean. Kendrick Lamar and Beyoncé split roughly evenly. This isn't just a content observation — it reflects fundamentally different target audiences.

**Songs That Lasted: 2023 vs 2024** shows that *Cruel Summer* and *I Wanna Be Yours* are true two-year chart legends, charting heavily in both years. *Lose Control* and *Beautiful Things* have zero 2023 presence — they are pure 2024 breakouts that exploded from nothing.

📸 *Screenshot: `screenshots(299).png`*

---

## Key Insights

**1. Appearance count ≠ Chart quality**
Taylor Swift has 1,871 appearances — the most of any artist — but averages position ~18. Jung Kook & Latto average position 2.0 with far fewer appearances. Volume and quality are completely different metrics.

**2. Bad Bunny lost 51% of chart presence from 2023 to 2024**
222 days in 2023 dropped to 108 in 2024. Meanwhile Billie Eilish nearly doubled from 143 to 277 days. The music landscape shifted significantly between the two years.

**3. Three pure 2024 breakouts had zero 2023 presence**
Teddy Swims, Benson Boone, and Sabrina Carpenter did not appear in 2023 at all. In 2024 they each clocked 260–324 chart days. These are not gradual risers — they exploded suddenly.

**4. Only 37 songs ever hit #1 across 550+ days of data**
Out of 794 unique songs, fewer than 5% ever reached the top position. The #1 spot is extremely rare real estate.

**5. Explicit content makes up 40% of charting songs**
Despite being restricted on many platforms and radio, explicit songs consistently chart. Among heavy-hitters like Travis Scott, Drake, and Eminem — 100% of their charting songs carry explicit content.

**6. Singles dominate chart entry, albums dominate volume**
Singles account for 35% of unique charting songs but tend to chart more intensely (higher popularity scores). Albums contribute 71% of volume but with more spread across position rankings.

---

## DAX Measures Used

All custom measures are stored in the `_measure` table inside the PBIX file.

```dax
-- Average chart position (quality metric)
Avg Position = AVERAGE('Top-50-world'[position])

-- Total unique artists
Total Unique Artists = DISTINCTCOUNT('Top-50-world'[artist])

-- Distinct songs count
Distinct Songs = DISTINCTCOUNT('Top-50-world'[song])

-- Average popularity
Avg Popularity = AVERAGE('Top-50-world'[popularity])

-- Average song duration in minutes
Avg Duration Minutes = AVERAGE('Top-50-world'[duration_ms]) / 60000

-- Explicit songs count
Explicit Songs = CALCULATE(
    DISTINCTCOUNT('Top-50-world'[song]),
    'Top-50-world'[is_explicit] = TRUE
)

-- Non-explicit songs count
Non Explicit Songs = CALCULATE(
    DISTINCTCOUNT('Top-50-world'[song]),
    'Top-50-world'[is_explicit] = FALSE
)

-- Days a song held the #1 position
Days at No1 = CALCULATE(
    COUNTROWS('Top-50-world'),
    'Top-50-world'[position] = 1
)

-- Top 5 finishes per artist
Top 5 Hits = CALCULATE(
    DISTINCTCOUNT('Top-50-world'[song]),
    'Top-50-world'[position] <= 5
)

-- Days on chart in 2023
Artist Days 2023 = CALCULATE(
    DISTINCTCOUNT('Top-50-world'[date]),
    YEAR('Top-50-world'[date]) = 2023
)

-- Days on chart in 2024
Artist Days 2024 = CALCULATE(
    DISTINCTCOUNT('Top-50-world'[date]),
    YEAR('Top-50-world'[date]) = 2024
)

-- Weeks on chart (total unique dates)
Weeks on Chart = DISTINCTCOUNT('Top-50-world'[date])

-- Song weeks in 2023
Weeks 2023 = CALCULATE(
    DISTINCTCOUNT('Top-50-world'[date]),
    YEAR('Top-50-world'[date]) = 2023
)

-- Song weeks in 2024
Weeks 2024 = CALCULATE(
    DISTINCTCOUNT('Top-50-world'[date]),
    YEAR('Top-50-world'[date]) = 2024
)

-- Peak chart position (best rank ever)
Peak Position = MIN('Top-50-world'[position])
```

---

## Dataset

**File:** `spotify-top-50-world.csv`
**Rows:** 27,800 | **Columns:** 11
**Period:** 18 May 2023 — 27 November 2024

| Column | Description |
|--------|-------------|
| `date` | Chart date |
| `position` | Chart rank that day (1 = top) |
| `song` | Song title |
| `artist` | Artist name |
| `popularity` | Spotify popularity score (0–100) |
| `duration_ms` | Song length in milliseconds |
| `album_type` | Album / Single / Compilation |
| `total_tracks` | Track count in the release |
| `release_date` | Original release date |
| `is_explicit` | TRUE / FALSE |
| `album_cover_url` | Spotify album art link |

> Note: `position` ranges 1–50. Lower is better. `popularity` is Spotify's live score — some songs show 0 if they were later delisted.

---

## Tools Used

| Tool | Purpose |
|------|---------|
| Power BI Desktop | Dashboard building, DAX measures, report design |
| Microsoft Excel | Initial data inspection |
| Power Query | Data type corrections, date formatting |

## Author

**Shivam Jaiswal**
B.Sc. Mathematics | Data Analytics Enthusiast
Currently upskilling in Power BI, Python, and Data Science

- 📧 Connect on [LinkedIn](https://www.linkedin.com/in/shivam-jaiswal-608748312/) ← 
- 📁 More projects on [GitHub](https://github.com/shivamjaiswal-data) 

---

*Built as part of a data analytics portfolio project — May 2026*
