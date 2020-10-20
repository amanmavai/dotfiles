
```bash
// First thing to do is to setup your name and email in git
 $ git config --global user.name "Aman Mavai"
 $ git config --global user.email "amanmavai@gmail.com"
 
 $ git config --global user.name (check the name)
 $ git config --global user.email (check the email)
 
 // Second thing is to open local/global git config (its better to setup global git config for alias)
 $ git config -e  # to open local repo config
 $ git config --global -e # to open global config
 
 // ALIAS (config file format)
[alias]
    # Shortening aliases
    c = commit
    co = checkout
    cob = checkout -b
    cm = !git add -A && git commit -m
    p = push
    ba = branch -a
    bd = branch -d
    bD = branch -D
    dc = diff --cached
    
    # Sometimes, I just want to save my work in a commit without having to think of a commit message
    save = !git add -A && git commit -m 'SAVEPOINT' 
    
    # When I return to work, I’ll just use git undo which resets the previous commit, 
    # but keeps all the changes from that commit in the working directory.
    undo = reset HEAD~1 --mixed
    
    # This commits everything in my working directory and then does a hard reset to remove that commit. 
    # The nice thing is, the commit is still there, but it’s just unreachable.
    wipe = !git add -A && git commit -qm 'WIPE SAVEPOINT' && git reset HEAD~1 --hard
 
```
