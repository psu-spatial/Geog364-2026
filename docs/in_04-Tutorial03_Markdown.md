

# R-Markdown {#T3_Markdown}

## What is markdown {#T31_Basics}

Remind yourself of what Rmarkdown is here <https://rmarkdown.rstudio.com> via this short video

<iframe title="vimeo-player" src="https://player.vimeo.com/video/846773750?h=7cb3871e91" width="640" height="360" frameborder="0" referrerpolicy="strict-origin-when-cross-origin" allow="autoplay; fullscreen; picture-in-picture; clipboard-write; encrypted-media; web-share" allowfullscreen>

</iframe>

### What are R-Scripts?

Read more here: <https://rmarkdown.rstudio.com>

Typing in console is like a having phone call with the computer, you're talking but you're not keeping records of what you say. When you close R-studio you lose your analysis.

What we need instead is a way to save the commands for future use - we can do this using scripts. There are several types of document, or script that you can create and save in R-Studio.

- A basic script (the file-type is .r). This is simply just a blank notepad where you can save code commands. When you "run" the commands in the script, R simply copy/pastes the commands over to the console. This is probably how you have done previous labs.

- An R-Notebook or R-Markdown document (the file type is .Rmd). These are much more interesting - and are how I wrote this lab book. This is what we will be using in our labs. \
  There is actually a more recent successor to these called a Quarto file. We will use markdown, but if you can use markdown, you can use quarto!

In this course we are going to focus on the R-Markdown format and you are going to submit your labs as websites/html files along with your code.

<br>

### What is R-Markdown?

What is an R-Markdown Document? imagine a normal Microsoft Word document, but halfway through you can press a button and a mini R console appears.... You type your code inside the mini console, and click run. The computer runs the code and puts the plots/output directly into your report - then you leave the console and write about the results below the plot.

As described in the video, Rmd files are also flexible. You can turn them into reports, websites, blogs, presentations or applications with a few short commands.

<br>

## Creating a markdown document {#T31_NewMarkdown}

Go to the File menu on the top left, then click New File - R-Markdown. If this is your first time ever doing this, it might ask to download some packages to be able to do this (look for a little yellow bar at the top of the screen and say yes)

Eventually a window will open up:

<img src="./index_images/pg_Tut4_markdown_fig1.png" alt="" width="80%" style="display: block; margin: auto;" />

- It will ask you to name and save your file. Give it a relevant name.

- A new file should appear on your screen.

