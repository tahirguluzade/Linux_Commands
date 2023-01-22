# Errors while installing or running commands

- [ ] if you get following error message while running cowsay command, the most probably it is because of non-existance environment for "cowsay" (which also shows in manual for cowsay):
```
+ echo "example"| cowsay
+ **cowsay: Could not find cowfile for 'default.cow'!**
```
#solving this issue you need to create environment for cowsay which is "COWPATH"
```
COWPATH=/usr/share/cowsay/cows
export COWPATH
``` 
        