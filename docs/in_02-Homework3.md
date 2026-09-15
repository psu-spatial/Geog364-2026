# (PART\*) [.]{style="color: white;"} {.unnumbered}

# (PART\*) **LAB INSTRUCTIONS** {.unnumbered}



# Homework 3 {#Lab_3 .unnumbered}

### Aim {.unnumbered}

Welcome to Homework 3. This is worth 15/20 (the other 10 was for the in-class exercises). Overall each lab is worth 4.8% and you can drop your lowest score.

This is due the night before your next lab. The maximum time it should take is about 2-3 hrs of your time, plus lab time.

The aim of this lab is to get comfortable with spatial data and exploratory analysis.

<br>

### Need help?

REMEMBER THAT EVERY TIME YOU RE-OPEN R-STUDIO YOU NEED TO RE-RUN **ALL** YOUR CODE CHUNKS. The easiest way to do this is to press the "Run All" button, in the "Run" menu at the top right of your screen

<br>

<br>

------------------------------------------------------------------------

## PART 1: LAB SET-UP (Important!) {.unnumbered}

### STEP 1: Create your project for homework 3 {.unnumbered}

- **[1A]** Make a project for Homework 3 (tutorial here) [Projects](#T1_Projects)

- **[1B]** Open your Homework3 project in R-Studio (see screenshot below).

<div class="figure">
<img src="./index_images/im_T1_Projectcheck.png" alt="Yours should look like this but say the name of your homework 3 project" width="100%" />
<p class="caption">(\#fig:L3-Projectcheck)Yours should look like this but say the name of your homework 3 project</p>
</div>

<br>

------------------------------------------------------------------------

### STEP 2: Create your lab report structure & YAML code {.unnumbered}

- **[2A]** Make a new RMarkdown Report ([Tutorial here](#T31_NewMarkdown)) <br>

- **[2B]** As we discussed last week, your YAML code at the top of your script tells R how to make the final report. It lives between the --- lines. CAREFULLY replace the YAML code with this code (remember to only have one set of ---) and press knit.


``` r
---
title: "GEOG-364 - Homework 3"
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

### STEP 4: NEW (ish) Adjust your knit options {.unnumbered}

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

### STEP 6: Finally.. sort out libraries {.unnumbered}

It's good practice to have a single code chunk near the top of the script containing all your library commands. This is to stop duplicated code and to make it easy to see what you are loading before running your labs.

- **[6A]** Add a new code chunk under the opts one, and add the code inside it to load the packages.


``` r
library(tidyverse) # Lots of data processing commands
library(knitr)     # Helps make pretty output files
library(ggplot2)   # Output plots
library(skimr)     # Summary statistics
library(sf)        # Spatial commands
library(tmap)      # Mapping commands
library(plotly)    # Interactive plots
library(readxl)    # Read from excel files
```

- **[6A]** Then press save or try to knit. If any packages are missing you will see

  - EITHER a little yellow bar at the top of the screen asking if you want to install the libraries. Say yes, wait until the libraries are installed and try again. <br>
  - OR an error saying that it can't find that library (it might also be a spelling mistake if you are sure it's installed). In this case, you have to go to the app store and download it (Packages/Install). <br>\

<br><br>

### STEP 7: Check progress {.unnumbered}

- OK - so by now, you should be running the project for homework 3, you have created your lab report, the YAML code works and your libraries work. If not, STOP, go back and redo the tutorials or talk to Dr G/Samrin

<br><br>

------------------------------------------------------------------------

## PART 2: IN-CLASS WORK {.unnumbered}

You are allowed and encouraged to work in groups for this section

<br><br>

### STEP 8: Reading in data {.unnumbered}

In lab 1, we used data that was built into R. This week we will read in data from files.

- **[8A]** Go to the canvas assignment page. Download all the datasets for the lab AND PUT THEM IN THE HOMEWORK 3 PROJECT FOLDER ON YOUR COMPUTER.

- **[8B]** In the TEXT part of the report, below the library code chunk, make a new heading 1, text header called "In-Class work".

- **[8C]** Below that, make a new code chunk. Use the read_excel() command to load the "Lab03_house.xlsx" data into your report and assign it it to a variable called House ([Tutorial 4 - Read Excel](#T4_load_excel)).

<br><br>

### STEP 9: Understand where the data has come from {.unnumbered}

IMPORTANT. Imagine that next month, your friend is moving to Sindian Dist., in New Taipei City, Taiwan. They want to buy a house and have asked you to figure out what most impacts house price.

YOU ARE WRITING THIS REPORT FOR THEM!

- **[9A]** You have been given a specific dataset to help answer your friend's question. Read more about the data here:<https://archive.ics.uci.edu/ml/datasets/Real+estate+valuation+data+set>.

- **[9B]** In your report, describe the data, including the object of analysis, population and variables. Now critique it! What aspects of this data are useful for your friend or not useful.

<br><br>

More to come.

------------------------------------------------------------------------

## PART 3: TAKE HOME WORK {.unnumbered}

<br><br>

### TO BE UPDATED

**Congrats! Finished!**

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

15/15: Exceptional! Hard to get! You understood the nuance of all the questions and have a very clear understanding of the concepts. Your lab book report is easy to read and its easy to find the answers.

14/15: Thoughtful, accurate, and shows a clear understanding of the concepts, with only very minor errors or omissions.Your lab book report is easy to read and its easy to find the answers.

12/15: Mostly accurate and shows a good understanding, but with some errors, omissions, or weaker explanations

9/15: Shows some understanding, but several answers are incorrect, incomplete, or unclear

5/15: Any attempt! A single word or a canvas comment to say hi will get you 5 points even if you haven't attended lab, because I want to know people who are simply dropping a lab compared to people who are really struggling.

Overall, here is what your lab should correspond to:

<table class=" lightable-classic-2 table table-striped table-hover table-responsive" style='font-family: "Arial Narrow", "Source Sans Pro", sans-serif; margin-left: auto; margin-right: auto; margin-left: auto; margin-right: auto;'>
 <thead>
  <tr>
   <th style="text-align:left;"> POINTS </th>
   <th style="text-align:left;"> Approx grade </th>
   <th style="text-align:left;"> What it means </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> 98-100 </td>
   <td style="text-align:left;"> A* </td>
   <td style="text-align:left;"> Exceptional.  Above and beyond.   THIS IS HARD TO GET. </td>
  </tr>
  <tr>
   <td style="text-align:left;"> 93-98 </td>
   <td style="text-align:left;"> A </td>
   <td style="text-align:left;"> Everything asked for with high quality.   Class example </td>
  </tr>
  <tr>
   <td style="text-align:left;"> 85-93 </td>
   <td style="text-align:left;"> B+/A- </td>
   <td style="text-align:left;"> Solid work but the odd  mistake or missing answer in either the code or interpretation </td>
  </tr>
  <tr>
   <td style="text-align:left;"> 70-85 </td>
   <td style="text-align:left;"> B-/B </td>
   <td style="text-align:left;"> Starting to miss entire/questions sections, or multiple larger mistakes. Still a solid attempt.  </td>
  </tr>
  <tr>
   <td style="text-align:left;"> 60-70 </td>
   <td style="text-align:left;"> C/C+ </td>
   <td style="text-align:left;"> It’s clear you tried and learned something.  Just attending labs will get you this much as we can help you get to this stage </td>
  </tr>
  <tr>
   <td style="text-align:left;"> 40-60 </td>
   <td style="text-align:left;"> D </td>
   <td style="text-align:left;"> You submit a single word AND have reached out to Dr G or Aish for help before the deadline (make sure to comment you did this so we can check) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> 30-40 </td>
   <td style="text-align:left;"> F </td>
   <td style="text-align:left;"> You submit a single word…....  ANYTHING..                Think, that's 30-40 marks towards your total…. </td>
  </tr>
  <tr>
   <td style="text-align:left;"> 0+ </td>
   <td style="text-align:left;"> F </td>
   <td style="text-align:left;"> Didn’t submit, or incredibly limited attempt.  </td>
  </tr>
</tbody>
</table>
