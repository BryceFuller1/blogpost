---
title: Dashboards in R Shiny
layout: post
author: BryceFuller1
post-image: "https://raw.githubusercontent.com/thedevslot/WhatATheme/master/assets/images/SamplePost.png?token=AHMQUEPC4IFADOF5VG4QVN26Z64GG"
description: An introduction to why shiny dashboards are useful and how to create a simple one.
tags:
- R
- Shiny
- Web Applications
---

# Introduction

This post will provide an introduction into what an R shiny application is, why they are useful, and how to create a simple web application. 

# What is an R Shiny Application?

R Shiny is a framework that was created by Rstudio in order to convert programs written in R into a web application. Often we see people coming out with Shiny applications that are very diverse in their purposes. One of the most common types of applications we see have to deal with geospatial data, allowing users to see trends in data across different geographic areas. They often have feature sliders which allow users to set different features across the data in order to explore the data more in depth. A good example of this is an application that enables users to see crime rates with feature sliders that can show crime rates based on important characteristics such as average income in the area, percentage below the poverty level, and even features you might not initially deem important such as daily average temperature. The following image is an example of an application taken from the Rstudio gallery that tracks crime rates in different parts of the world.

![](https://github.com/BryceFuller1/blogpost/blob/master/Screen%20Shot%202021-11-01%20at%202.43.31%20PM.png)

# Why are they useful? 
One of the biggest reasons why R Shiny applications are useful is that they allow users who are not proficient in R to explore and experiment with data in new and exciting ways that they would not be able to do on their own if they just had access to the raw data. Another reasons these applications are useful is that R programmers who wish to publish these applications don't actually need any web development experience. They simply need to learn the framework for Shiny and suddenly they are able to publish very interactive and useful applications for people who may not have any experience with R or even statistics for that matter. 

# How to Make A Simple App

We will now learn how to make a simple app that functions as a calculator that can add two numbers with a calculate button. In Shiny there are two parts to every app. The first is the user interface side and the second is the server side of the application. In the user interface side we can define what the user of the app is able to see such as different input systems and how reactive the application is. We can make it to where the app constantly refreshes after the user enters a character if there is a text box, changes the value on a slider, or we can make it to where the user enters all the requested input and then presses a button to refresh the app with the new information when they are ready,


We first start with the user interface side where we create two input boxes along with a button that when clicked calculates the difference between the two numbers.

```R
ui <- pageWithSidebar(
  headerPanel("actionButton test"),
  sidebarPanel(
    numericInput("one", "First Number:", min = 0, max = 100000, value = 1),
    numericInput("two", "Second Number:", min = 0, max = 100000, value = 0),
    br(),
    actionButton("goButton", "Go!"),
    p("Click the button to update the value displayed in the main panel.")
  ),
  mainPanel(
    verbatimTextOutput("nText")
  )
)
```