- At the top of that window (by the knit button, there is a save button. Save it as something relevant INSIDE YOUR PROJECT FOLDER!

<div class="figure" style="text-align: center">
<img src="./index_images/pg_Tut4_markdown_fig2.png" alt="Yours will say STAT462 rather than GEOG364" width="80%" />
<p class="caption">(\#fig:tut4fig2)Yours will say STAT462 rather than GEOG364</p>
</div>

The new file on your screen is your first markdown script.

<br><br>

------------------------------------------------------------------------

## Important things to know {#T32_MarkdownImportant}

<br>

### All markdown documents have three components. {#T32A_whatisit?}

<br>

All markdown documents have three components.

- There is a space at the top of the file where we can add information about themes/styles etc called "YAML". This determines what type/style of document your work will become <br>
- There is space to add text (white), <br>
- And you can add code in 'mini consoles' called 'code chunks'. (Grey) <br>

<div class="figure" style="text-align: center">
<img src="./index_images/im_T3_Markdown.png" alt="Markdown Components" width="100%" />
<p class="caption">(\#fig:tut4fig4)Markdown Components</p>
</div>

<br><br>

### Visual mode {#T32A_visualmode}

It is MUCH easier to edit markdown documents in the new visual mode. Essentially instead of having to remember text short cuts like \*\* for bold, you can edit the text part as though you were using a word processor. NOTE HEADERS where it says "Normal", this allows you to make auto tables of contents.

<div class="figure" style="text-align: center">
<img src="./index_images/im_T3_SourceVisual.png" alt="Look at the circled button near the top of the two reports" width="100%" />
<p class="caption">(\#fig:im-T3-SourceVis)Look at the circled button near the top of the two reports</p>
</div>

<br>

### Editing YAML Code {#Tut4E_YAML}

Your YAML code is the code at the top of your file in between the --- lines. (see \@ref(fig:tut4fig4))). Let's zoom in

<img src="./index_images/pg_Tut4_markdown_fig5.png" alt="" width="80%" style="display: block; margin: auto;" />

<br>

Your YAML code controls how your final output looks and which type of output it becomes. For example, your document could become a website, a pdf, a presentation or app..

The basic version is very simple with a title, an author and a self entered date. Let's add in more options.

YAML code is annoying to edit, because here, *spaces really do matter*. Everything has to be perfect or it won't knit.

**Select everything in my code chunk here and replace your YAML with this (remember the --- on line 1 and at the end).**


``` r
---
title: "GEOG-364 - Lab 2"
author: "hlg5155"
date: "`r Sys.Date()`"
output:
  html_document:
    toc: true
    toc_float: yes
    number_sections: yes
    theme: lumen
    df_print: paged
---
```

Replace the author ID with your user name, change the title if appropriate.

The elements we just added are:

- The title
- The author (note,use your ID not your name)
- Automatically created today's date
- A floating table of contents
- Numbered sections (this won't appear until you start typing section headings)
- The document is now in the lumen theme.

<br>

### Troubleshooting

- Note, if you copy/paste this and it doesn't work, sometimes the quote marks copy weirdly from the internet - try deleting and retyping the quotes.

- If it still doesn't work.. this might be because a space is missing (especially if you typed it out).

  - Editing YAML code can be a pain. It is very case and space sensitive.<br>For example, the spaces at the start of some lines are important and are created using the SPACE BAR, not the tab key.

*Don't continue until you can make and view your html when you press knit. If it doesn't work, ask for help before moving on*

<br>

### Changing the theme

You don't need to choose the lumen theme. There are many other ways you can edit your markdown documents here: <https://www.datadreaming.org/post/r-markdown-theme-gallery/>

To edit, replace the word lumen with the name of your chosen theme (THIS IS CASE SENSITIVE). Now click knit and see if it works.Some themes are buggy. Try a different one if it doesn't work.

The themes in "Even More Themes" on the website, require you to install/load some new packages, so they need some extra work. You're welcome to try if you have one you fell in love with!

<nr>

### Adding other YAML options

There are many more details about different options on these websites:

- <https://bookdown.org/yihui/rmarkdown/html-document.html>
- <https://rstudio.com/wp-content/uploads/2015/03/rmarkdown-reference.pdf>

If you want to get really fancy, there is an interesting package to help you design YAML code here: <https://education.rstudio.com/blog/2019/10/tools-for-teaching-yaml-with-ymlthis/>

<br> <br>

## Knitting {#T32E_Knitting}

<img src="./index_images/im_T3_knit.png" alt="" width="100%" style="display: block; margin: auto;" />

The file on your screen isn't the finished article. To see how it will look as a final version, we need to "knit" it. Go to the top of the .Rmd file, find the `knit` button. Press it (you might have to first save your script if you haven't already, then press it again)

You should see that the Markdown tab "builds" your document and you get an output as a website. The html should also be saved into your project folder.

For example, here is a file with markdown and knitted output.

<img src="./index_images/im_T3_AllMarkdownElements.png" alt="" width="100%" style="display: block; margin: auto;" />

<br><br>

## Editing the report text

You can type anywhere inside the white report area. R will ignore it.

<br>

### Inserting images/tables and formatting {#T32B_formatting}

In visual mode, look at the menu at the top. It's very easy to insert images, tables and other formatting. Pay special attention to the Normal/Heading 1/Heading 2 buttons..

**You can also use the "insert anything" menu by typing / on a new line and choosing bullet point list, picture, heading levels or any other formatting choice.**

You can also do this in source mode, but you have to learn the keyboard shortcuts. For example to make something **bold** you put stars around it e.g. `**bold**` . You can see more examples in the pic above and here

For more, see this link: <https://zsmith27.github.io/rmarkdown_crash-course/lesson-3-basic-syntax.html>

<br><br>

------------------------------------------------------------------------

### Code chunks {#T32D_CodeChunks}

Code chunks are mini consoles where you can run R commands.

#### Adding a code chunk {#T32Da_Adding}

On the top right there are a suite of buttons for adding a new code chunk, running code etc. The green one adds a new code chunk.

**You can also use the "insert anything" menu by typing / on a new line and choosing an R code chunk,**

<img src="./index_images/im_T3_CodeChunkCreate.png" alt="" width="100%" style="display: block; margin: auto;" />

<br>

#### Editing and running code chunks {#T32Db_Editing}

You should see that a new area has appeared in your report that is a different color to the background. Inside its essentially a "mini console". It's where you add your code and you need to 'speak R' inside it.

When you press enter, the code won't run. INSTEAD, click the little green arrow

<img src="./index_images/im_T3_RunCodeChunk.png" alt="" width="100%" style="display: block; margin: auto;" />

<br>

------------------------------------------------------------------------

<br>

## Writing Maths equations in R-Markdown {#T3_MathsEquations}

Equations in R-Markdon use the "LateX" format.

### Inserting an equation

Equations in R-Markdon use the "LateX" format.

To make a new equation on a new line, you first need to put them between double dollar signs.

For example, try typing

`$$`

`x=2`

`$$`

on a new line of the white text area in your report ( NOT INTO A CODE CHUNK), then pressing knit. You should see:

$$x=2$$

**You can make a space for an equation the "insert anything" menu by typing / on a new line and choosing "display math"**

<br>

#### Inline equations - Single dollar signs

Essentially this is the same, but the equation is part of the text and you only see the output when you press knit. For example including `$x=2$` in this sentence shows $x=2$ as an output.

**You can make a space for an inline equation via "insert anything" menu by typing / on a new line and choosing "inline math"**

<br><br>

### Writing the equations themselves

How do we write all the fancy equation stuff? We cheat.

Create the equation you want in one of these generators, then copy the code into your script and put it between double dollar signs:

- <https://latex.codecogs.com/eqneditor/editor.php>
- <https://www.tutorialspoint.com/latex_equation_editor.htm>

For example

`$$\widehat{y} = b_{0}+b_{1}x$$`

Shows up as $$\widehat{y} = b_{0}+b_{1}x$$

Or, try asking chatgpt/claude to help (although it does get confused sometimes on exactly which type of latex to use - so TELL IT THAT YOU WANT A VERSION THAT WORKS FOR R-MARKDOWN!)

<br>

------------------------------------------------------------------------

<br>

## Code Chunk options {#T3_CodeChunkOptions}

What are they? Essentially, instructions that you tell the computer when you press knit.

### Creating them in Source mode

Click source mode and have a look at a code chunk. You will see it starts with three little back-ticks and the {r} sign. For code chunk options, we will be focusing on the top line with the {r}

<img src="index_images/im_T3CodeChunkOptions.png" alt="" width="100%" style="display: block; margin: auto;" />

At the moment, the code chunk tells us that the code inside is written in R.

We can also add other options, **separated using commas.**

<img src="index_images/im_T3CodeChunkOptionsComplete.png" alt="" width="100%" style="display: block; margin: auto;" />

In fact, you have often seen me add message=FALSE and warning=FALSE to prevent any spurious messages appearing when you press knit. Keep reading to see the many other things you can add.

<br>

### Creating them in Visual mode

You can also edit code chunk options in view mode. Create a new code chunk, then click on the little (almost invisible) cogwheel near the run triangle

<img src="index_images/im_T3CodeChunkOptionsView.png" alt="" width="100%" style="display: block; margin: auto;" />

This will open a menu where you can choose many of the common options

<img src="index_images/im_T3CodeChunkOptionsViewMenu.png" alt="" width="70%" style="display: block; margin: auto;" />

<br>

### Setting the default for the whole document {#T3_CodeChunkWholeDoc}

Many templates already include this for you to edit.

If not, you can put a code chunk at the top of your document (below the YAML code) containing `knitr::opts_chunk$set(echo=TRUE)` to change the default values of chunk options in a document.

For example, you may put this in the first code chunk of your document to stop it showing messages on knit.

````         
```{}
knitr::opts_chunk$set(echo=TRUE, 
                      warning=FALSE, 
                      message=FALSE)
```
````

<br>

### Common options

Here are the common options we typically need:

- `message = TRUE/FALSE`. Don't show friendly R messages on knitting. I use this so often that I put it in that knitr code chunk at the top of my scripts. <br>

- `warning = TRUE/FALSE` . Don't show R warnings on knitting. It will still show errors, so this is another good one to use. <br>

- `include = TRUE/FALSE.` Show or Hide the code AND output in the final document. <br>

- `echo = TRUE/FALSE.` Show or Hide the code chunk code in the final document. The output will still be shown. <br>

- `eval = TRUE/FALSE`. This option determines whether the code is evaluated or executed. If **`eval = TRUE`**, the code is executed. If **`eval = FALSE`**, the code is not executed, but the code chunk is still displayed. This can be useful for showing example code without actually running it.

- Or for example, if you can't knit because of an error, you can add eval=FALSE to the problem code chunk so I can see what you did but you can still knit.

<br><br>

------------------------------------------------------------------------

## Inline Code

There are two types of code you can write in your reports: code chunks and inline R code.

#### Code chunks..... (as discussed above)

Click source mode and have a look at a code chunk. You will see it starts with three little back-ticks and the {r} sign.

<img src="index_images/im_T3CodeChunk.png" alt="" width="100%" style="display: block; margin: auto;" />

#### ..... and Inline Code



Inline R code is embedded in the TEXT/NARRATIVE of your document using single back-ticks. For example, writing

My value of y is `` `r y` `` and x-squared is `` `r x^2` ``

Will output:

My value of y is 10 and x-squared is 49.

If this doesn't make sense, follow these tutorial to see how to add inline code.

- <https://bookdown.org/yihui/rmarkdown-cookbook/r-code.html>
- <https://www.njtierney.com/post/2019/07/10/jq-verbatim-inline-r/>
- <https://rmarkdown.rstudio.com/lesson-4.html>

<br><br>

### Tips for adding inline code

Inline code is GREAT. Imagine writing your 100 page thesis, but then you realise that your dataset was wrong. If all the numbers in your report are added using inline code, then it will automatically update your entire report.

The easiest way to do this is to run your commands in a "silent" code chunk with the echo=FALSE and include=FALSE options. Then in the text, I just put the variable name I want to print, sometimes rounding to a better number of decimal places[^in_04-tutorial03_markdown-1].

[^in_04-tutorial03_markdown-1]: You can round in the inline code or the code chunk. Both are fine



For example here's how I typed that the mean height of the starwars data is 174.6 cm:

<img src="index_images/im_T3InlineCode.png" alt="" width="100%" style="display: block; margin: auto;" />
