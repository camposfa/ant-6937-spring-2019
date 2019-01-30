---
title: "In-class Activity: Visualization Basics"
author: ""
date: 2019-01-31
output: html_document
---



## Mammal sleep data

We will be working with the `msleep` data set that is provided with ggplot2. The data set contains information about the sleep habits of 83 mammals. Enter `?msleep` on the R command line to learn more about the dataset.

Let's say we want to show a few rows of the `msleep` data in the report. You can use the base R function `head()` to see the first 5 rows of data:


```r
head(msleep)
```

```
## # A tibble: 6 x 11
##   name  genus vore  order conservation sleep_total sleep_rem sleep_cycle
##   <chr> <chr> <chr> <chr> <chr>              <dbl>     <dbl>       <dbl>
## 1 Chee… Acin… carni Carn… lc                  12.1      NA        NA    
## 2 Owl … Aotus omni  Prim… <NA>                17         1.8      NA    
## 3 Moun… Aplo… herbi Rode… nt                  14.4       2.4      NA    
## 4 Grea… Blar… omni  Sori… lc                  14.9       2.3       0.133
## 5 Cow   Bos   herbi Arti… domesticated         4         0.7       0.667
## 6 Thre… Brad… herbi Pilo… <NA>                14.4       2.2       0.767
## # … with 3 more variables: awake <dbl>, brainwt <dbl>, bodywt <dbl>
```

But that's sort of ugly, and the output is cut off. Now try wrap this same command in the `knitr` function `kable()` to create a nice-looking table.


```r
# your R code goes here
```


#### **Problem 1:** 

Create a scatterplot of total time awake vs. body weight, colored by "vore" (carnivore, herbivore, etc.). What perceptual problems does this figure have, and what change could you make to show the data more effectively? What specifically causes these problems?


```r
# your R code goes here
```

*Problem 1 answer goes here.*

<hr>

#### **Problem 2:** 

Create a scatterplot of body weight vs. brain weight, again colored by "vore." When you plot body weight and/or brain weight, consider whether a linear scale or a logarithmic scale seems more appropriate, and explain your reasoning in 1-2 sentences.

**HINT:** Use the functions `scale_x_log10()` and `scale_y_log10()` to change the scales.


```r
# your R code goes here
```

*Problem 2 answer goes here.*

<hr>

#### **Problem 3:** 

Create the same plot of body weight vs. brain weight, colored by "vore," but this time label the points using the name of the animal.

**HINT:** Use the function `geom_text()` and be sure to supply it with the proper aesthetic (type `?geom_text()` and see the bolded entries under "Aesthetics" in the help file). 

What perceptual problems does this figure have?


```r
# your R code goes here
```

*Problem 3 answer goes here.* 

<hr>

#### **Problem 4:** 

This was all an elaborate setup to introduce you to the `ggrepel` package, which is one example of the many helpful "extensions" that people have created for `ggplot2`. Install this package in the usual way: 


```r
install.packages("ggrepel")
```

Now, modify the same plot of body weight vs. brain weight, colored by "vore" and labeled with the name of the animal. But this time, instead of using `geom_text()`, use the `geom_text_repel()` function provided by this packages. What has changed in your figure, and how does the change improve the interpretability of the data?


```r
library(ggrepel)

# your R code goes here
```

*Problem 4 answer goes here.* 

<hr>

#### **Problem 5:** 

Add a linear regression line to the plot using the function `geom_smooth()`.

**Hint:** A regresion line can be added with the function `geom_smooth(method = "lm")` ("lm" stands for "linear model").

Play around with the relative position of the smoothed line by putting it above or below the other geoms. Try also to use `se = FALSE` to see the line without a confidence region around the smooth. What do you think is the best place to show this line and why? 

How does this simple addition changed the figure's interpretability? Can you find any interesting "stories" in the data that have been revealed?



```r
# your R code goes here
```

*Problem 5 answer goes here.* 
