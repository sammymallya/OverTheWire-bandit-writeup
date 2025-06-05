# Level 1 → Level 2

### 🎯 Goal:
The password for the next level is stored in a file called '-' located in the home directory.

### 🛠️ Steps:
```bash
ssh bandit1@bandit.labs.overthewire.org -p 2220
```
```bash
Password: (password from Level 0)
```
```bash
ls
```
```bash
cat ./-  # Use './-' to avoid interpreting '-' as a flag
```

---
_Password output is omitted for security and learning integrity._
