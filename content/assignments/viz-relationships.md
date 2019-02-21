---
title: Visualizing Relationships and Change Over Time
---

### Complete in Class and Submit

**Baby Names**

Instructions: Download the R Markdown file below, insert your code where indicated, and **email me your knitted `.html` output**. No need to send the `.Rmd` file!

To complete this assignment, you must install the `babynames` package:

```
install.packages("babynames")
```

- [<i class="fab fa-markdown fa-sm"></i> babynames.Rmd](/livecode/viz-relationships/babynames.Rmd)
- [<i class="fas fa-code fa-sm"></i> babynames-solutions.html](/livecode/viz-relationships/babynames-solutions.html) (for reference---finished plots with no code!)

<br>

### For Reference Only _(nothing to turn in!)_

**Katrina**

Instructions: Just look at it! And use it as a guide if you want to create maps.

To make the maps, you will need to install the packages `rnaturalearth` and `rgeos`.

```
install.pacakges("rnaturalearth")
install.pacakges("rgeos")
```

- [<i class="fas fa-code fa-sm"></i> katrina.html](/livecode/viz-relationships/katrina.html)

**Pay Gaps**

Instructions: Reminder of how we arrived at our dumbbell plot in class.

- [<i class="fas fa-code fa-sm"></i> pay-gaps.html](/livecode/viz-relationships/pay-gaps.html)


<br>
<hr>
<br>

### Between now and class on Feb. 28

- **Work on Small Project 1!**
- Get caught up will any other assignments that you haven't completed. This includes:

    - 9 DataCamp chapters.
    - `msleep`
    - `pies`
    - `baboon-activities`
    - `babynames`


<br>
<hr>
<br>

### For the keeners _(optional)_

Using what you learned in the `pay-gaps` activity, try to visualize the earnings data as a slopegraph:

![](/livecode/viz-relationships/pay-gaps-slopegraph.svg)

Notes:

- Only 6 schools are shown: Emory, U.Penn, Yale, Berkeley, Notre Dame, and Stanford.
- There are labels on both sides that do not obscure the points (hint: plot left and right labels separately, and use `glue()` to pad the label with spaces on the appropriate side).