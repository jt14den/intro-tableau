---
title: Setup
---

:::: caution
## Public data only

Tableau Public publishes workbooks to a public website, and the underlying data may be downloadable by anyone who views it. **Do not use this workshop's tools with sensitive, private, licensed, or restricted data.** The dataset used here is public and openly licensed.
::::

> These instructions were validated against **Tableau Desktop: Public Edition 2026.2.x**. Web authoring (public.tableau.com) and earlier desktop versions may use slightly different menus.

## Tableau Installation

This workshop uses **Tableau Desktop: Public Edition**, an installed desktop application, not the web-based authoring tool at public.tableau.com. Desktop: Public Edition can save workbooks locally on your computer and can also publish them to Tableau Public. It is free, but it is not licensed for commercial use, and workbooks you publish are visible to anyone.

1. Go to <https://www.tableau.com/products/public/download>.
2. Enter your information and click **Download the App**.
3. Install the application following the on-screen instructions.
4. Launch Tableau Desktop: Public Edition.

::: callout
## Already have institutionally licensed Tableau Desktop?

If your institution provides licensed **Tableau Desktop: Professional Edition** (for example, through a course or department license), you can use it instead — everything in this lesson works the same way. Follow your institution's instructions for activating that license; this lesson does not cover that process.
:::

### Pre-workshop check

Before the workshop, please:

1. Install Tableau Desktop: Public Edition (above) and confirm it launches.
2. Download the workshop dataset (below).
3. Open the CSV file in Tableau (`Connect > Text File`) and confirm you see a data preview. You do not need to build anything yet — we'll do that together in Episode 1.

If you run into trouble with any of these steps, please reach out before the workshop so we can help you get set up.

## Data Set

This workshop uses the **legacy LAPD Traffic Collision dataset**, a historical record of traffic collisions in the City of Los Angeles from 2010 through early 2026. LAPD stopped updating this dataset after transitioning to a new records management system; it remains published for historical reference only, and a separate, modernized collision dataset may eventually replace it. Because the data is no longer changing, it's well suited to a workshop: everyone works from the same numbers.

The data was transcribed from paper traffic reports, and the source notice cautions that it may contain inaccuracies. Locations with missing coordinates are recorded as `(0, 0)` rather than left blank — this is a sentinel value, not a "null point," and we'll filter it out when mapping in Episode 3.

- Source: [Traffic Collision Data from 2010 to Present](https://catalog.data.gov/dataset/traffic-collision-data-from-2010-to-present) (data.gov / LAPD, via the Los Angeles Open Data portal)
- Provider: Los Angeles Police Department
- Coverage: 2010 through the dataset's final update

**Download:**

1. Go to <https://data.lacity.org/Public-Safety/Traffic-Collision-Data-from-2010-to-Present/d5tf-ez2w/about_data>.
2. Click **Export** in the upper-right menu.
3. Choose **CSV** as the export format and click **Download**.
4. Save the file somewhere you can find it, and note the folder — you'll connect to this file in Episode 1.

::: callout
## Follow-up: fixed workshop snapshot

This live source can in principle be re-exported at any time, which means learners downloading on different days could get slightly different row counts. For a reproducible, dated snapshot (e.g. `traffic-collisions-2026-08-19.csv`, with the retrieval date recorded in this file and in the instructor notes), that snapshot has not yet been created. **This is a tracked follow-up**, not something silently added to this build — see the instructor notes for status. Until it exists, download fresh from the source above and record your retrieval date.
:::

### Optional: LAPD Divisions boundary data

Episode 3 includes an **optional** challenge that overlays LAPD division boundaries on the collision map. This is not required for the core lesson. If you want to try it:

1. Go to the [LAPD Divisions dataset page](https://geohub.lacity.org/datasets/lapd-divisions/about) on the LA GeoHub.
2. Download the shapefile or GeoJSON.
3. Unzip if needed, and keep the files together in one folder.

You can skip this and still complete every required part of the workshop.
