# Useful Bash aliases
I've put these in here for my own use, but copy them, use then, abuse them, and laugh at them. 

They aren't that impressive, but they save me some time.

## How to add them

To add these to your bash terminal, on _Windows_ at least follow these steps:

1. run the below command, and create the file if it doesnt exist:
```bash
    notepad ~/.bash_profile
```
2. Add the below to the top of the file:

```bash
if [ -f /etc/bash_completion ] && ! shopt -oq posix; then
     . /etc/bash_completion
fi
```

3. Add in any of the aliases you want from below.
4. Save the file and close the notepad window.
4. Close the terminal, and open it again.

It's that simple...

# The Commands


## Git Bash

```bash
# ----------------------
# Git Aliases
# ----------------------

alias g='git'
alias rebase@master='git checkout master && git pull && git checkout - && git rebase master'
alias whoops='git reset --hard HEAD && git clean -fd'
```
