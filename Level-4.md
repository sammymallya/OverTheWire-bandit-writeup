# Level 4 → Level 5

### 🎯 Goal:
The password is stored in the only human-readable file in the 'inhere' directory.

### 🛠️ Steps:
```bash
ssh bandit4@bandit.labs.overthewire.org -p 2220
```
```bash
Password: (password from Level 3)
```
first I used ls -a to see all content in my current working directory:
```bash
ls -a
```
and then next i traveled into the inhere directory using :
```bash
cd inhere
```
```bash
file *  # Check file types
```
This doesnt work because all file names begin with a hyphen (-) so then the file -file00 command is interpreted as run file command with the option file00 which causes this error as it is not a valid option: 
```bash
file: Cannot open `ile00' (No such file or directory)
file: Cannot open `ile01' (No such file or directory)
file: Cannot open `ile02' (No such file or directory)
file: Cannot open `ile03' (No such file or directory)
file: Cannot open `ile04' (No such file or directory)
file: Cannot open `ile05' (No such file or directory)
file: Cannot open `ile06' (No such file or directory)
file: Cannot open `ile07' (No such file or directory)
file: Cannot open `ile08' (No such file or directory)
file: Cannot open `ile09' (No such file or directory)
```
so to clarify that the name following - is not an option but a filename, we use -- separator that tells that all subsequent arguments are filenames:
```bash
file -- *
```
and now that we got the data type of all files, and we are looking for ASCII datatype file, we find it and use cat to open it and get the password to the next level
```bash
cat -- <human-readable-file>  # Replace with the actual filename
#we use -- since filename starts with -
```

---
_Password output is omitted for security and learning integrity._
