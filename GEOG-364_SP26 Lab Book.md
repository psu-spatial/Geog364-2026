---
title: "GEOG364 Lab Book 2026"
author: "Dr Helen Greatrex"
date: "2026-09-16"
site: bookdown::bookdown_site
documentclass: book
bibliography: [book.bib, packages.bib]
url: https://psu-spatial.github.io/Geog364-2026/
# cover-image: path to the social sharing image like images/cover.jpg
description: |
  This is the R-based lab book for Penn State GEOG-364 on spatial analysis. 
biblio-style: apalike
csl: chicago-fullnote-bibliography.csl
---

# cover-image: path to the social sharing image like images/cover.jpg

Placeholder


## Useful Links {#Home_UsefulLinks .unnumbered}
## How to use this website {#Home_howtouse .unnumbered}

<!--chapter:end:index.Rmd-->


# Course FAQ {#FAQ .unnumbered}

Placeholder


## What files should I submit? {#FAQ-1 .unnumbered}
## My report won't knit! {#FAQ-2 .unnumbered}
## How am I graded? {#FAQ-3 .unnumbered}
## I'm late! What's the late policy? {#FAQ-4 .unnumbered}
#### [**I never give late penalties for technical issues that we are working on together.**]{.underline} {.unnumbered}
#### [**If the assignment is still open, you are welcome to submit to it, but there is a sliding scale if you are more than 24hrs late.**]{.underline} {.unnumbered}
#### [**In general, I prefer you submit late than not at all.**]{.underline} {.unnumbered}
#### [**BUT! Submitting later than 10 days late is a risk.**]{.underline} {.unnumbered}
## Can I work with friends? What counts as cheating? {#FAQ-5 .unnumbered}
## How can I use chatGPT safely? {#FAQ-6 .unnumbered}
### [**What would Sam do?**]{.underline} {.unnumbered}
### [**Example conversation**]{.underline} {.unnumbered}

<!--chapter:end:in_01-CourseFAQ.Rmd-->


# HELP! {#Help .unnumbered}

Placeholder


## My report won't knit! {#Help-Noknit .unnumbered}

<!--chapter:end:in_01-HELP.Rmd-->


# What are R and R-Studio? {#WhatIsR .unnumbered}

Placeholder


## 1. What is R? {#WhatisRitself .unnumbered}
#### **R IS A LANGUAGE SPOKEN BY YOUR COMPUTER** {.unnumbered}
## 2. What is R-Studio/POSIT? {#WhatisRstudio .unnumbered}
#### **R-STUDIO/POSIT is a Software Application like Word, Chrome or Spotify** {.unnumbered}
## 3. What is R-Markdown? {#WhatisMarkdown .unnumbered}
#### Markdown is a way of writing documents with computer code embedded into them. {.unnumbered}
#### R-Markdown is a markdown file that uses R code {.unnumbered}
### Some examples? {.unnumbered}

<!--chapter:end:in_01-WhatIsR.Rmd-->


# Installing R/R-Studio {#Setup_Desktop .unnumbered}

Placeholder


### Video instructions {#Setup_DesktopVideo .unnumbered}
## Written Instructions

<!--chapter:end:in_03-Setup1_desktop.Rmd-->


# Updating R/R-Studio {#Setup_UpdateDesktop .unnumbered}

Placeholder


## "Why update R and R-Studio? I took a course using them last semester" {#Setup_WhyUpdate .unnumbered}
## How to update? {#Setup_UpdateHow .unnumbered}
### Then update your packages.

<!--chapter:end:in_03-Setup2_updatedesktop.Rmd-->


# Posit Cloud Online {#Setup_Online .unnumbered}

Placeholder


## Doing your labs online - Posit/R-Studio Cloud Website {#PositCloud .unnumbered}
#### [EVERYONE]{.underline} SHOULD SIGN UP FOR AN ACCOUNT HERE: <https://posit.cloud/>
### What if I run out of free time?

<!--chapter:end:in_03-Setup3_RCloud.Rmd-->


# (PART\*) [.]{style="color: white;"} {.unnumbered}

Placeholder


