# Files
## Opening File
```fortran
OPENFILE ThisFile FOR READ
```
## Closing File
```fortran
CLOSEFILE ThisFile
```

## Reading File
```fortran
DECLARE ThisLine : STRING

IF EOF(ThisFile) THEN
	OUTPUT "Warning: File is Empty!"
ENDIF

READFILE ThisFile, ThisLine
```

# Weird Things
* You probably can't return out of *procedures*