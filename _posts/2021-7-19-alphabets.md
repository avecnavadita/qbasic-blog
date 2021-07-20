---
layout: post
title: "Print alphabets with their ASCII CODE"
---

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

END
```
