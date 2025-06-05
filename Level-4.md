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
```bash
cd inhere
```
```bash
file *  # Check file types
```
```bash
cat <human-readable-file>  # Replace with the actual filename
```

---
_Password output is omitted for security and learning integrity._
