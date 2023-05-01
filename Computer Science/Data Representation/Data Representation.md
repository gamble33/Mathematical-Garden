# Data Types
```ad-definition
Data types which are defined based on primitive data types are called **user defined data types**.
```

```ad-definition
A **non-composite data type** is one which can be defined without the need to reference another data type.

All primitive types are non-composite data types. Enumerated data types are examples of user-defined non-composite data types.
```

# File Organisation
Millions of people expect to be able to retrieve information from files quickly. File access must be quick. Thus, the need for file organisation. 

## Serial File Organisation
New records are appended to the end of the file. Records are stored one by one.

## Sequential File Organisation
Files are stored based in order of a key or unique identifier.

## Random File Organisation
The location of any file is found via a hashing algorithm.

# File Access
## Sequential Access
A linear search pretty much. Files are checked one after another until the required one is found.

## Direct Access
A key or hash is used as an index to access the file directly.