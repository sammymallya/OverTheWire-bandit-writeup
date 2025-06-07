So this level was extremely interesting as it said that the file existed somewhere on the server, was 33 bytes long, owned by bandit7 and owned by group bandit6, and using ls -a as usual gave no useful output as shown:
```bash
.  ..  .bash_logout  .bashrc  .profile
```
On searching online, I learnt that file is on the server doesn't mean I have to initiate a new connection online to some other link as I had originally thought, but it meant that the file existed somewhere on the Bandit Virtual system's storage!
so we have to use the find function to search the whole machine as shown:
```bash
find / -type f -size 33c -user bandit7 -group bandit6 2</dev/null
```
Let's break this code down for our understanding:
* find is the command used to look for particular files
* / specifies that we want to search the whole system
* -user is used to specify the owner of the file
* -group is used to specify the group which owns the file
* the last part 2</dev/null is used to create a blackhole computer of sorts where all the (read) permission denied error logs go so that they dont crowd our output in our terminal and keep it clean.
* this gives us the path to the file and the file name, we use cd to travel to that path and then use cat to open it, getting our password for the next level
  
