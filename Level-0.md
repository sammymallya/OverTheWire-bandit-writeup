# Level 0 → Level 1

### 🎯 Goal:
Connect via SSH and find the password stored in a file called 'readme' in the home directory.

### 🛠️ Steps:
```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
```
```bash
Password: bandit0
```
```bash
ls
```
```bash
cat readme  # Displays the password for Level 1
```

---
_Password output is omitted for security and learning integrity._
