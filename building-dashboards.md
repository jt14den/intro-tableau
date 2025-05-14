---
title: "Building and Sharing Dashboards"
teaching: 20
exercises: 15
---

::: questions
- How do I combine multiple visualizations into a single dashboard?
- How can filters and interactivity be shared across charts?
- How do I publish or share Tableau Public visualizations?
:::

::: objectives
- Create a dashboard that brings together multiple views.
- Enable filtering across all visualizations in a dashboard.
- Save and share your dashboard using Tableau Public.
:::

## What Is a Dashboard?

A **dashboard** in Tableau is a canvas where you can combine multiple charts and visual elements into a single interactive view. This allows users to compare different perspectives and apply filters across charts.

## Creating a Dashboard

::: checklist
- Click the **Dashboard** icon (bottom tab next to sheets).
- In the left sidebar, drag your sheets into the dashboard area.
  - Example: `Line Chart`, `Histogram`, and `Map`.
- Adjust layout by dragging edges or setting size to **Automatic**.
- Label your sheets by double-clicking the tab name at the bottom.

:::

## Adding Interactivity

You can make any sheet act as a filter for others in the dashboard.

::: checklist
- Click on a chart inside the dashboard.
- Use the filter icon (funnel symbol) to **Use as Filter**.
- Repeat for any views that should affect others interactively.
:::

> Now, when you click a value (e.g., a bar or map area), other views will respond.

## Saving and Publishing to Tableau Public

Once you’re satisfied with your dashboard:

::: checklist
- Go to **File > Save to Tableau Public As...**
- Log in to your Tableau Public account.
- Name your workbook and save it.
- Tableau will open a browser with your published visualization.
- Click the **Share** icon to get an embed code or link.
:::

::: caution
All data in Tableau Public is public. Don’t upload sensitive or private data.
:::

---

::: challenge
**Challenge: Build and Publish a Dashboard**

Create a dashboard with at least two visualizations. Enable filter interactivity, and publish it to your Tableau Public profile.

- What story does your dashboard tell?
- Could someone unfamiliar with the data understand what they’re seeing?

::: hint
Add meaningful titles and tooltips to help interpret your charts.
:::

::: solution
- Combine the Line Chart and Map into one dashboard.
- Use `Area Name` as a filter.
- Add a dynamic title and test your dashboard in the browser.
:::
:::

---

::: keypoints
- Dashboards combine multiple charts into one interactive view.
- Filters and selections can link multiple charts together.
- Tableau Public lets you publish and share dashboards easily.
:::
