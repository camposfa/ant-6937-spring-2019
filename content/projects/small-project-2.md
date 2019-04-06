---
title: "Small Project 2"

---

<span style="color:red">**Due date: Apr. 18 by the end of the day (11:59:59 pm)**</span>

## Introduction

In this small project, you will think of conceptual questions to ask of one or more data sets.

**Because I think some of you disliked the ape_teeth data set from small project 1, this time I'm providing several different data sets that can be used.**

All your questions can be from one data set, or you can ask different questions of different data sets. It's up to you.

<br>

## Description of the data


#### 1. Research funding bias

Data on gender bias in research funding in the Netherlands. From van der Lee and Ellemers (2015), _PNAS_, ["Gender contributes to personal research funding success in The Netherlands"](https://www.pnas.org/content/112/40/12349).

Download: [<i class="fas fa-file-csv fa-lg"></i> research_funding.csv](/files/data/research_funding.csv)

<u>Columns</u>

- discipline: Research area discipline.
- applications_men: Total applications by men.
- applications_women: Total applications by women.
- awards_men: Total awards received by men.
- awards_women: Total awards received by women.
- success_rates_men: Success rate for men.
- success_rates_women: Success rate for women.

<br>

#### 2. Pollling data from US 2016 presidential elections

Poll results from US 2016 presidential elections. Data from <https://fivethirtyeight.com/>. Original source: <http://projects.fivethirtyeight.com/general-model/president_general_polls_2016.csv>.

Download: [<i class="fas fa-file-csv fa-lg"></i> fte_polls_2016.csv](/files/data/fte_polls_2016.csv)

<u>Columns</u>

- state: State in which poll was taken. "U.S" is for national polls.
- startdate: Poll's start date.
- enddate: Poll's end date.
- pollster: Pollster conducting the poll.
- grade: Grade assigned by fivethirtyeight to pollster.
- samplesize: Sample size.
- population: Type of population being polled. A = all adults, RV = registered voters, LV = likely voters, V = voters
- rawpoll_clinton: Percentage for Hillary Clinton.
- rawpoll_trump: Percentage for Donald Trump
- rawpoll_johnson: Percentage for Gary Johnson
- rawpoll_mcmullin: Percentage for Evan McMullin.
- adjpoll_clinton: Fivethirtyeight adjusted percentage for Hillary Clinton.
- ajdpoll_trump: Fivethirtyeight adjusted percentage for Donald Trump
- adjpoll_johnson: Fivethirtyeight adjusted percentage for Gary Johnson
- adjpoll_mcmullin: Fivethirtyeight adjusted percentage for Evan McMullin.

<br>

#### 3. Primate fruit patch visits

Characteristics of fruit-producing trees visited by several capuchin groups over a 4-year period.

Download: [<i class="fas fa-file-csv fa-lg"></i> ssr_fpv.csv](/files/data/ssr_fpv.csv)

<u>Columns</u>

 - group: Code of capuchin group that visited the tree.
 - scientific_name: Scientific name of the tree species.
 - timestamp: Date and time of the visit.
 - elevation: Elevation of tree in meters.
 - num_monkeys: Number of monkeys observed eating in the tree.
 - leaf_cover: Leaf cover score on 1--4 scale (0 = no leaves, 4 = full of leaves)
 - leaf_maturity: Leaf maturity score on 1--4 scale (0 = no mature leaves, 4 = 100% of leaves present are mature leaves)
 - fruit_cover: Fruit cover score on 1--4 scale (0 = no fruit, 4 = full of fruit)
 - fruit_maturity: Fruit maturity score on 1--4 scale (0 = no ripe fruit, 4 = 100% of fruits present are ripe)
 - flower_cover: Flower cover score on 1--4 scale (0 = no fruit, 4 = full of flowers)
 - flower_maturity: Flower maturity score on 1--4 scale (0 = no mature flowers, 4 = 100% of flowers present are mature)
 - trunk_diameter_cm: Diameter at breast height of the tree trunk.
 - fruit_avail_index: A ripe fruit "availability index" ranging from 0 (no ripe fruit) to 1 (completely full of ripe fruit). Calculated as (fruit_cover / 4) * (fruit_maturity / 4).
 - fruit_biomass_kg: Estimated biomass of available ripe fruit.
 - lon: Geographic longitude coordinate (crs = 4326)
 - lat: Geographic latitude coordinate (crs = 4326)


<br>

#### 4. Hourly temperature measurements in Kenya

Air temperature recorded hourly during 2016 by a weather station located in Amboseli national park, Kenya.

Download: [<i class="fas fa-file-csv fa-lg"></i> weather_2016.csv](/files/data/weather_2016.csv)

<u>Columns</u>

- year_of: Year
- month_of: Abbreviation of month
- date_of: Date of temperature reading
- 0: Air temperature at hour 0 (midnight)    
...
- 23: Air temperature at hour 23 (11 pm)


<br>
<hr>
<br>

## Instructions

#### Content Instructions

- Think of three (and only three!) conceptual questions about any of the data sets. Clearly state each question in your report. You might want to create different sections for your different questions.
- Using `dplyr` and/or `tidyr`, manipulate the data as necessary to get it into shape for plotting.
- Using `ggplot2`, create _at least one plot for each question_ that helps you to answer the question. For each plot, provide an explanation for why you chose the _type_ of plot (e.g. scatterplot, boxplot, bar chart, histogram, etc.), and why you believe that it is best for showing the information related to your question. 
- Answer your questions by interpreting your plots and identifying any trends that they reveal (or do not reveal).
- In total, your text related to the conceptual questions, plot design decisions, and interpretation should be in the neighborhood of 1000 words.
- In your report, 
    - **Use at least 3 different `dplyr` verbs** (e.g., `filter()`, `arrange()`, `select()`, `mutate()`, `summarise()`, `group_by()`, etc.)
    - **Use at least 1 `tidyr` verb** (e.g., `pivot_longer()`, `pivot_wider()`, or the older versions if necessary).
    - **Use at least 3 different `ggplot2` geoms.**

<br>

#### Formatting Instructions

- The project report should look similar to some of our class activities, but it should include more narrative/explanation along with the code and plots.
- Please create your report in an R markdown file called `small-project-2_XX.Rmd`, where you substitute your initials for "XX" (for example, my report would be called `small-project-2_FC.Rmd`.
- The R Markdown report should show all of the code that you used to work with the data and produce your plots.
- Put your `.html` file and the `.Rmd` file **together in one `.zip` file and submit through Blackboard.**

<br>

#### Evaluation Criteria

Projects will be graded on workflow and presentation rather than particular conclusions. _So don't fret if you ask a question that fails to turn up interesting results!_ The data are what they are.

To receive full credit, I am looking for:

- Clear, coherent questions about the data. Questions end in a question mark!
- The data manipulations should be purposeful---they should be used to get the data into shape for answering your questions and plotting.
- Each plot that you include in the report should help to answer one of your proposed questions, with a justification for _why_ you chose to make the type of plot that you made. I am not looking for a dumping ground of many preliminary or poor-quality plots that you experimented with while trying to make a good one.
- Interpretation of your plots and responses to your proposed question.