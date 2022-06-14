#CompSci 

# Direct-Access Files
---
A file, with which a key can be used to directly access any record within it.

Direct-access files can be achieved by:
- storing a [[Sequential File|sequential file]] alongside it. The sequential file stores record, each with two fields. The first field stores the key and the second stores a value for the position of the respective [[Record Data Type|record]] in the main file.
- using a hashing algorithm. The hash of the key of any record should give the position of that record in the file. 

