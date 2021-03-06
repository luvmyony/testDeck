---
title       : BMI Calculator Application
subtitle    : Shiny Project
author      : MYK
job         : Data Science Specialization student
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : [mathjax]            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Objective of the project

### To demonstrate the skills

* to build an application using Shiny
* to prepare and publish presentation using Slidify and/or Rstudio Presenter.


--- .class #id 

## About the BMI Calculator Application

### What is BMI?

BMI (Body Mass Index) is a measure of weight proportionate to height. Generally, BMI is considered an effective way to evaluate a person's degree of obesity. The index is calculated simply using one's height and weight.

### Manual Calculation of BMI

$$\frac{\text{weight(lbs)}*703}{\text{height(inches)}^2}$$


--- .class #id

## BMI Calculation using R

```r
ht_feet <- 5
ht_inches <- 3
wt_lbs <- 130

bmi <- function(f,i,p) round(703*p/((f*12+i)^2),1)
category <- function(x) {
  if (x <= 18.5) return("Underweight")
  else if (x > 18.5 & x < 25) return("Normal Weight")
  else if (x >= 25 & x < 30 ) return("Over Weight")
  else return("Obesity")
}
b <- bmi(ht_feet, ht_inches, wt_lbs)
c(b, category(b))
```

```
## [1] "23"            "Normal Weight"
```

--- .class #id

## How does the Application work?
* It takes height in feet and inches, and weight in pounds as inputs.

* Once a user enters the values and clicks on the "Calculate BMI" button, BMI index and category of obesity will be displayed.

* Go to the link below and get your BMI instantly by just entering your height and weight.   
http://luvmyony.shinyapps.io/BMIcalculator/

* The codes for the application can be found in the following link.  
http://github.com/luvmyony/ShinyProjectRepo
