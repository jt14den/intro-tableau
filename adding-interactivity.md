---
title: "Adding Interactivity with Pages and Filters"
teaching: 25
exercises: 15
---

::: questions
- How can I animate a visualization by year using the Pages shelf?
- How can filters help explore different aspects of a dataset?
- What options in Tableau help make visualizations more dynamic and readable?
:::

::: objectives
- Use the Pages shelf to step a chart through one year at a time.
- Apply filters and filter cards to limit and explore subsets of your data.
- Improve visualization clarity with labels, tooltips, and color.
:::

In this episode, we'll add interactivity: a year-by-year animated bar chart using the Pages shelf, and filters that let a viewer explore subsets of the data.

## Animation Using the Pages Shelf

We'll build a self-contained bar chart that steps through one year of collision data at a time. Each page you see represents that year's collisions — the Pages shelf breaks the view into a sequence of frames, one per value of whatever field you put on it. It does not accumulate or carry totals forward from one page to the next.

::: checklist
1.  Open a new worksheet and rename it `Collisions by Area (Animated)`.
2.  Drag `Area Name` to **Rows**.
3.  Drag `Collision Count` to **Columns**.
4.  Confirm the Marks type is **Bar**.
5.  Drag `YEAR(Date Occurred)` — the discrete, blue Year — to the **Pages** shelf.
6.  Optional: right-click `Collision Count` on Columns → **Sort > Descending**, so the largest areas appear at the top or the bars are ordered by size.
7.  Click the **Play** button on the Pages card to step through years.
:::

::: callout
## Expected outcome
Each page shows one year's `Collision Count` by `Area Name` as a bar chart. As you click through years (or press Play), the bar lengths change to reflect that year's totals. This shows collisions **per year**, not a running or cumulative total — a bar shrinking from one year to the next means that year had fewer collisions, not that anything was "lost."
:::

::: callout
#### The Pages Shelf: your animation control

The Pages shelf breaks a view into frames based on the values of whatever field you place on it. Here, that's one frame per year. If you want a genuine running total instead, that's a different, separate calculation — see the optional extension below.
:::

::: challenge
#### Optional extension: a real running total

If you want a cumulative view, that requires a table calculation, not just the Pages shelf:

1. Duplicate your `Collisions by Area (Animated)` sheet and rename it `Running Total by Area`.
2. Right-click the `Collision Count` pill → **Quick Table Calculation > Running Total**.
3. This computes an actual running sum across the Pages sequence.

::: solution
The Pages shelf alone re-draws each year's independent value; a Running Total table calculation is what makes the number cumulative. Naming these two things the same thing is a common source of confusion — keep them separate in your own notes.
:::
:::

## Using Filters to Refine Visuals

Filters let users explore specific subsets of your data directly within the visualization.

::: checklist
- Drag a field like `Area Name` to the **Filters** shelf.
- In the filter dialog box, select the values you want to include, then click **OK**.
- Right-click the `Area Name` filter on the Filters shelf and select **Show Filter Card**.
:::

Tableau adds a **filter card** to your view — an interactive control, typically shown on the right side, that lets a viewer change which data is displayed without editing the underlying chart.

It's worth distinguishing four related but different things:

- **A field on the Filters shelf** — restricts the data in this one worksheet. Viewers can't change it unless a filter card is shown.
- **An interactive filter card** — the visible control (dropdown, list, slider) that lets a viewer change a filter's selected values.
- **Applying a filter to multiple worksheets** — a filter card can be set to affect just this sheet, or propagate to others (see below).
- **A dashboard filter action** — a separate mechanism, covered in Episode 5, where clicking a mark in one chart filters other charts on a dashboard.

::: callout

### Filter card display modes

Filter cards have several display modes, chosen from the card's own dropdown menu:

- **Single Value (List)**
- **Single Value (Dropdown)**
- **Multiple Values (List)**
- **Multiple Values (Dropdown)**

**Looking ahead:** in the next episode, we'll see how a filter card can be applied to every worksheet using the same data source, and how dashboard filter actions let clicking one chart filter others.

:::

## Improving Readability

Small changes improve how users read and interpret your visualization:

- **Drag a field to Label** to annotate points or bars
- **Use Color** to differentiate categories
- **Hover** to preview tooltips and ensure they communicate clearly
- Use a clear title and axis titles to explain your chart

## Editing a title

To edit a worksheet's title:

1. Right-click the title area (or open the title's dropdown menu) and choose **Edit Title...**
2. Use **Insert** in the Edit Title dialog to add a dynamic value, such as a field or parameter, into the title text.

::: challenge
**Challenge: Filter and Customize a Bar Chart**

Using your `Collisions by Hour` bar chart from Episode 3, add a filter to let users explore different `Area Name` values.

- Can you make the title dynamic?
- Can you adjust the filter card's display mode for better readability?

::: hint
Right-click the title → **Edit Title...** → **Insert** → select the filter field name.
:::

::: solution
- Drag `Area Name` to Filters → right-click the filter → **Show Filter Card**.
- Change the filter card's display mode via its dropdown menu.
- Right-click the chart title → **Edit Title...** → **Insert** → `Area Name`.
:::
:::

---

::: keypoints
- The Pages shelf steps a view through one frame per year — it shows each year's own values, not a running total.
- A genuine cumulative view requires a Running Total table calculation, a separate feature from Pages.
- A field on the Filters shelf, a filter card, and a dashboard filter action are three different things.
- Filter cards have specific display modes: Single Value (List), Single Value (Dropdown), Multiple Values (List), Multiple Values (Dropdown).
- Labels, color, and dynamic titles help clarify what your visualization is showing.
:::
