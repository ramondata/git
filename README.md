
```
       _ _                                                   _   _ _              _       _             __               
      (_) |                                                 | | | (_)            (_)     | |           / _|              
  __ _ _| |_    ___ ___  _ __ ___  _ __ ___   __ _ _ __   __| | | |_ _ __   ___   _ _ __ | |_ ___ _ __| |_ __ _  ___ ___ 
 / _` | | __|  / __/ _ \| '_ ` _ \| '_ ` _ \ / _` | '_ \ / _` | | | | '_ \ / _ \ | | '_ \| __/ _ \ '__|  _/ _` |/ __/ _ \
| (_| | | |_  | (_| (_) | | | | | | | | | | | (_| | | | | (_| | | | | | | |  __/ | | | | | ||  __/ |  | || (_| | (_|  __/
 \__, |_|\__|  \___\___/|_| |_| |_|_| |_| |_|\__,_|_| |_|\__,_| |_|_|_| |_|\___| |_|_| |_|\__\___|_|  |_| \__,_|\___\___|
  __/ |                                                                                                                  
 |___/  
```

tl,dr:
# *DRAFT YET*


### Good resume and practices about git cli

## Configurations
- [x] git config --global user.name "my name"
- [x] git config --global user.email myemail@duckpretty.com
- [x] git config --local user.name "my name"
- [x] git config --local user.email myemail@duckpretty.com

## First acess in repository
- [x] git init 
- [x] git clone

## Branch

- [x] watch a list with local branches
```
git branch
```
or
````
git branch --list
````
- [x] watch a list with remote branches
```
git branch -r
```
or
```
git branch --remotes
```
- [x] watch a list with remote and local branches
````
git branch -a
````
or
````
git branch --all
````
- [x] git branch -d del-branch or git branch -D del-branch

## set up a default remote and branch for pull/push
- [x] git push --set-upstream remote branch
- [x] git branch --set-upstream-to=remote/branch 

## Change place
- [x] git checkout other-branch 
- [x] git checkout -b new-branch
- [x] git checkout id-commit --> access a commit to see the historic code --> for back to current commit: git checkout <branch-name>

## Remote server
- [x] git remote -v
- [x] git remote add xxx yyy
- [x] git remote remove/rm xxx
- [x] delete a remote branch ??? 

## Upload to the server
- [x] git push --set-upstream origin branch
- [x] git push

## Follow changed files
- [x] git status

## Follow historic changes commits
- [x] git log --oneline
- [x] git log --graph

## Compare and watch files changes 
- [x] git diff HEAD file --> compare with last commited changes before git add files
- [x] git show --' 
- [x] git diff --cached --> used after git add files
- [x] git diff tag-name..other-tag-name --> amazing way to compare difference between code versions(fyi: the tag contain the flag about last change)

## Manager Stashes
- [x] git stash push or git stash
- [x] git stash list --> all changed stashed
- [x] git stash show --> changes from currently branch
- [x] git stash apply  or git stash apply 0(or stash@{0})
- [x] git stash drop  or git stash drop 0
- [x] git stash pop or git stash pop 0(or stash@{0}) --> similiar git stash apply stash@{0} + git stash drop stash@{0} 
- [x] git stash branch new-branch-name stash@{0}(or just 0) --> keep clean currently branch and create a new branch apply the changes from stash
- [x] git stash clear --> drop all stashes

## Insert changed files by saved 
- [x] git add file1, file2, ...
- [x] git add . --> added everything changed

## Save changed files into a commit
- [x] git commit or git commit -m "message"
- [x] git commit -a -m "message commit" --> same thing which git add . + git commit -m "message"

## Throw changes from a branch in another branch
- [x] git merge branch-copy 
- [x] open a pull request to approve your merge

## tags
- [x] git tag or git tag -l(i.e. --list) --> list of tags in repo
- [x] git tag -n(i.e. --num) --> list tags with message or last commit associated
- [x] git tag -d(i.e. --delete)name-tag
- [x] git tag name-tag --> made a new tag for you
- [x] git tag -a(i.e. --annotate) name-tag -m(i.e. message) "message for your tag here"
       
## Reset commits
- [x] git reset HEAD~ or git reset HEAD^ --> reset last commit
- [x] git reset HEAD~x --> To back by x commit before HEAD(HEAD is a pointer for actualy branch and commit)
       
## Hooks
- [x] commit-msg: good pattern to organize commits message
> mv .git/hooks/commit-msg.sample .git/hooks/commit-msg
       
> make your regex reding .git/COMMIT_EDITMSG --> where your messagem commit was saved
       
> remember apply exit 1 and a error message case pattern commit is wrong
       
> when you push commit, your commit-msg for git hooks will be available for everybody that get your repo branch
