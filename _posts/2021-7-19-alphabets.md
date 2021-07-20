---
layout: post
title: "Print alphabets with their ASCII CODE"
---

## Introduction
This program prints alphabets with their ASCII Code.

## Algorithm
1. Start
1. Get ASCII code for A and Z
1. Print character and ASCII code for A
1. Repeat step 3 for all characters until Z
1. End

## Program
```
REM "---------------------------------------"
REM "Prints alphabets from a to z and A to Z
REM "---------------------------------------"

'ASCII code for A and Z
A% = ASC("A")
Z% = ASC("Z")

'ASCII code for a and z
sa% = ASC("a")
sz% = ASC("z")

PRINT "Alphabets with their ASCII code"
PRINT

REM "Prints alphabets with their ASCII code from A to Z"
FOR m% = A% TO Z% STEP 1
    PRINT CHR$(m%); " = "; m%; "  ";
NEXT m%

PRINT
PRINT

REM "Prints alphabets with their ASCII code from a to z"
FOR n% = sa% TO sz% STEP 1
    PRINT CHR$(n%); " = "; n%; "  ";
NEXT n%

```

## Description

**ACS :**

ASC returns the ASCII code for the character of the string. 

Example :


`ASC("A")` returns *ASCII CODE*

The following program returns the ASCII code from capital A to Z
```
A% = ASC("A")
Z% = ASC("Z")

FOR m% = A% TO Z% STEP 1
    PRINT CHR$(m%); " = "; m%; "  ";
NEXT m%
```

**CHR$ :**

CHR$ returns the character corresponding to the ASCII code.

Example :

`PRINT CHR$(65)` returns *A*