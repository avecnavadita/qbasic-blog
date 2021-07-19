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
1. Print the result
1. End

```
REM "Write a program to check if a given string is PALINDROME"

'ask for input
INPUT "Enter a string"; s$

'remove the space from the given string
without_space$ = strip_space$(s$)
PRINT without_space$

'reverse the given string
backward$ = reverse$(without_space$)
PRINT backward$

CALL print_result(without_space$, backward$)


'print the result
SUB print_result (a$, b$)
    'check if the two strings are equal
    IF a$ = b$ THEN

        PRINT "It is a palindrome"

    ELSE
        PRINT "It is not a palindrome"

    END IF
END SUB
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

<!-- **MID$ :**

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

[Reference: Our GitHub](https://github.com/avecnavadita/QBASIC) -->

**Function Procedure**

A Function procedure is a series of Visual Basic statements enclosed by the Function and End Function statements. The Function procedure performs a task and then returns control to the calling code. When it returns control, it also returns a value to the calling code.

**Sub Procedure**

A Sub procedure is a series of Visual Basic statements enclosed by the Sub and End Sub statements. The Sub procedure performs a task and then returns control to the calling code, but it does not return a value to the calling code.