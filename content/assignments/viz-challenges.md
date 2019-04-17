---
title: Visualization Challenges
---

<br>

### Catch-up work

- **Work on Small Project 2!**
- Get caught up will any other assignments that you haven't completed. This includes:

    - 9 DataCamp chapters.
    - `msleep`
    - `pies`
    - `baboon-activities`
    - `babynames`
    - `maps`
    - `ozone`
    - `spreadsheets`
    - `tidy-data`
    - `data-manip1`

<br>

**If you're all caught up,** practice your data manipulation and plotting skills by working on the two small challenges below. I'll post solutions after class is over.

<br>
<hr>
<br>

#### 1. Sex differences in mortality over time in Western Europe

**Data:**

Source: [The Human Mortality Database](https://www.mortality.org).

- [<i class="fas fa-file-alt fa-lg"></i> England_Mx_1x1.txt](/livecode/viz-challenges/England_Mx_1x1.txt) (death rates by age and year for England and Wales)
- [<i class="fas fa-file-alt fa-lg"></i> France_Mx_1x1.txt](/livecode/viz-challenges/France_Mx_1x1.txt) (death rates by age and year for France)


<br>

**Instructions:**

1. Download the `.txt` files above.
2. Try to create something similar to this plot:

![](/livecode/viz-challenges/mortality.svg)

**Hints for data manipulation:**

1. Check to see how the columns are delimited in the text files. Each line is the same length, and each field is in the same position in every line. Use a `readr` function to read white-space-deparated columns that are formatted like this.
2. Inspect the data in the text files carefully. There are a couple of problems with the data structure that will need to be addressed when you import the files.
3. The two files can be "bound" together row-wise using the `dplyr` function `bind_rows()`. Before binding, what do you need to add to each country's data file?
4. Notice in the data how people >= 110 years old are coded, and why this is a problem. Since we want to treat age as a number, recode all such people to be 110 years old, and convert the column to a number.
5. You can create a new column with percentile bins using the `dplyr` function `ntile()`. When doinng so, create 100 bins.

**Hints for plotting:**

1. Filter out any people older than age 100 (there are some weird things going on above that age due to small sample sizes).
2. Use `geom_raster()`, which is like `geom_tile()` but is more effective at creating a "blended" effect when you have a large number of tiles.
3. Facet by two variables (what are they?) using `facet_grid()`.
4. Use a sequential color palette. I used the `viridis` palette called "magma".
    - By default, a color bar will be created. Change this to a discrete legend by adding this line to your plot: `guides(fill = guide_legend())`. Additional options can be provided to `guide_legend()` to set the number of legend rows and to position the title and labels.
    - In your `scale_fill_` function, manually set the color breaks using `breaks = <your sequence of breaks here>`.

**What interesting things does this visualization reveal about mortality patterns in these countries?**

<br>
<hr>
<br>


#### Monthly temperature anomalies in San Antonio

**Data:**

- [<i class="fas fa-file-csv fa-lg"></i> sat_weather.csv](/livecode/viz-challenges/England_Mx_1x1.txt) (Daily temperature summaries from SAT)

Source: [Global Historical Climatology Network Daily](https://www.ncdc.noaa.gov/ghcnd-data-access).

<br>

**Instructions:**

1. Download the `.csv` file above.
2. Try to create something similar to this plot:

![](/livecode/viz-challenges/sat_t_anom.svg)

**Hints for data manipulation:**

1. Some rows have `tmax` and `tmin` but are missing `tavg`, while a few rows have `tavg` but no `tmax` or `tmin`. We cannot recover `tmax` and `tmin` when they are missing, but we can approximate any missing `tavg` values by taking the average of `tmax` and `tmin` for that day. Then we need to "coalesce" the two different kinds of `tavg` measurements: use the recorded `tavg` if present, otherwise use the approximated one. There's a nice function called `coalesce()` that will accomplish this for us. Given a set of vectors, it takes the first non-missing value at each position. Use it like this: `mutate(tavg = coalesce(tavg, tavg_approx))`.
2. You will need to summarize multiple variables (by which groups?) and reshape.
3. You can use a grouped mutate to calculate the anomalies.

**Hints for plotting:**

1. Use `geom_tile()`.
2. Facet by the temperature variables using `facet_wrap()`.
3. Use a diverging color palette centered at zero. I used the `RColorBrewer` palette called "RdBu".
4. To get the diverging color scale right (centered at zero), find the largest absolute value in the new anomaly column (call it "lim"). Then use `limits = c(-lim, lim)` in your `scale_fill_` function.