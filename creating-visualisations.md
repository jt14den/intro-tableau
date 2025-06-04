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

Welcome back! In this episode, we will take the data we've prepared and start building impactful visualizations. We'll explore how to create common chart types, such as line charts and histograms, and delve into the exciting world of mapping with geographic data.


## Line Chart: Accidents Over Time by Area

To start, let's visualize how the number of accidents changes over time, broken down by different areas. When thinking about a "time series" chart, we typically want time on our horizontal (x) axis. Let's examine our available time variables.

::: checklist

## Accidents over time

- Open a new worksheet. Let's rename this sheet `Accidents Over Time`.
- Drag `Date Occurred` to **Columns**. You'll notice it likely appears as a **blue pill** (discrete year).
- **Important:** Right-click `Date Occurred` on the Columns shelf → Convert to **Continuous** (choose `Year` under the green "Continuous" section). This transforms it into a **green pill**, representing a continuous timeline.
- Drag your calculated field, `Number of Accidents`, to **Rows**.
- To see trends for different areas, drag `Area Name` to **Color** under the Marks card. This will create a separate line for each area and generate a color legend.
- Double-click axis labels to rename them if desired, for example, from "SUM(Number of Accidents)" to "Number of Accidents."
:::

::: callout

#### Understanding Continuous vs. Discrete Dates

When you first drag a date field, Tableau often defaults to a "blue pill" (discrete), showing individual years as distinct categories. However, for visualizing trends *over time* along a continuous axis, a "green pill" (continuous) is essential. This creates a proper timeline, allowing for smooth lines and animations, which we'll explore later!

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

Next, let’s visualize how accident counts vary by the age of the victim. This will help us understand the distribution of accidents across different age groups.

::: checklist

1.  Create a new worksheet and rename it `Age Distribution of Accidents`.
2.  Drag `Victim Age` to **Columns**.
3.  Right-click on `Victim Age` on the Columns shelf and choose **Convert to Dimension**. *(Even though age is a number, we're treating it as a distinct category for each bar in this chart, rather than a continuous range for a single line.)*
4.  Drag `Number of Accidents` (your calculated field) to **Rows**.
5.  Change the Marks type from **Automatic** to **Bar**.
6.  Use the **Size** slider on the Marks card to reduce bar width and prevent overlap, making the bars easier to distinguish.
7.  Go to **Analysis > Show Mark Labels** to display the `Number of Accidents` directly on top of each bar.
:::::

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

## Optional: Refine Your Map Display

To improve readability and orientation:

- Go to **Map → Background Maps → Streets** to switch to a street-level basemap.
- Use the **Pan Tool** (click the hand icon) to move across the map.
- Remove null points by right-clicking on any point in the ocean (0,0) and selecting **Exclude**.


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
