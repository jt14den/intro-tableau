---
title: 'Reference'
---

## Glossary

Aggregation
: How Tableau summarizes multiple values of a measure into one, such as `SUM`, `AVG`, `COUNT`, or `COUNTD` (count distinct). Aggregation is independent of a field's data type or role — it's the calculation applied when combining rows.

Calculated Field
: A new field created in Tableau using a formula based on existing data, marked with a small `=` icon in the Data pane. Calculated fields allow you to perform computations, manipulate strings, apply logic, and derive new insights that aren't directly present in your original dataset. The `=` icon indicates the field was calculated or copied — it does not by itself indicate a data type or aggregation.

Card
: A container in the Tableau interface that holds related controls — for example, the Marks card (controls how marks are drawn) or a filter card (the interactive control a viewer uses to change a filter's selected values).

Continuous
: In Tableau, a way of displaying a field so it forms an unbroken axis of values, typically for numbers or dates. Continuous fields are shown as **green** pills and usually create an axis in a visualization. Both dimensions and measures can be continuous — continuous is a display property, not a field role.

Dashboard
: A canvas in Tableau where you combine multiple worksheets and other visual elements into a single interactive view. Dashboards allow users to compare different perspectives of data and apply shared filters or filter actions across multiple charts.

Data Type
: The kind of value a field holds — string, number, date, Boolean, spatial, and so on — shown by a small icon next to the field name. Data type is independent of field role (dimension/measure) and of discrete/continuous display.

Dimension
: In Tableau, a field role for qualitative data used to categorize, segment, and reveal detail — names, IDs, geographic data, and so forth. Dimensions are commonly discrete (blue) but can also be set to continuous, for example a date dimension shown as a continuous timeline.

Discrete
: In Tableau, a way of displaying a field so it produces distinct, separate values or categories. Discrete fields are shown as **blue** pills and usually create headers in a visualization. Both dimensions and measures can be discrete.

Exploratory Data Analysis (EDA)
: An iterative process of analyzing data sets to summarize their main characteristics, often using visual methods. EDA helps you understand your data, detect outliers, discover patterns, and formulate hypotheses.

Filter Action
: A dashboard-level interaction, created via **Use as Filter** on a sheet (or **Dashboard > Actions**), where selecting a mark on one sheet filters the data shown on other sheets in the dashboard.

Filter Card
: The interactive control Tableau displays in a view when a filter's **Show Filter Card** option is enabled, letting a viewer change which values are included. Filter cards have several display modes, including Single Value (List), Single Value (Dropdown), Multiple Values (List), and Multiple Values (Dropdown).

Mark
: A single visual element in a Tableau view representing one or more records — a bar, line segment, circle, map point, and so on. The Marks card controls how marks are drawn and lets you assign fields to properties like Color, Size, Label, Detail, and Tooltip.

Measure
: In Tableau, a field role for quantitative data meant to be aggregated — sums, averages, counts, and so forth. Measures are commonly continuous (green) but can be set to discrete, for example when you want one bar per exact value rather than a single aggregated number.

Pages Shelf
: A shelf in Tableau that breaks a view into a sequence of pages (frames) based on the individual values of a field placed on it — for example, one page per year. Each page shows that value's own data; the Pages shelf does not by itself accumulate or total values across pages. A genuine running total requires a separate table calculation.

Pill
: The small rounded box representing a field once it's placed on a shelf or card. A pill's color (blue or discrete, green or continuous) reflects the discrete/continuous display setting, not the field's data type or role.

Shelf
: A drop target in the Tableau interface — Rows, Columns, Filters, Pages, and so on — where you place pills to build a view.

Tableau Desktop: Public Edition
: The free, installed edition of Tableau Desktop used in this workshop. It can save workbooks locally and publish them to Tableau Public, supports a limited set of data source types, is capped at 15 million rows, and is not licensed for commercial use.

Worksheet
: An individual authoring sheet in a Tableau workbook where a single chart or view is built, as distinct from a dashboard (which combines multiple worksheets).

## References

Official Tableau and source-data documentation consulted while validating this lesson for Tableau Desktop: Public Edition 2026.2.x:

- [Tableau releases](https://www.tableau.com/support/releases)
- [Tableau for Students](https://www.tableau.com/academic/students)
- [Edition comparison](https://help.tableau.com/current/pro/desktop/en-us/desktop_comparison.htm)
- [Saving and publishing to Tableau Public](https://help.tableau.com/current/pro/desktop/en-us/publish_workbooks_tableaupublic.htm)
- [Fields in the Data pane](https://help.tableau.com/current/pro/desktop/en-us/datafields_understanddatawindow.htm)
- [Dimensions, measures, blue, and green](https://help.tableau.com/current/pro/desktop/en-us/datafields_typesandroles.htm)
- [Show Me](https://help.tableau.com/current/pro/desktop/en-us/buildauto_showme.htm)
- [Calculated fields](https://help.tableau.com/current/pro/desktop/en-us/calculations_calculatedfields_formulas.htm)
- [Bins](https://help.tableau.com/current/pro/desktop/en-us/calculations_bins.htm)
- [Continuous dates](https://help.tableau.com/current/pro/desktop/en-us/dates_continuous.htm)
- [Edit axes](https://help.tableau.com/current/pro/desktop/en-us/formatting_editaxes.htm)
- [Split fields](https://help.tableau.com/current/pro/desktop/en-us/split.htm)
- [Point maps](https://help.tableau.com/current/pro/desktop/en-us/maps_howto_symbol.htm)
- [Map appearance](https://help.tableau.com/current/pro/desktop/en-us/maps_options.htm)
- [Map controls](https://help.tableau.com/current/pro/desktop/en-us/maps_explore.htm)
- [Shelves and Pages](https://help.tableau.com/current/pro/desktop/en-us/buildmanual_shelves.htm)
- [Filters](https://help.tableau.com/current/pro/desktop/en-us/filtering.htm)
- [Applying filters across worksheets](https://help.tableau.com/current/pro/desktop/en-us/filtering_global.htm)
- [Dashboards](https://help.tableau.com/current/pro/desktop/en-us/dashboards_create.htm)
- [Filter actions](https://help.tableau.com/current/pro/desktop/en-us/actions_filter.htm)
- [Titles](https://help.tableau.com/current/pro/desktop/en-us/formatting_specific_titlecaption.htm)
- [Accessibility](https://help.tableau.com/current/pro/desktop/en-us/accessibility_create_view.htm)
- [Historical LAPD collision dataset notice](https://catalog.data.gov/dataset/traffic-collision-data-from-2010-to-present)
- [Current LAPD Divisions page](https://geohub.lacity.org/datasets/lapd-divisions/about)
