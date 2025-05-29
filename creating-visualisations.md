---
title: "Visualizing Data with Charts and Maps"
teaching: 30
exercises: 20
---

::: questions
- How do I create a line chart, histogram, or map in Tableau?
- How do field types affect the kind of visualization Tableau creates?
- How can I use geographic data for mapping?
:::

::: objectives
- Create a line chart showing accidents over time by area.
- Use binned time data to generate a histogram.
- Create a basic map using latitude and longitude values.
:::

## Line Chart: Accidents Over Time by Area

We’ll create a line chart showing how accident counts vary by area over time.

::: checklist
- Open a new worksheet.
- Drag `Date Occurred` to **Columns** → right-click → Convert to **Continuous**.
- Drag `DR Number` to **Rows** → right-click → **Measure > Count**.
- Drag `Area Name` to **Color** under the Marks card.
- Double-click axis labels to rename them if desired.
:::

::: callout
A "blue pill" in Tableau means the field is discrete (e.g., individual years), while a "green pill" is continuous (e.g., time as a timeline).
:::

## Histogram: Accidents by Time of Day

Use the binned field created in the previous episode to examine accident frequency over time.

::: checklist

- Create a new worksheet.
- Drag `Time Occurred (bin)` to **Columns**.
- Drag the calculated field `Number of Accidents` to **Rows**.
- Optional: Drag `Area Name` to **Filters**, then click the filter card menu → **Show Filter**.

:::

::: callout
Histograms are ideal for showing the distribution of values across intervals—perfect for analyzing "Time Occurred."
:::

## Bar Chart: Accidents by Age

Let’s visualize how accident counts vary by age of victim.

1. Drag `Age` to **Columns`
2. Right-click and choose **Convert to Dimension**
3. Drag `Number of Accidents` (your calculated field) to **Rows**
4. Change the Marks type to **Bar**
5. Use **Size** to reduce bar width and prevent overlap
6. Go to **Analysis > Show Mark Labels**

::: challenge

**Interpret the Distribution**  
- Do any ages have unusual spikes?  
- What might cause them?  

(Hint: Consider estimation or rounding practices in field data collection.)

:::


## Map: Plotting Accidents in Los Angeles

If your dataset includes a `Location` column like `"34.05, -118.24"`:

::: checklist
- Right-click `Location` → **Split**.
- Rename the resulting fields `Latitude` and `Longitude`.
- Right-click each field → set **Data Type** to *Number (decimal)*.
- Set **Geographic Role**: `Latitude` and `Longitude`.
- Double-click both fields to generate a map.
- Use the map search bar to zoom to *Los Angeles*.
:::

Each point now represents a traffic incident.

::: challenge
**Challenge: Compare Accidents Across Areas**

Create a bar chart showing how accident counts compare across different police areas.

- Which field will you put on the x-axis (Columns)?
- Which field is best for the y-axis (Rows)?
- Can you improve the chart by adding `Color`, `Label`, or a `Filter`?

::: hint
Use `Area Name` for Columns and `Number of Accidents` as the Measure.
:::

::: solution
- Drag `Area Name` to **Columns**.
- Use `Number of Accidents` (COUNT of `DR Number`) on **Rows**.
- Optionally add `Number of Accidents` to **Label** for better readability.
:::
:::

::: keypoints
- Dragging fields to Columns and Rows defines the structure of your chart.
- The Show Me panel helps you quickly preview different visualization types.
- Latitude and longitude values can be transformed into map views using geographic roles.
:::
