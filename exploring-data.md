---
title: "Exploring and Cleaning Your Data"
teaching: 25
exercises: 15
---

::: questions
- How does Tableau interpret and categorize data types?
- What are Dimensions and Measures?
- How do I identify and prepare fields for visualization?
:::

::: objectives
- Understand Tableau's automatic data typing (dimensions vs. measures).
- Explore the Show Me panel to preview visualization options.
- Use calculated fields and binning to prepare data for charts.
:::

## Dimensions and Measures

After loading your dataset and opening a worksheet, you'll notice that Tableau classifies your columns as either:

- **Dimensions** (blue pills): qualitative data like names, IDs, or categories.
- **Measures** (green pills): quantitative data that can be aggregated, such as counts or amounts.

> Tip: You can change a field's classification by right-clicking and selecting **Convert to Dimension** or **Convert to Measure**.

## Discrete vs. Continuous

Tableau also distinguishes between:

- **Discrete** fields: Separate values like city names, months, or categories.
- **Continuous** fields: Numeric or time-based fields used on a continuous scale.

> Discrete = blue  
> Continuous = green

## Exploring the Data with Show Me

The **Show Me** panel suggests visualizations based on the fields you've selected.

Try this:

1. Select `Area Name` and `DR Number`
2. Click on different chart types in the **Show Me** panel
3. See how Tableau updates the chart preview dynamically

## Creating a Calculated Field

You can create new fields to better control your visualizations.

To count the number of traffic accidents:

1. Right-click in the Data pane → **Create Calculated Field**
2. Name it: `Number of Accidents`
3. Formula: `COUNT([DR Number])`

This new measure will appear in your data pane.

## Creating Bins (for Time of Day)

To examine accident frequency across different times of day:

1. Right-click on `Time Occurred` → **Duplicate**
2. Right-click the duplicate → **Convert to Dimension**
3. Right-click again → **Create Bins**
4. Set bin size to `100`

This creates a new field like `Time Occurred (bin)` that groups records by hour.

---

:::: challenge

1. Use Show Me to try 3 different chart types with `Area Name`, `Date Occurred`, and `DR Number`.
2. Create a calculated field to count accidents.
3. Create a binned version of `Time Occurred`.
4. Which fields would be good candidates for filters in a dashboard?

:::::::

---
:::: callout

Think about what each field *represents* and how it might be grouped or summarized. Clean, consistent values (like standardized department names) make visualizations more readable and accurate.
:::: 


::: keypoints
- Tableau automatically classifies data into dimensions (categorical) and measures (quantitative).
- The "Show Me" panel suggests visualization types based on selected data.
- Data preparation, including binning and calculated fields, improves visualization clarity.
:::
