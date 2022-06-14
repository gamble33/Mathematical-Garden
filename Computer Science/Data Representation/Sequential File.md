#CompSci 

# Sequential File
---
A file that stores [[Record Data Type|records]] that are ordered.

There are two cases for when a new record is stored in a sequential file. Either
* The record is appended to the file and left to be sorted/organised later.
* Each record in the file is read sequentially and written to a new sequential file until the appropriate position for the new record is found. Then, the record is written to the new file. Finally, the files following the order of the new record are written