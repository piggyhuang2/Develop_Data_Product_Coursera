---
title       : Shiny App Presentation
subtitle    : Develop Data Products Course Project
author      : Piggyhuang2
job         : DS student
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Slide 2

This presentation is aimed to go through the ideas behind my simple shiny app.
I use this simple shiny app to show the summary stats of three small datasets, 
sleep, mtcars and iris. All of them can be loaded through data library. Users can view 
each dataset's summary stats by clicking their name at the dropdown box.

---


## Slide 3:

* Here are some sample code in server.R:

```r
  datasetInput <- reactive(function() {
    switch(input$dataset,
           "sleep" = sleep,
           "mtcars" = mtcars,
  	   "iris" = iris
          )
  })
```

---

## Slide 4:
* Here are some sample code from ui.R:

```r
sidebarPanel(
    textInput("caption", "Caption:", "Data Summary"),
    
    selectInput("dataset", "Choose a dataset:", 
                choices = c("sleep", "mtcars", "iris")),
    
    numericInput("obs", "Number of observations to view:", 10)
  )
```

---

## Slide 5:

* Here is the link to my simple Shiny App:

  http://piggyhuang2.shinyapps.io/shiny_summary




