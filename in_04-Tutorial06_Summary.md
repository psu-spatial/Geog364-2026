

# Summarising Data {#T5_Summarising}



## Overall :  Useful commands for looking at a dataset

There are a few commands you will use constantly when working with data.

```         
View(mpg)       # open the dataset in a spreadsheet-style viewer
glimpse(mpg)    # show the structure of the dataset
names(mpg)      # show the column names
summary(mpg)    # give a quick summary of the dataset
```

`View()` is an interactive command, so I normally run it in the **Console** rather than putting it in a report that I need to knit.


<br>

In this tutorial we will use the `pirates` dataset from the `yarrr` package as our example. If you want to follow along, make sure `library(yarrr)` is in your library code chunk, then run:


``` r
data("pirates")
```

> **Summarising vs EDA — what's the difference?**
> This tutorial is about **quality control** — checking your data arrived correctly, understanding its structure, fixing column types, and dealing with missing values. You're making sure everything is sensible before any analysis begins.
>
> EDA (Exploratory Data Analysis) comes next — that's about looking for patterns and relationships using plots and grouped summaries. The two overlap, but a useful rule of thumb is: summarising first (is my data clean?), EDA second (what's interesting?).

<br>

---

## First look at your data {#T5_FirstLook}

<br>

#### View your data — `View()` {#T5_View}

The quickest way to look at your data is to click its name in the **Environment pane**, or type this directly into the **console** (not your code chunk):


``` r
View(pirates)
```

This opens a spreadsheet-style viewer. Run this in the console rather than in a code chunk — it's an interactive command that won't work when you knit your document.

<br>

#### Check structure — `str()` and `glimpse()` {#T5_str}

`str()` (structure) is usually the first command to run on any new dataset. It shows how many rows and columns you have, each column's name, its data type, and the first few values.


``` r
str(pirates)
```

```
## 'data.frame':	1000 obs. of  17 variables:
##  $ id             : int  1 2 3 4 5 6 7 8 9 10 ...
##  $ sex            : chr  "male" "male" "male" "female" ...
##  $ age            : num  28 31 26 31 41 26 31 31 28 30 ...
##  $ height         : num  173 209 170 144 158 ...
##  $ weight         : num  70.5 105.6 77.1 58.5 58.4 ...
##  $ headband       : chr  "yes" "yes" "yes" "no" ...
##  $ college        : chr  "JSSFP" "JSSFP" "CCCC" "JSSFP" ...
##  $ tattoos        : num  9 9 10 2 9 7 9 5 12 12 ...
##  $ tchests        : num  0 11 10 0 6 19 1 13 37 69 ...
##  $ parrots        : num  0 0 1 2 4 0 7 7 2 4 ...
##  $ favorite.pirate: chr  "Jack Sparrow" "Jack Sparrow" "Jack Sparrow" "Jack Sparrow" ...
##  $ sword.type     : chr  "cutlass" "cutlass" "cutlass" "scimitar" ...
##  $ eyepatch       : num  1 0 1 1 1 1 0 1 0 1 ...
##  $ sword.time     : num  0.58 1.11 1.44 36.11 0.11 ...
##  $ beard.length   : num  16 21 19 2 0 17 1 1 1 25 ...
##  $ fav.pixar      : chr  "Monsters, Inc." "WALL-E" "Inside Out" "Inside Out" ...
##  $ grogg          : num  11 9 7 9 14 7 9 12 16 9 ...
```

`glimpse()` from the `tidyverse` gives the same information in a slightly cleaner layout:


``` r
glimpse(pirates)
```

