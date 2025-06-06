So in this level, inside the inhere directory there are multiple sub directories named as maybehere00 till maybehere09 for eg. We have been told to find a file that is human readable (so ASCII) datatype, and it is given that the file is 1033 bytes long and is not executable.\
Now instead of going inside each maybe subdirectory and using ls -a and file * to find a file matching our criteria, we will use the find command which does exactly this:
```bash
cd inhere
```
```bash
find . -type f -size 1033c ! -executable
```
lets break this down into parts for us to understand:
* find is a command that finds files or directories which match the conditions given.
* '.' tells the find to search in its current working directory and the find function also recursively travels to each subdirectory and matches the condition
* -type f specifies that we are looking for a file and not special or hidden files or directories
* -size 1033c specifies that we want a file which has a size of 1033 bytes (c stands for a byte so 1033c is 1033 bytes)
* ! -executable was used since it is specified that we dont want a file that is executable which means it shouldnt be a program or have a executable code in it so we use LOGICAL NOT operator ! to flip the -executable into ! -executable which means not executable

from this we get the path to that file as output, and then we navigate to it using cd and open it using cat:
```bash
  cd <put file path you got as output in previous query>
  cat -- filename # we use -- as the file might start with special character
  ```
