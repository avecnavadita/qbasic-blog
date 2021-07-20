---
layout: post
title: "Clean the given string"
---

## Introduction
This program extracts **ONLY** numbers, alphabets and spaces from the given string and prints the clean string.

## Algorithm
1. Start
1. Ask for input string
1. Get each character from the string
1. Convert the character to its ASCII code
1. Check for A to Z (A=65 / Z=91) and append in a global variable
1. Check for 0 to 9 (0=41 / 9=57) and append in a global variable
1. Check for space (space=32) and append in a global variable
1. Repeat the above steps(from step 3 onwards) for all the characters in the string
1. Print the result
1. End

## Program 
```
REM "a program to extract alphabets and numbers from the given string"

sentence$ = "hi, my name is 123 thisthisthis !@#$%"

'for all the characters in the given string
FOR x% = 1 TO LEN(sentence$)

    'get each character from the string
    char$ = UCASE$(MID$(sentence$, x%, 1))

    'convert the character to its ASCII code
    code% = ASC(char$)

    'check for A to Z  (A=65 / Z=91)
    IF code% >= 65 AND code% <= 91 THEN
        result$ = result$ + char$

    'check for 0 to 9 (0=41 / 9=57)
    ELSEIF code% >= 48 AND code% <= 57 THEN
        result$ = result$ + char$

    'check for space (space=32)
    ELSEIF code% = 32 THEN
        result$ = result$ + char$
    END IF

NEXT x%
'print the result
PRINT result$
```

Hre's the same program using function

```
REM "a program to extract alphabets and numbers from the given string"

sentence$ = "Hi, my name is 123 thisthisthis !@#$%"

clearText$ = alphaNum$(sentence$)
PRINT clearText$

sentence$ = "Hi, my name is blahblahblahhhh%$#@1236"

clearText$ = alphaNum$(sentence$)
PRINT clearText$

'for all the characters in the given string
FUNCTION alphaNum$ (sentence$)
    FOR x% = 1 TO LEN(sentence$)

        'get each character from the string
        char$ = (MID$(sentence$, x%, 1))

        'convert the character to its ASCII code
        code% = ASC(UCASE$(char$))

        'check for A to Z  (A=65 / Z=90)
        IF code% >= 65 AND code% <= 90 THEN
            result$ = result$ + char$

        'check for 0 to 9 (0=41 / 9=57)
        ELSEIF code% >= 48 AND code% <= 57 THEN
            result$ = result$ + char$

        'check for space (space=32)
        ELSEIF code% = 32 THEN
            result$ = result$ + char$
        END IF
    NEXT x%
    'print the result
    PRINT result$
END FUNCTION
```
<!-- 
## Description

**MID$ :**

This function is used to extract characters from the given string. 

Example :


`MID$("apple", 2, 2)` returns *pp*

The following program returns two characters, *go* from the fourth position of the string "mango"
```
fruit$ = "mango"
MID$(fruit$, 4, 2) 
```

**LCASE$ :**

This function returns the string in lowercase.

Example :

`LCASE$("HELLOWORLD")` returns *helloworld*

(Similarly, `UCASE$` returns the string the uppercase)

[Reference: Our GitHub](https://github.com/avecnavadita/QBASIC)

**Function Procedure**

A Function procedure is a series of Visual Basic statements enclosed by the Function and End Function statements. The Function procedure performs a task and then returns control to the calling code. When it returns control, it also returns a value to the calling code. -->