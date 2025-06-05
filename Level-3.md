# Level 3 → Level 4

### 🎯 Goal:
The password is stored in a hidden file in the 'inhere' directory.

### 🛠️ Steps:
```bash
ssh bandit3@bandit.labs.overthewire.org -p 2220
```
```bash
Password: (password from Level 2)
```
```bash
cd inhere
```
```bash
ls -a  # Show hidden files
```
```bash
cat .hidden  # Read the hidden file
```

---
_Password output is omitted for security and learning integrity._