## LAB AIM {.unnumbered}
## LAB SET-UP (Important!) {.unnumbered}
### STEP 1: Install/update R and R-Studio {.unnumbered}
### STEP 2: Creating a project.. {#HW2_Step2 .unnumbered}
#### QUICK CHECK  {.unnumbered}
### STEP 3: Install Packages using the app store.. {.unnumbered}
### STEP 4: Download your lab report {.unnumbered}
### STEP 5: Initial questions {HW2_Step5 .unnumbered}
### STEP 6: R-Coding Questions {.unnumbered}
### STEP 7: Loading the Penguins Data {.unnumbered}
### STEP 8: Penguin analysis {.unnumbered}
## WHAT TO SUBMIT {.unnumbered}
### If you are using your own computer {.unnumbered}
### If you are using Posit Cloud online {.unnumbered}
## CHECK YOUR GRADE! {#CheckGradeL1 .unnumbered}
### RUBRIC {.unnumbered}

<!--chapter:end:in_02-Homework2.Rmd-->


# Homework 3 {#Lab_3 .unnumbered}

Placeholder


### Aim {.unnumbered}
### Need help?
## PART 1: LAB SET-UP (Important!) {.unnumbered}
### STEP 1: Create your project for homework 3 {.unnumbered}
### STEP 2: Create your lab report structure & YAML code {.unnumbered}
### STEP 3: Change the theme {.unnumbered}
### STEP 4: NEW (ish) Adjust your knit options {.unnumbered}
### STEP 5: Tidy up {.unnumbered}
### STEP 6: Finally.. sort out libraries {.unnumbered}
### STEP 7: Check progress {.unnumbered}
## PART 2: IN-CLASS WORK AND TAKE-HOME WORK {.unnumbered}
### STEP 8: Reading in data {.unnumbered}
### STEP 9: Understand where the data has come from {.unnumbered}
### STEP 10: Basic stats {.unnumbered}
### STEP 11: Make the data spatial {.unnumbered}
## WHAT TO SUBMIT {.unnumbered}
### If you are using your own computer {.unnumbered}
### If you are using Posit Cloud online {.unnumbered}
## CHECK YOUR GRADE! {#CheckGradeL1 .unnumbered}
### RUBRIC {.unnumbered}

<!--chapter:end:in_02-Homework3.Rmd-->



# Project 1 {#Lab_3 .unnumbered}

### Aim {.unnumbered}

Welcome to Project-1. This is worth 100 points! You can drop your lowest score out of the three projects.

YOU HAVE TWO WEEKS! The maximum time it should take is about 4-6 hrs of your time, plus both lab times.

The aim of this lab is to showcase your spatial analysis. <br>

### Need help?

REMEMBER THAT EVERY TIME YOU RE-OPEN R-STUDIO YOU NEED TO RE-RUN **ALL** YOUR CODE CHUNKS. The easiest way to do this is to press the "Run All" button, in the "Run" menu at the top right of your screen

<br>

<br>

------------------------------------------------------------------------

## PART 1: LAB SET-UP (Important!) {.unnumbered}

### STEP 1: Create your R-project for Project-1 {.unnumbered}

