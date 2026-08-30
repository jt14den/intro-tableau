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

In this episode, we'll transform our static visualizations into dynamic, interactive tools. We'll explore how to animate charts to reveal trends over time and how to empower users to examine specific subsets of your data using filters.


## Animation Using the Pages Shelf

We can animate our line chart to show how accidents accumulate over time. To do this without altering your original chart, it's a good practice to **duplicate** the existing worksheet.

::: checklist
- Duplicate your line chart worksheet (Right-click on the sheet tab > Duplicate).
- Drag `Date Occurred` to the **Pages** shelf. This creates a control panel for animation.
- Change the **Marks** type from `Automatic` to `Circle` for better visibility of individual data points as they move.
- In the Pages card:
    - Click **Show History**.
    - Set Marks to show history for **All**, and enable **Trails**. *(Choosing 'Trails' creates a nice line indicating the past path, with the circle marking the current point in time. 'Both' would show individual circles at every past point, which can get cluttered.)*
- Click the **Play** button in the Pages card to animate the content. Be patient, as rendering can sometimes take a moment, depending on your computer's performance and the size of the data.
::::

::: callout
#### The Pages Shelf: Your Animation Control

The Pages shelf enables you to break your visualizations into "frames" based on the values of a field, making it perfect for time-based animations. As the animation plays, you might observe lines "zigzagging" or crossing. This indicates that an area's relative ranking in accident counts might change over time.
:::

:::: challenge
#### Interpreting Your Animated Chart

As your chart animates, observe the evolving trends:
* Notice how lines grow and diverge over the years.
* Can you identify which areas consistently show higher accident counts?
* Do some areas, like 77th Street, visibly "take the lead" in cumulative accidents compared to others like Foothill?

This dynamic view helps reveal long-term patterns that a static chart might not.
::::


## Using Filters to Refine Visuals

Filters empower users to explore specific subsets of your data directly within the visualization. This is a fundamental step in making your charts more interactive and user-driven.

::: checklist

1. Drag a field like `Area Name` to the **Filters** shelf.
1. In the filter dialog box, select the specific values you wish to include, then click "OK".
1. Now, right-click on the `Area Name` filter on the Filters shelf and select **Show Filter** from the dropdown menu.
1. Tableau adds a filter widget to your view, typically on the right sidebar. Users can now control which data is displayed dynamically.
:::

:::: callout 

### Using Filters in Tableau 

You can change the filter style (e.g., to a dropdown, checklist, or slider) by clicking the small dropdown arrow in the top right of the filter widget in your view.

Filters are powerful, especially when building interactive dashboards. In the next episode, we'll see how filters on one sheet can be used to control all visualizations on a dashboard, creating a truly unified experience.

:::: 

## Improving Readability

Small changes improve how users read and interpret your visualization:

- Drag a field to Label** to annotate points or bars
- Use Color to differentiate categories
- Hover to preview tooltips and ensure they communicate clearly
- Use **Title** and **Axis Labels** to explain your chart

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
