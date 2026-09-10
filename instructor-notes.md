---
title: 'Instructor Notes'
---

## Version and application

This lesson was updated and validated against **Tableau Desktop: Public Edition 2026.2.x**. If you're teaching from a different version:

- Menu paths for calculated fields, splits, map layers, and filter cards have moved between Tableau versions in the past (for example, the map background style menu moved from `Map > Background Maps` to `Map > Map Layers > Background > Style`). Spot-check the menu paths in each episode against your installed version before teaching.
- This lesson is written for the **installed desktop application**, not the web-based authoring tool at public.tableau.com. If a learner opens web authoring instead of the desktop app, some menu paths and shortcuts in this lesson won't match what they see.

## Dataset status

The workshop dataset (legacy LAPD Traffic Collision data) has stopped receiving updates — LAPD migrated to a new records management system and this dataset is retained for historical reference only. That makes it stable for teaching (everyone gets the same numbers), but be ready for a learner to ask why the data doesn't include recent years.

**Outstanding follow-up:** a fixed, dated CSV snapshot for this workshop has not yet been created (see `learners/setup.md`). Until it exists, learners download directly from the live source, which could in principle change between sessions. Creating and hosting a dated snapshot removes that risk — flag this to whoever preps the next offering.

## Likely trouble spots

- **Coordinate splitting (Episode 3):** `Custom Split` on `Location` can behave differently if a learner's export has extra whitespace or a different delimiter than a plain comma. Check the split preview before moving on.
- **Aggregation confusion (Episode 2–3):** learners will want to use `COUNT([DR Number])` out of habit. Walk through the grain check exercise before introducing `COUNTD` — the distinction won't stick if it's just asserted.
- **Map rendering as a single dot:** almost always means `DR Number` (or another record-level dimension) is missing from Detail on the Marks card. This is the single most common map troubleshooting question.
- **Zero-length "phantom" bars on the hourly bar chart:** if a filter has been applied, an hour with zero collisions in the current selection may simply not render a bar at all rather than showing a bar at height zero. Worth calling out live if it comes up.

## Desktop vs. web authoring

If a learner is working from a personal Chromebook or otherwise can't install the desktop app, they may be tempted to use Tableau Public's web authoring tool instead. It's a different (though related) product with its own menu structure; this lesson does not cover it. Point such learners to institutional lab machines if available, or flag it as an unsupported path for this particular workshop.