- **[1A]** Make a project for Project-1 (tutorial here) [Projects](#T1_Projects)

- **[1B]** Open your Project-1 R-project in R-Studio (see screenshot below).

<div class="figure">
<img src="./index_images/im_T1_Projectcheck.png" alt="Yours should look like this but say the name of your Project-1 project" width="100%" />
<p class="caption">(\#fig:L3-Projectcheck)Yours should look like this but say the name of your Project-1 project</p>
</div>

<br>

------------------------------------------------------------------------

### STEP 2: Create your lab report structure & YAML code {.unnumbered}

- **[2A]** Make a new RMarkdown Report ([Tutorial here](#T31_NewMarkdown)) <br>

- **[2B]** As we discussed last week, your YAML code at the top of your script tells R how to make the final report. It lives between the --- lines. CAREFULLY replace the YAML code with this code (remember to only have one set of ---) and press knit.


``` r
---
title: "GEOG-364 - Project-1"
author: "CHANGE TO YOUR E-MAIL ID"
date: "`r Sys.Date()`"
output:
  html_document:
    toc: true
    toc_float: yes
    number_sections: yes
    theme: journal
    df_print: paged
---
```

It should look like this.

<div class="figure">
<img src="./index_images/L3B_YAMLcode.png" alt="Remember the ---! This is easier in source mode" width="100%" />
<p class="caption">(\#fig:L3-YAML)Remember the ---! This is easier in source mode</p>
</div>

<br>

------------------------------------------------------------------------

### STEP 3: Change the theme {.unnumbered}

There are many easy themes you can select to change the look of your report.

- **[3A]** In your YAML code, try changing the theme line to one of these, then press knit to see how it looks (some don't work in some versions of R). YOU DON'T NEED THE QUOTES.

- “bootstrap”, “cerulean”, “cosmo”, “darkly”, “flatly”, “journal”, “lumen”, “paper”, “readable”, “sandstone”, “simplex”, “spacelab”, “united”, “yeti”

- Choose a theme of your choice.

<br>

### STEP 4: Adjust your knit options {.unnumbered}

When you press knit when you have packages, a load of library loading text will appear. This makes it hard to find your answers and makes your labs less professional. Although this was addressed in earlier labs, here's how to fix this issue.

- **[4A]** Look at the first code chunk below the YAML code. The `opts_chunk$set()` command allows us to set general knit options for the entire report.

```         
   knitr::opts_chunk$set(echo = TRUE)
```

- Add in two more options, warning=FALSE and message=FALSE.

```         
   knitr::opts_chunk$set(echo = TRUE, warning=FALSE, message=FALSE)
```

- When you press knit for now, nothing should happen (but no errors. )

<br>

### STEP 5: Tidy up {.unnumbered}

- **[5A]** Delete all "the friendly welcome text", below the knitr::opts_chunk so you have a nice clean report:

<img src="./index_images/im_L2_SetupReport.png" alt="" width="100%" style="display: block; margin: auto;" />

<br>

### STEP 6: Finally.. sort out libraries {.unnumbered}

It's good practice to have a single code chunk near the top of the script containing all your library commands. This is to stop duplicated code and to make it easy to see what you are loading before running your labs.

- **[6A]** Add a new code chunk under the opts one, and add the code inside it to load the packages.


``` r
library(tidyverse) # Lots of data processing commands
library(knitr)     # Helps make pretty output files
library(ggplot2)   # Output plots
library(sf)        # Spatial commands
library(tmap)      # Mapping commands
library(readxl)    # Read from excel files
```

- **[6B]** Then press save or try to knit. If any packages are missing you will see

  - EITHER a little yellow bar at the top of the screen asking if you want to install the libraries. Say yes, wait until the libraries are installed and try again. <br>
  - OR an error saying that it can't find that library (it might also be a spelling mistake if you are sure it's installed). In this case, you have to go to the app store and download it (Packages/Install). <br>\

<br><br>

### STEP 7: Check progress {.unnumbered}

- OK - so by now, you should be running the project for Project-1, you have created your lab report, the YAML code works and your libraries work. If not, STOP, go back and redo the tutorials or talk to Dr G/Samrin

<br><br>

------------------------------------------------------------------------

## PART 2: IN-CLASS WORK  {.unnumbered}

## PART 3: MAIN PROJECT {.unnumbered}

In this lab, you will work with wildfire occurrence data from Santa Cruz County, California. You will start with an Excel spreadsheet containing fire locations and attributes, convert it to spatial `sf` data, explore the spatial pattern of fires, and aggregate the fire locations to census tracts.

### STEP 8: Reading in data {.unnumbered}

In lab 1, we used data that was built into R. This week we will read in data from files.

- **[8A]** Go to the canvas assignment page. Download all the datasets for the lab AND PUT THEM IN THE Project-1 PROJECT FOLDER ON YOUR COMPUTER.

- **[8B]** In the TEXT part of the report, below the library code chunk, make a new heading 1, text header called "In-Class work".

- **[8C]** Below that, make a new code chunk. Use the read_excel() command to load the "Lab03_house.xlsx" data into your report and assign it it to a variable called House ([Tutorial 4 - Read Excel](#T4_load_excel)).

<br><br>

### STEP 9: Understand where the data has come from {.unnumbered}

IMPORTANT. Imagine that next month, your friend is moving to Sindian Dist., in New Taipei City, Taiwan. They want to buy a house and have asked you to figure out what most impacts house price.

YOU ARE WRITING THIS REPORT FOR THEM!

- **[9A]** You have been given a specific dataset to help answer your friend's question. Read more about the data here:<https://archive.ics.uci.edu/ml/datasets/Real+estate+valuation+data+set>.

<br>

- **[9B]** In your report, describe the data, including the object of analysis, population and variables. Now critique it! What aspects of this data are useful for your friend or not useful.

<br><br>

### STEP 10: Basic stats {.unnumbered}

Now use R-Commands that you learned in so far tutorials to explore the summary statistics and distribution of the dataset.

**[Step 10A]:** Calculate the mean distance to the MRT and report your answer in the text with units!. (hint summary command or mean command)

<br>

**[Step 10B]:** Make a professional looking histogram of the price data with units! [Tutorial - Histograms](#T7_Histograms)

<br>

**[Step 10C]:** Assume your sample is representative of the underlying population. What is the 90% confidence interval on the TRUE mean price? [hint t.test](#Ttest)

<br><br>

### STEP 11: Make the data spatial {.unnumbered}

**[Step 11A]:** The spatial tutorial is FINALLY available. Make your house data 'spatial' by following this tutorial and assign it to a variable called house_sf [Tutorial - "How to make existing data spatial"](#T5_st_as_sf)

<br>

**[Step 11B]:** Type `house_sf` into the console or a code chunk to bring up the summary. Use this to find out the bounding box of your data and write the bounding box into your report. [Tutorial - "How to make existing data spatial"](#T5_st_as_sf)

<br>

**[Step 11C]:** Make an interactive qtm map of the price per unit area from your dataset (hint you already have this data/column, you only need to make the map) [Tutorial - QTM maps](#T5_qtmmaps)

<br>

**[Step 11D]:** Explore the data spatially by looking at the maps and changing the basemaps. In the text, write a paragraph decribing what you see to help your friend understand the spatial patterns of house prices in the area.

<br><br>

**Congrats! Finished!**

Becuase of the technical issues getting this homework up, this is everything you need to do for this week. And check out the rubric for some very easy grading.

<br><br>

## WHAT TO SUBMIT {.unnumbered}

<br>

### If you are using your own computer {.unnumbered}

Press knit one final time. You will have created two files; a `.Rmd` file containing your code and a `.html` file for viewing your finished document.

Find the html and RmD files in your Lab 1 folder on your computer. Double click the html file to open it in your browser and check it's the one you want to submit.

**You need to submit BOTH of these files on the relevant Canvas assignment page.**

You can also add comments to your submission as needed on the canvas page, or you can message Dr G.

<div class="figure">
<img src="./index_images/im_T1_WhattoSubmit.png" alt="Find them in your GEOG364 folder on your computer" width="100%" />
<p class="caption">(\#fig:L1-Submit)Find them in your GEOG364 folder on your computer</p>
</div>

<br>

### If you are using Posit Cloud online {.unnumbered}

1.  Press knit one final time. You will have created two files; a `.Rmd` file containing your code and a `.html` file for viewing your finished document.

2.  Go to the files tab an click on the little check-box by the RmD file. Then click the blue "more button" and press export. Save onto your computer.

<div class="figure">
<img src="./index_images/im_T1_CloudSubmit.png" alt="How do download the files from PositCloud" width="100%" />
<p class="caption">(\#fig:L1-CloudDownload)How do download the files from PositCloud</p>
</div>

2.  Uncheck the .RmD box and click the box by the html file. Then click the blue "more button" and press export. Save onto your computer.

**You need to submit BOTH of these files on the relevant Canvas assignment page.**

You can also add comments to your submission as needed on the canvas page, or you can message Dr G.

<br>

## CHECK YOUR GRADE! {#CheckGradeL1 .unnumbered}

### RUBRIC {.unnumbered}

This is how you will be graded (plus any in-class components)

25/25: You made a good effort and answered all the questions. If you came to the lab, there's probably about 10-15 mins additional work. CHECK EACH PART OF QUESTION 10 AND 11.

15/25: You attempted most of the lab and explained where you got stuck.

5/15: Any attempt! A single word or a canvas comment to say hi will get you 5 points even if you haven't attended lab, because I want to know people who are simply dropping a lab compared to people who are really struggling.

<!--chapter:end:in_02-Project1.Rmd-->


# (PART\*) [.]{style="color: white;"} {.unnumbered}

Placeholder


## What are projects {#T1A_ProjectIntro}
## Projects using posit Cloud {#T1_ProjectsCloud}
## Projects on your desktop {#T1_ProjectsDesktop}
### How to check you are running your project
### Returning to your lab project
#### From your computer
#### From inside R-studio.

<!--chapter:end:in_04-Tutorial01_Projects.Rmd-->


# Libraries/Packages {#T2_Libraries}

Placeholder


## IMPORTANT TAKE AWAY
## What are packages? {#T2_Libraries_about}
## Installing new packages {#T2_Libraries_install}
### Ways to install packages
#### 1. Click the "Install" (app-store) button in the Packages menu
#### 2. Look for the little yellow banner/ribbon
#### 3. Type the install command into the CONSOLE
## Loading/using packages {#T2_Libraries_load}
## Advanced: Forcing R to use a package (::) {#T2_singlecommand}
## Seeing what packages you already have
## Package Problem Solving {#T2_packageproblems}
### Installation
#### Why isn't my package downloading? R is frozen
#### R keeps asking to restart.
### Loading packages
#### Nothing happened when I ran the library command!
#### There was a load of text output - an error?

<!--chapter:end:in_04-Tutorial02_Libraries.Rmd-->


# R-Markdown {#T3_Markdown}

Placeholder


## What is markdown {#T31_Basics}
### What are R-Scripts?
### What is R-Markdown?
## Creating a markdown document {#T31_NewMarkdown}
## Important things to know {#T32_MarkdownImportant}
### All markdown documents have three components. {#T32A_whatisit?}
### Visual mode {#T32A_visualmode}
### Editing YAML Code {#Tut4E_YAML}
### Troubleshooting
### Changing the theme
### Adding other YAML options
## Knitting {#T32E_Knitting}
## Editing the report text
### Inserting images/tables and formatting {#T32B_formatting}
### Code chunks {#T32D_CodeChunks}
#### Adding a code chunk {#T32Da_Adding}
#### Editing and running code chunks {#T32Db_Editing}
## Writing Maths equations in R-Markdown {#T3_MathsEquations}
### Inserting an equation
#### Inline equations - Single dollar signs
### Writing the equations themselves
## Code Chunk options {#T3_CodeChunkOptions}
### Creating them in Source mode
### Creating them in Visual mode
### Setting the default for the whole document {#T3_CodeChunkWholeDoc}
### Common options
## Inline Code
#### Code chunks..... (as discussed above)
#### ..... and Inline Code
### Tips for adding inline code

<!--chapter:end:in_04-Tutorial03_Markdown.Rmd-->


# Coding {#T4_Coding}

Placeholder


## Quick reminder
## Functions / Commands
## Giving information to a function: arguments
### Commands are case sensitive!
### But you can put them on different lines..
### Working out the arguments
### A special case: functions with empty `( )`
## Stacking commands
## Referring to a column using `$` {#T4_applyingonecolumn}
## Saving your results using `<-`

<!--chapter:end:in_04-Tutorial04_CodingBasics.Rmd-->


# Reading in data {#T4_ReadingData}

Placeholder


## Before you start {#T4_DataCheck}
## Reading in your data {#T4_Commands}
### Spreadsheets and tables {#T4_ReadinSpreadsheets}
#### CSV files (.csv) — `read.csv()` {#T4_load_csv}
#### Excel files (.xlsx, .xls) — `read_excel()` {#T4_load_excel}
#### TXT files (.txt) — `read.table()` {#T4_load_txt}
### R-specific data {#T4_ReadinRData}
#### Built-in package datasets — `data()` {#T4_load_builtindata}
#### RDS files (.rds) — `readRDS()` {#T4_load_rds}
#### RData files (.RData, .rda) — `load()` {#T4_load_rdata}
### Spatial data {#T4_ReadinSpatial}
#### Vector files (.shp, .geojson, .gpkg) — `st_read()` {#T4_load_vector}
#### Raster files (.tif, .nc, .img) — `rast()` {#T4_load_raster}
## Troubleshooting {#T4_Troubleshooting}

<!--chapter:end:in_04-Tutorial05_ReadingInData.Rmd-->


# Summarising Data {#T5_Summarising}

Placeholder


## Overall :  Useful commands for looking at a dataset
## First look at your data {#T5_FirstLook}
#### View your data — `View()` {#T5_View}
#### Check structure — `str()` and `glimpse()` {#T5_str}
#### Check size — `nrow()`, `ncol()`, `dim()` {#T5_size}
## Checking and fixing column types {#T5_ColTypes}
#### Checking the type of a single column — `class()` {#T5_class}
### Factors {#T5_Factors}
#### Converting a column to a factor — `as.factor()` {#T5_asfactor}
#### Checking factor levels — `levels()` {#T5_levels}
#### Changing the reference level — `relevel()` {#T5_relevel}
#### Renaming factor levels — `levels()` assignment {#T5_relabel}
#### Ordered factors {#T5_ordered}
## Dealing with missing data {#T5_Missing}
#### Checking for missing values {#T5_checkNA}
#### Ignoring NAs in calculations — `na.rm = TRUE` {#T5_naInCalcs}
#### Removing rows where a specific column is NA — `filter()` {#T5_naFilter}
#### Removing all incomplete rows — `na.omit()` {#T5_naomit}
## Summarising your data {#T5_Summaries}
### The whole dataset {#T5_WholeSummary}
#### `summary()` {#T5_summary}
#### `skim()` {#T5_skim}
### A single column {#T5_SingleCol}
## Frequency tables {#T5_Tables}
## Troubleshooting {#T5_Troubleshooting}

<!--chapter:end:in_04-Tutorial06_Summary.Rmd-->


# Missing Data In Depth {#T6B_MissingData}

Placeholder


## What is missing data? {#T6B_WhatIsMissing}
#### Missing values in external datasets {#T6B_ExternalMissing}
#### Turning existing values into NA {#T6B_ForceNA}
## Why is data missing? {#T6B_WhyMissing}
## Identifying missing data {#T6B_Identifying}
#### Counting NAs {#T6B_Counting}
#### Summary functions {#T6B_SummaryFunctions}
#### Visualising missing data — `naniar` {#T6B_Visualising}
## Handling missing data {#T6B_Handling}
### Remove rows with any NA — `na.omit()` {#T6B_naomit}
### Remove rows where specific columns are NA {#T6B_FilterNA}
### Replace NAs with a value {#T6B_Replace}
## Missing data in common functions {#T6B_Functions}
#### `na.rm = TRUE` {#T6B_naRM}
#### Correlation and missing data {#T6B_Correlation}
## Missing data in regression models {#T6B_Regression}
## Command reference {#T6B_Commands}
## Troubleshooting {#T6B_Troubleshooting}

<!--chapter:end:in_04-Tutorial06B_MissingData.Rmd-->


# Plots {#T6_plots}

Placeholder


### What to choose?
### Where to find worked examples
## Example dataset
## Scatterplots {#T7_PlotsScatter}
### Basic plot (no line of best fit)
### GGplot2 scatterplots {#T7_PlotsScatter_ggplot2}
### GGplot2 adding a line of best fit. {#T7_PlotGGPlotWLine}
### GGplot2 adding a line of best fit and confidence intervals
### Plotly Interactive scatterplots! {#T6_ScatterPlotly}
### Basic plot WITH a line of best fit
## Histograms {#T7_Histograms}
### ggstatsplot histograms
### ggplot2 histograms
#### Adding a boxplot and histogram
#### Adding a density function
#### Adding a distribution
#### Mulitple histograms
## Boxplots {#T6_boxplots}
### Basics (single boxplot)
### Comparing groups
### Sophisticated
## Violin plots
## Ridgeline plots
## Beeswarm plots

<!--chapter:end:in_04-Tutorial07_Plots.Rmd-->


# Data Filtering {#T8_Wrangle}

Placeholder


## Introduction & packages
## Selecting COLUMNS
### Selecting a specific column using $
### Selecting multiple columns
#### Tidyverse Approach {-}
#### Base R Approach {-}
## SELECTING SPECIFIC CELLS
### Deleting data
## Selecting ROWS {#T8_RowSelect}
### Random sampling
### Tidyverse/dplyr filter command
### BaseR `which()` command
## Saving data to new columns
### Base R Approach {-}
### Tidyverse Approach {-}
## Sorting Data
### Tidyverse Approach {-}
### Base R Approach {-}
## Combining Everything
### Tidyverse Approach {-}
### Base R Approach {-}

<!--chapter:end:in_04-Tutorial08_Wrangling.Rmd-->


# Probability distributions

Placeholder


## What are they?  Full info
## The normal distribution {#T5_NormalDist}
### Help file
### Generate a random sample
### Calculate probability when given a z-score
### Calculate z-score when given a probability
### Testing normality
#### Wilks Shapiro test for normality
####  QQ-Norm plot
## T-distribution {#TDist}
### Calculate a probability given a T-Statistic
### Calculate a T-Statistic for a given probability
### T-Test {#Ttest}
## Others?

<!--chapter:end:in_04-Tutorial09_DistributionsHypTests.Rmd-->


# Correlation

Placeholder


## Basics
### Correlation not causation
## Correlation basic code
## Correlation matrices
### `corrplot()` from the corrplot library
## `ggcorrmat()` from ggstatsplot  {#T10_ggcorrmat}
## `ggpairs()` from `GGally`

<!--chapter:end:in_04-Tutorial10_Correlation.Rmd-->


# Simple Linear Regression {#T11_SLR}

Placeholder


## Running the model {#T11_RunModel}
### Example
### Important
## Model Outputs {#T11_Output}
#### Quick look {#T11_OLSregress}
#### Standard summary
#### The `ols_regress()` summary
## Writing the regression equation {#T11_Equation}
#### Population vs sample notation {#T11_Notation}
#### Filling in the numbers {#T11_FillIn}
#### Writing these equations yourself {#T11_EquationCode}
## Interpreting slope and intercept {#T11_Interpret}
#### The sample intercept ($b_0 = 114.09$) {#T11_Intercept}
#### The sample slope ($b_1 = -0.5749$) {#T11_Slope}
## Significance tests {#T11_Significance}
### Is the slope or intercept significantly different from zero? {#T11_SigZero}
### Confidence intervals on slope and intercept {#T11_CI}
### Testing against a non-zero value {#T11_SigOther}
## The F-test and ANOVA table {#T11_Ftest}
## $R^2$ and $r$ {#T11_Rsquared}
#### $R^2$ — coefficient of determination {#T11_R2}
#### $r$ — Pearson's correlation coefficient {#T11_r}
## Plotting the regression line {#T11_Plot}
#### Quick plot — base R {#T11_BasePlot}
#### Publication plot — ggplot {#T11_GGPlot}
## Checking LINE assumptions {#T11_LINE}
### Checking Linearity {#T11_Linearity}
### Checking Equal Variance (Homoscedasticity) {#T11_Variance}
### Checking Normality of Residuals {#T11_Normality}
### Checking Independence {#T11_Independence}
## Troubleshooting {#T11_TroubleshootingB}
## What are they
### An "outlier" {.unnumbered}
### A high leverage point {.unnumbered}
### An influential point {.unnumbered}
## How to find them
### Residual vs leverage plots
## Examples
### No outliers, influential or high leverage points {.unnumbered}
## How to find them
### Assessing outliers via visual inspection
### No outliers, influential or high leverage points {.unnumbered}
### An outlier with no leverage {.unnumbered}
### A high leverage point that isn't an outlier {.unnumbered}
### An influential high leverage outlier {.unnumbered}
### Detecting outliers via plots
### Detecting influential points
## Troubleshooting {#T11_Troubleshooting}

<!--chapter:end:in_04-Tutorial11_SLR.Rmd-->


# Spatial data {#T5_VectorSpatial}

Placeholder


## Example datasets
## Useful tutorials
## Spatial data basics {#T5_WhatIsSpatial}
### Map projections
#### The UTM system
#### EPSG codes
## Vector Data {#T5_sfobjects}
### How to make existing data "spatial" (`st_as_sf`) {#T5_st_as_sf}
#### Step 1: Note the column names of your x/y coordinates {.unnumbered}
#### Step 2: Note the coordinate reference system {.unnumbered}
#### Step 3: Make the data spatial {.unnumbered}
### Reading spatial data from file — `st_read()` {#T5_st_read}
#### Reading in shapefiles
### Exploring vector data {#T5_sfexplore}
### Keeping the long/lat/coordinate columns
## Making basic maps (qtm) {#T5_qtmmaps}

<!--chapter:end:in_04-Tutorial12_SpatialBasics.Rmd-->


# Making maps

Placeholder


## LIBRARIES NEEDED
## Example Data
## Quick thematic map (qtm)
## Basic Tmap
## Start adding tmap options
## Nicer example
## Tmap components
### tmap_mode()
### Colour palettes
### The + sign
### tm_basemap()
### IMPORTANT tm_shape()
### tm_dots()
### tm_symbols()
### tm_borders()
### tm_polygons()
### Extras
## 

<!--chapter:end:in_04-Tutorial13_Maps.Rmd-->