```
## Rows: 1,000
## Columns: 17
## $ id              <int> 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16,…
## $ sex             <chr> "male", "male", "male", "female", "female", "male", "f…
## $ age             <dbl> 28, 31, 26, 31, 41, 26, 31, 31, 28, 30, 25, 20, 24, 26…
## $ height          <dbl> 173.11, 209.25, 169.95, 144.29, 157.85, 190.20, 158.05…
## $ weight          <dbl> 70.5, 105.6, 77.1, 58.5, 58.4, 85.4, 59.6, 74.5, 68.7,…
## $ headband        <chr> "yes", "yes", "yes", "no", "yes", "yes", "yes", "yes",…
## $ college         <chr> "JSSFP", "JSSFP", "CCCC", "JSSFP", "JSSFP", "CCCC", "J…
## $ tattoos         <dbl> 9, 9, 10, 2, 9, 7, 9, 5, 12, 12, 10, 14, 8, 9, 14, 8, …
## $ tchests         <dbl> 0, 11, 10, 0, 6, 19, 1, 13, 37, 69, 1, 5, 6, 12, 70, 3…
## $ parrots         <dbl> 0, 0, 1, 2, 4, 0, 7, 7, 2, 4, 3, 3, 0, 3, 0, 1, 0, 3, …
## $ favorite.pirate <chr> "Jack Sparrow", "Jack Sparrow", "Jack Sparrow", "Jack …
## $ sword.type      <chr> "cutlass", "cutlass", "cutlass", "scimitar", "cutlass"…
## $ eyepatch        <dbl> 1, 0, 1, 1, 1, 1, 0, 1, 0, 1, 1, 0, 0, 1, 1, 1, 0, 0, …
## $ sword.time      <dbl> 0.58, 1.11, 1.44, 36.11, 0.11, 0.59, 3.01, 0.06, 0.74,…
## $ beard.length    <dbl> 16, 21, 19, 2, 0, 17, 1, 1, 1, 25, 1, 27, 0, 19, 0, 1,…
## $ fav.pixar       <chr> "Monsters, Inc.", "WALL-E", "Inside Out", "Inside Out"…
## $ grogg           <dbl> 11, 9, 7, 9, 14, 7, 9, 12, 16, 9, 7, 8, 12, 7, 9, 10, …
```

Both are useful for spotting problems immediately — for example, a column of numbers that R has accidentally read in as text (`chr` instead of `num`), or a categorical column that should be a factor but isn't.

<br>

#### Check size — `nrow()`, `ncol()`, `dim()` {#T5_size}


``` r
nrow(pirates)   # number of rows
ncol(pirates)   # number of columns
dim(pirates)    # both at once: rows then columns
```

<br>

---

## Checking and fixing column types {#T5_ColTypes}

When R reads in data, it makes a guess at each column's type. It usually gets this right, but not always. Before running any analysis, it's worth checking that every column is the type you expect.

The main data types you'll encounter are:

| Type | What it means | Example |
|---|---|---|
| `num` or `dbl` | Numeric (continuous) | height, weight, temperature |
| `int` | Integer (whole numbers) | count of tattoos, age in years |
| `chr` | Character (text) | names, free-text responses |
| `factor` | Categorical with defined levels | sex, college, treatment group |
| `logi` | Logical (TRUE/FALSE) | passed/failed, yes/no |

<br>

#### Checking the type of a single column — `class()` {#T5_class}

To check one column at a time, use `class()` with the `$` operator (`datasetname$columnname`):


``` r
class(pirates$sex)
```

```
## [1] "character"
```

``` r
class(pirates$age)
```

```
## [1] "numeric"
```

``` r
class(pirates$college)
```

```
## [1] "character"
```

If a column should be a factor but shows as `chr`, or should be numeric but shows as `chr`, you need to fix it before your analysis will work correctly.

<br>

### Factors {#T5_Factors}

A **factor** is R's way of storing a categorical variable — one that takes a fixed set of values (called **levels**), like sex, treatment group, or college attended. Factors matter because:

- Many statistical functions (like `lm()`) treat factors differently from plain text — they automatically create the correct dummy variables for you
- Plots will group and order categories correctly
- R will warn you if you try to use a value that isn't one of the defined levels

If a categorical column is stored as `chr` (character/text) rather than a factor, R will often still produce output — but it may be wrong, or the output may not behave as expected.

<br>

#### Converting a column to a factor — `as.factor()` {#T5_asfactor}

Looking at `str(pirates)`, several columns are stored as `chr` (character/text) that would be better as factors for analysis: `sex`, `college`, `headband`, and `sword.type`. The `eyepatch` column is stored as `num` (0/1) but is also categorical — it should be a factor too.


``` r
pirates$sex       <- as.factor(pirates$sex)
pirates$college   <- as.factor(pirates$college)
pirates$headband  <- as.factor(pirates$headband)
pirates$sword.type <- as.factor(pirates$sword.type)
pirates$eyepatch  <- as.factor(pirates$eyepatch)
```

After converting, run `str()` again to confirm the changes:


``` r
str(pirates)
```

