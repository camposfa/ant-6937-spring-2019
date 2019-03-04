---
title: "Data Import"
---

## Read

<br>

#### Organizing Data

- **["Tidy Data"](http://vita.had.co.nz/papers/tidy-data.pdf) by Hadley Wickham.**  
    - Don't pay much attention to any R code you encounter, as most of it has now been superseded by newer tidyverse functions.  
    - This was Wickham's early "tidy tools" manifesto; it provided guiding principles and a framework for developing the tidyverse.
- **Peruse the website ["Data Organization in Spreadsheets"](https://kbroman.org/dataorg/)**, much of which has been written up in a journal article:  
    Broman KW, Woo KH (2018) Data organization in spreadsheets. _The American Statistician_ 78:2–10. [PDF ( <i class="far fa-file-pdf"></i> 3.9 MB)](../../files/Broman - 2018 - Data Organization in Spreadsheets.pdf)

<br>

#### Importing Data

- **[R4DS, Ch. 10: Tibbles](https://r4ds.had.co.nz/tibbles.html) (short)**
- **[R4DS, Ch. 11.2: Data Import, "Getting started"](https://r4ds.had.co.nz/data-import.html#getting-started)**  
    - I suggest working through the exercises to help you understand the code.


<br><hr><br>

## Supplemental Reading

**Do you need to read messy files?** I suggeset reading the remainder of [R4DS, Ch. 11](https://r4ds.had.co.nz/data-import.html). In particular:

- [Section 11.3, "Parsing a Vector"](https://r4ds.had.co.nz/data-import.html#parsing-a-vector) decribes a variety of functions provided by the `readr` package to analyze and interpret different kinds of input and figure out what kind of value it's supposed to be. For example, understanding that the value represents a number when it's formatted as `$123,456,789`, or that the value represents a date when it's formatted as `oct. 14, 1979` or `1 enero 2015`.
- [Section 11.4, "Parsing a file"](https://r4ds.had.co.nz/data-import.html#parsing-a-file) describes strategies for guessing column types during import, diagnosing problems, and overriding the defaults when the guesses fail.