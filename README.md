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
alias gph='git push'
alias gphf='git push -f'
alias gpl='git pull'
alias g+='git add .'
alias g-='git reset'
alias g--='git reset --hard'

#Rebase your current branch from master
alias rebase@current='git checkout master && git pull && git checkout - && git rebase master'

#Rebase the master branch from current
alias rebase@master='git checkout master && git pull && git rebase - && git push && git checkout -'

#You screwed up - clean it up and try again
alias whoops='git reset --hard HEAD && git clean -fd'

#Remove all local branches, that are no longer on the remote server
alias cleanbranches="git branch -r | awk '{print $1}' | egrep -v -f /dev/fd/0 <(git branch -vv | grep origin) | awk '{print $1}' | xargs git branch -d"
```