```
## 'data.frame':	1000 obs. of  17 variables:
##  $ id             : int  1 2 3 4 5 6 7 8 9 10 ...
##  $ sex            : Factor w/ 3 levels "female","male",..: 2 2 2 1 1 2 1 1 1 2 ...
##  $ age            : num  28 31 26 31 41 26 31 31 28 30 ...
##  $ height         : num  173 209 170 144 158 ...
##  $ weight         : num  70.5 105.6 77.1 58.5 58.4 ...
##  $ headband       : Factor w/ 2 levels "no","yes": 2 2 2 1 2 2 2 2 2 2 ...
##  $ college        : Factor w/ 2 levels "CCCC","JSSFP": 2 2 1 2 2 1 2 2 2 2 ...
##  $ tattoos        : num  9 9 10 2 9 7 9 5 12 12 ...
##  $ tchests        : num  0 11 10 0 6 19 1 13 37 69 ...
##  $ parrots        : num  0 0 1 2 4 0 7 7 2 4 ...
##  $ favorite.pirate: chr  "Jack Sparrow" "Jack Sparrow" "Jack Sparrow" "Jack Sparrow" ...
##  $ sword.type     : Factor w/ 4 levels "banana","cutlass",..: 2 2 2 4 2 2 2 2 2 2 ...
##  $ eyepatch       : Factor w/ 2 levels "0","1": 2 1 2 2 2 2 1 2 1 2 ...
##  $ sword.time     : num  0.58 1.11 1.44 36.11 0.11 ...
##  $ beard.length   : num  16 21 19 2 0 17 1 1 1 25 ...
##  $ fav.pixar      : chr  "Monsters, Inc." "WALL-E" "Inside Out" "Inside Out" ...
##  $ grogg          : num  11 9 7 9 14 7 9 12 16 9 ...
```

<br>

#### Checking factor levels — `levels()` {#T5_levels}

`levels()` shows you all the categories R knows about, in the order it will use them:


``` r
levels(pirates$sex)
```

```
## [1] "female" "male"   "other"
```

The first level is always the **reference category** in regression models — R will compare all other levels against it. By default levels are ordered alphabetically, so `female` would come before `male`.

<br>

#### Changing the reference level — `relevel()` {#T5_relevel}

If you want a different reference category (for example, you want `"male"` to be the baseline in a regression rather than `"female"`, which comes first alphabetically):


``` r
levels(pirates$sex)   # check current order first — female is the default reference
```

```
## [1] "female" "male"   "other"
```

``` r
pirates$sex <- relevel(pirates$sex, ref = "male")
levels(pirates$sex)   # male is now first
```

```
## [1] "male"   "female" "other"
```

<br>

#### Renaming factor levels — `levels()` assignment {#T5_relabel}

To rename the categories themselves (for example, to capitalise labels for a plot):


``` r
levels(pirates$sex)                                    # check current labels and order first
```

```
## [1] "male"   "female" "other"
```

``` r
levels(pirates$sex) <- c("Male", "Female", "Other")   # rename in the same order
levels(pirates$sex)
```

```
## [1] "Male"   "Female" "Other"
```

> **Warning:** The new names must be listed in the **same order** as the existing levels. Always run `levels()` first to check the current order before renaming.

<br>

#### Ordered factors {#T5_ordered}

Some categorical variables have a natural order — for example, education level (low, medium, high) or survey responses (never, sometimes, always). A plain `factor` treats all levels as equal; an **ordered factor** tells R that the categories have a meaningful sequence.

The `pirates` dataset doesn't have a natural ordinal column, but we can create one by grouping grogg consumption into low, medium, and high:


``` r
# Create an ordinal grogg consumption variable
pirates$grogg.level <- cut(pirates$grogg, 
                           breaks = c(0, 7, 12, Inf),
                           labels = c("low", "medium", "high"))
```

Here's the actual code you need to create an ordered factor where you control the order.


``` r
pirates$grogg.level <- factor(pirates$grogg.level,
                              levels = c("low", "medium", "high"),
                              ordered = TRUE)

levels(pirates$grogg.level)
```

```
## [1] "low"    "medium" "high"
```

``` r
is.ordered(pirates$grogg.level)
```

```
## [1] TRUE
```

Ordered factors matter in regression — R fits them differently from unordered factors (using polynomial contrasts rather than dummy variables), so only use `ordered = TRUE` when the order genuinely reflects a meaningful progression.

<br>

---

## Dealing with missing data {#T5_Missing}

Missing values in R are stored as `NA`. It's important to understand where your missing data is and deal with it *before* running any analysis, because most statistical functions will either return `NA` or silently drop rows if you don't.

<br>

#### Checking for missing values {#T5_checkNA}

To count missing values in every column at once:


``` r
colSums(is.na(pirates))
```

```
##              id             sex             age          height          weight 
##               0               0               0               0               0 
##        headband         college         tattoos         tchests         parrots 
##               0               0               0               0               0 
## favorite.pirate      sword.type        eyepatch      sword.time    beard.length 
##               0               0               0               0               0 
##       fav.pixar           grogg     grogg.level 
##               0               0               2
```

