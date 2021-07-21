---
layout: post
title: "Check if a string is palindrome"
render_with_liquid: false
---

## Function

A Function is a program that performs a task and then returns control to the calling code. When it returns control, it also returns a value to the calling code.

Example 1:
```
a% = 2
b% = 3

remove% =subtract(a%, b%)
PRINT a%; "-"; b%; "="; remove%

FUNCTIONsubtract(a%, b%)
    remove = a% - b%
   subtract = remove 'returns the value of remove
END FUNCTION
```

Example 2:
```
REM "Find the area of a circle"

CONST PI! = 3.14152
r! = 2

area! = areaCircle(r!)
PRINT "The area of a circle with radius "; r!; "="; area!

' Area of a circle
' A = PI * r ^ 2
FUNCTION areaCircle (radius!)
    area! = PI! * radius! ^ 2
    areaCircle = area!
END FUNCTION
```

[Reference: Our GitHub](https://github.com/avecnavadita/QBASIC)