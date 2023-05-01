# Pseudocode
## Files
Example, you're given a text file with the name LogFile and it must be written to.
```fortran
CONSTANT LogFile = "LogFile"

OPENFILE LogFile FOR APPEND

WRITEFILE (LogFile, "Whatever you want to write to it")

CLOSEFILE LogFile
```

### Opening File
```fortran
OPENFILE ThisFile FOR READ
```

```fortran
OPENFILE ThisFile FOR WRITE
```

```fortran
OPENFILE ThisFile FOR APPEND
```
### Closing File
```fortran
CLOSEFILE ThisFile
```

### Reading File
```fortran
DECLARE ThisLine : STRING

IF EOF(ThisFile) THEN
	OUTPUT "Warning: File is Empty!"
ENDIF

READFILE ThisFile, ThisLine
```


## 2D Arrays
```fortran
arr[i, j]
```


# Weird Things
* You probably can't return out of *procedures*