`skim()` (covered in the next section) also shows missing value counts automatically, which is one reason it's useful as a first QC step.

<br>

#### Ignoring NAs in calculations — `na.rm = TRUE` {#T5_naInCalcs}

Most summary functions have a built-in argument to skip NAs rather than returning `NA`:


``` r
mean(pirates$age, na.rm = TRUE)
```

`na.rm = TRUE` works in `mean()`, `median()`, `sd()`, `sum()`, `min()`, `max()`, and most other summary functions.

<br>

#### Removing rows where a specific column is NA — `filter()` {#T5_naFilter}

If you want to remove rows where a particular column is missing, use `filter()`. This is the most precise approach:


``` r
pirates_clean <- pirates |>
  filter(!is.na(age))
```

`!is.na(age)` means *"keep rows where age is NOT missing"*. You can chain multiple columns:


``` r
pirates_clean <- pirates |>
  filter(!is.na(age),
         !is.na(height))
```

<br>

#### Removing all incomplete rows — `na.omit()` {#T5_naomit}

To remove any row that has an NA in *any* column:


``` r
pirates_clean <- na.omit(pirates)
```

> **Note:** `na.omit()` can remove a lot of rows if your dataset has many columns. Always check how many rows you lose:

> 
> ``` r
> nrow(pirates)        # before
> nrow(pirates_clean)  # after
> ```
> If you've lost more than you expected, use `filter(!is.na(columnname))` instead to target only the columns that matter for your analysis.

Once you've cleaned your data, USE THE CLEAN VERSION IN YOUR ANALYSIS

<br>

---

## Summarising your data {#T5_Summaries}

Once you're happy that column types are correct and missing data is handled, you're ready to summarise.

<br>

### The whole dataset {#T5_WholeSummary}

<br>

#### `summary()` {#T5_summary}

`summary()` gives a statistical overview of every column — min, max, mean, and quartiles for numeric columns, and level counts for factors.


``` r
summary(pirates)
```

> **Tip:** `summary()` output can wrap awkwardly in a knitted document. Run it in the **console** for easier reading.

<br>

#### `skim()` {#T5_skim}

`skim()` from the `skimr` package gives a more detailed summary, including missing value counts and a small histogram for each numeric column. It's the most useful single command for a thorough QC check.


``` r
skim(pirates)
```

Like `summary()`, `skim()` is often easier to read in the console than in a knitted document.

<br>

### A single column {#T5_SingleCol}

Use `$` to refer to one column: `datasetname$columnname`.


``` r
mean(pirates$age)      # mean
median(pirates$age)    # median
sd(pirates$age)        # standard deviation
range(pirates$age)     # minimum and maximum
sum(pirates$age)       # total
```


## Frequency tables {#T5_Tables}

For categorical columns, `table()` counts how many observations fall into each level:


``` r
table(pirates$sex)
```

```
## 
##   Male Female  Other 
##    490    464     46
```

For proportions instead of counts:


``` r
proportions(table(pirates$sex))
```

```
## 
##   Male Female  Other 
##  0.490  0.464  0.046
```

<br>

---

## Troubleshooting {#T5_Troubleshooting}

<br>

**Got `NA` as your answer?**
Your column probably contains missing values. Add `na.rm = TRUE`:

``` r
mean(pirates$age, na.rm = TRUE)
```

<br>

**`Error: object 'columnname' not found`**
You probably forgot the `$`. R doesn't know which dataset to look in for a bare column name. Use `datasetname$columnname`.

<br>

**Factor conversion seems to have done nothing**
Make sure you saved the result back to the column with `<-`:

``` r
pirates$sex <- as.factor(pirates$sex)   # correct — saves the result
as.factor(pirates$sex)                  # wrong — converts but doesn't save
```

<br>

**`levels()` returns `NULL`**
The column isn't a factor yet. Convert it with `as.factor()` first, then check levels.

<br>

**Relabelling levels changed the wrong categories**
`levels()` assignment replaces labels in the current level order, not alphabetically. Always run `levels(columnname)` first to check the order before reassigning.

<br>

**Lost more rows than expected after `na.omit()`**
`na.omit()` removes any row with *any* NA across all columns. Use `filter(!is.na(columnname))` to target only the columns you care about.

<br>

**`summary()` or `skim()` output looks broken in my knitted document**
Run these in the console — they're wide commands that don't always render neatly in knitted HTML.
