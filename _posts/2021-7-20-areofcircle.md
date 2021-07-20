---
layout: post
title: "Find the area of a circle"
---

## Introduction
This program finds the area of a circle.

## Algorithm
1. START
1. Ask for radius
1. Multiply PI (22/7) with the square of radius
1. Print the result
1. STOP

## Program
```
REM "----------------------------------------"
REM "Area of a circle"
REM "----------------------------------------"

DIM PI AS SINGLE
PI = 22 / 7

INPUT "Enter radius"; radius!
area! = PI * radius! ^ 2
PRINT "The area of a circle with radius"; radius!; "="; area!

END

```