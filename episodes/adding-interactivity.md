---
title: "Adding Interactivity with Pages and Filters"
teaching: 25
exercises: 15
---

::: questions
- How can I animate a visualization over time?
- How can filters help explore different aspects of a dataset?
- What options in Tableau help make visualizations more dynamic and readable?
:::

::: objectives
- Use the Pages shelf to animate a chart over time.
- Apply filters to limit and explore subsets of your data.
- Improve visualization clarity with labels, tooltips, and color.
:::

## Animation Using the Pages Shelf

We can animate our line chart to show how accidents accumulate over time.

::: checklist
- Duplicate your line chart worksheet (`Right-click > Duplicate`).
- Drag `Date Occurred` to the **Pages** shelf.
- Change the **Marks** type to `Circle` for better visibility.
- In the Pages card:
  - Click **Show History**
  - Set Marks to show history for **All**, and enable **Trails**
- Click the **Play** button in the Pages card to animate.

:::

::: callout
The Pages shelf lets you break visualizations into "frames" by a field—perfect for time-based animation.
:::

## Using Filters to Refine Visuals

Filters allow users to focus on specific subsets of data.

::: checklist
- Drag a field like `Area Name` to the **Filters** shelf.
- Select values to include, then click **Show Filter** from the dropdown menu.
- Tableau adds a filter widget to your view—users can now control the data dynamically.
:::

> You can change the filter style to a dropdown, checklist, slider, etc.

## Improving Readability

Small changes improve how users read and interpret your visualization:

- **Drag a field to Label** to annotate points or bars
- **Use Color** to differentiate categories
- **Hover** to preview tooltips and ensure they communicate clearly
- Use **Title** and **Axis Labels** to explain your chart

---

::: challenge
**Challenge: Filter and Customize a Histogram**

Using your histogram of `Time Occurred (bin)`, add a filter to let users explore different `Area Name` values.

- Can you make the title dynamic?
- Can you adjust the filter appearance for better UX?

::: hint
Double-click the title → Insert → select the filter field name.
:::

::: solution
- Drag `Area Name` to Filters → click **Show Filter**.
- Change filter style via dropdown menu.
- Double-click the chart title → Insert → `Area Name`.
:::
:::

---

::: keypoints
- The Pages shelf adds animation by slicing your visualization into steps.
- Filters let you focus on specific parts of your dataset.
- Labels, color, and dynamic titles help clarify what your visualization is showing.
:::
