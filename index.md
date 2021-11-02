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

```R
def func():
  target_val = 26.17          # O(1)
  num = 0                     # O(1)
  for i in df.some_column:    # O(n)
    for j in i[0]:            # O(n) -> because it occurs within the first loop, multiply n * n = O(n²)
      if j == target_val      # O(1)
      num += 1                # O(1)
  
  lst = []
  for k in df.other_column:   # O(n)
    lst.append(k)             # O(1)
```
