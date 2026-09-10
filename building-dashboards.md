---
title: "Building and Sharing Dashboards"
teaching: 20
exercises: 15
---

::: questions
- How do I combine multiple visualizations into a single dashboard?
- How can filters and interactivity be shared across charts?
- How do I publish or share a Tableau Public visualization?
:::

::: objectives
- Create a dashboard that brings together multiple views.
- Enable filter actions and shared filters across a dashboard.
- Save and share a dashboard using Tableau Public, with attention to accessibility and privacy.
:::

Welcome to the final episode! Here, we'll bring together the visualizations we've built — `Collisions Over Time`, `Collisions by Hour`, `Age Distribution`, `Collision Map`, and `Collisions by Area (Animated)` — into an interactive dashboard.

## What Is a Dashboard?

A **dashboard** in Tableau is a canvas where you combine multiple worksheets and other visual elements into a single interactive view, letting users compare different perspectives at once.

::: checklist

### Creating a Dashboard

- Click the **New Dashboard** icon (the middle tab at the bottom, between "New Worksheet" and "New Story").
- In the left sidebar, you'll see a list of your created sheets. Drag `Collisions Over Time` and `Collision Map` into the dashboard area.
:::

## Layout: Tiled vs. Floating

Tableau places dashboard objects in one of two ways:

- **Tiled** objects snap into a grid alongside other objects and automatically resize as you add or move things — predictable and easiest to keep organized. This is the default and what we recommend for this workshop.
- **Floating** objects sit at a fixed position and can overlap other objects — more flexible for layering elements like a logo or a text box over a chart, but easier to make a mess of.

Stick with **tiled** placement (and layout containers, which group tiled objects together) for your first dashboard. Floating is worth exploring later once you're comfortable with the basics.

::: checklist
### Sizing your dashboard

- In the Dashboard pane on the left, set **Size** to a fixed desktop size (for example, `1000 x 800`) rather than **Automatic** for this workshop. A fixed size makes the layout predictable while you're learning; **Automatic** sizing and device-specific layouts (desktop/tablet/phone) are worth exploring as a later extension, not something to take on today.
:::

## Titling sheets on a dashboard

To show a title for a sheet within the dashboard:

1. Select the sheet inside the dashboard.
2. Open that sheet's menu (the small dropdown arrow that appears in its top-right corner when selected) and choose **Show Title**.
3. Double-click the title text to edit it directly, or use the same **Edit Title...** / **Insert** workflow from Episode 4 to add a dynamic value.

::: callout
Don't rename a dashboard sheet by double-clicking its worksheet tab at the bottom of the screen — that renames the underlying worksheet everywhere it's used, not just its dashboard title. Use the sheet's own **Show Title** / **Edit Title** controls instead.
:::

## Adding Interactivity

This is where dashboards become powerful: you can make any sheet act as a filter for others.

::: checklist

### Adding an Interactive Filter Action

- Select the sheet inside the dashboard you want to use as a filter source (e.g. `Collision Map`).
- Open that sheet's menu (the dropdown arrow in its corner, or **More Options**) and choose **Use as Filter**.
- Repeat for any other sheet that should filter the rest of the dashboard.
:::

`Use as Filter` is a menu option on the sheet itself — it generates a filter action behind the scenes (visible under **Dashboard > Actions** if you want to inspect or adjust it), rather than something you configure through a separate floating toolbar.

Now, clicking a mark on a filter-source sheet — a bar, a map point — updates the other linked sheets to show only the related data.

## Shared filters across worksheets

A filter card can also be applied beyond the single sheet it started on:

::: checklist
- On a worksheet, right-click the field on the Filters shelf.
- Choose **Apply to Worksheets**.
- Select **All Using This Data Source** to apply it everywhere that data source is used, or **Selected Worksheets...** to choose specific sheets.
:::

This is different from a dashboard filter action: a shared filter changes what data each sheet can show at all, while a filter action responds to a click and filters based on what was selected.

## Saving and Publishing to Tableau Public

Once you're satisfied with your dashboard:

::: checklist
- Go to **Server > Tableau Public > Save to Tableau Public**.
- Log in to your Tableau Public account (create one if needed).
- Name your workbook and save.
:::

::: callout
## Expected outcome
Tableau uploads your workbook and opens your default browser to the published view on Tableau Public's website. Sharing controls — including embed code, a direct link, and download settings — appear below the visualization on that page.
:::

::: caution
## Publishing is public

- Your visualization, once published, is visible to anyone on the web.
- The workbook and its underlying data **may be downloadable** by viewers, depending on your settings.
- Disabling downloads reduces but does not eliminate exposure — it is **not sufficient protection** for sensitive data.
- **Never publish sensitive, private, licensed, or restricted data** to Tableau Public. If you're working with data like that in your own work, use a licensed edition that can publish to Tableau Cloud or Tableau Server with proper access controls instead.
:::

## Accessibility

Before sharing, take a pass at accessibility:

- For each worksheet, go to **Worksheet > Accessibility** to add alt text describing what the chart shows and why it matters — this is what screen reader users will hear in place of the visual.
- On the dashboard, check each sheet's **More Options** menu for an **Accessibility** option to set dashboard-level alt text where available.
- Don't rely on color alone to convey meaning — pair color with labels, shapes, or direct annotation, since color-blind viewers and screen readers won't get the same information from color that sighted viewers do.

## Final check before sharing

Before you consider a dashboard done, view it in a browser (not just the desktop app) and check:

::: checklist
- Titles and axis units are clear and accurate.
- Filters behave as expected, and selections can be cleared.
- Tooltips display useful, correctly formatted information.
- Text and marks have adequate color contrast.
- The dashboard remains usable at a smaller browser width.
- Every filter action's target sheets update correctly when you click.
- Any public-facing title, description, or tags you set are accurate and don't reference private context.
:::

::: challenge
**Challenge: Build and Publish a Dashboard**

Create a dashboard with at least two visualizations. Enable a filter action, and publish it to your Tableau Public profile.

- What story does your dashboard tell?
- Could someone unfamiliar with the data understand what they're seeing?

::: hint
Add meaningful titles, alt text, and tooltips to help interpret your charts.
:::

::: solution
- Combine `Collisions Over Time` and `Collision Map` into one dashboard.
- Use `Collision Map` as a filter source via **Use as Filter**.
- Add worksheet alt text, a dynamic dashboard title, and test the published dashboard in a browser.
:::
:::

---

::: keypoints
- Reference only worksheets you've actually built, by their exact names, in dashboard instructions.
- Tiled layout with a fixed dashboard size is the reliable beginner default; Floating and Automatic sizing are later extensions.
- Use each sheet's own menu for **Show Title** and **Use as Filter** — don't rename dashboard titles by editing the underlying worksheet tab.
- A shared filter (**Apply to Worksheets**) and a dashboard filter action (**Use as Filter**) solve different problems.
- Tableau Public dashboards are public and may be downloadable — never publish sensitive data, and add accessibility alt text before sharing.
:::
