# Level 2 → Level 3

### 🎯 Goal:
The password is stored in a file called 'spaces in this filename'.

### 🛠️ Steps:
```bash
ssh bandit2@bandit.labs.overthewire.org -p 2220
```
```bash
Password: (password from Level 1)
```
```bash
ls
```
```bash
cat 'spaces in this filename'  # Wrap filename in quotes or double quotes as terminal sees spaces as delimiter and thus will interpret hi hello as 2 different file names in cat hi hello
```

---
_Password output is omitted for security and learning integrity._
