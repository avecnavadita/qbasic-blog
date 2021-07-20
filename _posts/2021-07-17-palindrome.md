---
layout: post
title: "Check if a string is palindrome"
render_with_liquid: false
---

## Definition
A palindrome is a word, number, phrase, or other sequence of characters which reads the same backward as forward, such as madam or racecar.

## Algorithm
1. Start
1. Ask for input
1. Remove the space from the given string
1. Reverse the given string
1. Check if the given string and reversed string are equal
1. Print the result
1. End

## Program
```
REM "Write a program to check if a given string is PALINDROME"
CLS

'ask for input
INPUT "Enter a string"; s$

'remove the space from the given string
without_space$ = strip_space$(s$)

'reverse the given string
backward$ = reverse$(without_space$)

'print the result
'check if the two strings are equal
IF a$ = b$ THEN
    PRINT "It is a palindrome"
ELSE
    PRINT "It is not a palindrome"
END IF

END

'reverse the given string
FUNCTION reverse$ (s$)
    FOR i% = LEN(s$) TO 1 STEP -1
        c$ = MID$(s$, i%, 1)
        p$ = p$ + c$
    NEXT i%
    reverse$ = p$
END FUNCTION

' removes the space from a given string
FUNCTION strip_space$ (word$)

    'read the given word one character at a time
    FOR x% = 1 TO LEN(word$)
        char$ = MID$(word$, x%, 1)
        IF char$ <> " " THEN
            temp$ = temp$ + char$
        END IF
    NEXT x%

    strip_space$ = temp$
END FUNCTION
```

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

**Function**

A Function is a program that performs a task and then returns control to the calling code. When it returns control, it also returns a value to the calling code.

Example:

```
a% = 2
b% = 3

sum% = addition(a%, b%)
PRINT a%; "+"; b%; "="; sum%

FUNCTION addition(a%, b%)
    sum = a% + b%
    addition = sum 'returns the value of sum
END FUNCTION
```

**Sub Procedure**

A Sub procedure (or sub routine) performs a task and then returns control to the calling code, *but it does not return* a value to the calling code.

```
CALL addition(2, 3)

SUB addition(a%, b%)
    sum% = a% + b%
    PRINT a%; "+"; b%; "="; sum%
END SUB
``` 