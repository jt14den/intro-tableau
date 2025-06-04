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

Welcome to the final episode! Here, we'll bring together all the visualizations we've created into powerful, interactive dashboards. Dashboards are where your data story truly comes alive, allowing others to explore and understand your insights.


## What Is a Dashboard?

A **dashboard** in Tableau is a canvas where you can combine multiple charts and visual elements into a single interactive view. This allows users to compare different perspectives and present a lot more information in a smaller, cohesive frame.

::: checklist

### Creating a Dashboard

- Click the **Dashboard** icon (the middle tab at the bottom, typically between "New Worksheet" and "New Story").
- In the left sidebar, you'll see a list of all your created sheets. Drag your desired sheets (e.g., `Accidents Over Time (Animated)`, `Running Total Accidents Over Time`, and `Accident Map`) into the main dashboard area.
- Adjust the layout by dragging edges of the sheets or by setting the dashboard size to **Automatic** for flexible viewing.
- You can label your sheets directly on the dashboard by double-clicking the tab name at the bottom of each sheet you've added.
:::

## Adding Interactivity

This is where dashboards become truly powerful! You can make any sheet on your dashboard act as a filter for others, allowing users to interact with your data dynamically.

::: checklist

### Adding an Interactive Filter

- Click on a chart *inside* the dashboard that you want to use as a filter (e.g., your `Accident Map`).
- On the floating toolbar that appears when a chart is selected, click the **Use as Filter** icon (it looks like a funnel symbol).
- Repeat this step for any other views that should affect others interactively. For example, if you make your `Accidents Over Time (Animated)` sheet a filter as well.
:::

Now, when you click a specific value (e.g., a bar on a chart, or a specific area on a map), other views linked by the filter will respond instantly, updating to show only the data relevant to your selection. This dynamic interaction makes your dashboard a powerful exploration tool!

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
