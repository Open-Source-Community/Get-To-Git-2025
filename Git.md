## Definitions
- **Root commit** -> initial comment
- **Branch** -> arrangements of comments By default(master)

## Configurations

To create config
```bash
git config --global user.name "hadeer"
git config --global user.email "hadeer"
git config --global core.editor "nano" # or add your Fav Text editor

# to see all config
git config --list
```

## Initializing Repo
```bash

git init #initialize repo, do it in folder to create a repo
# it creates .git directory, the place where git sotre all your commits and changes

```

## Commit
```bash
git status # status of files
git status -s # summarize status for every file
git add file.txt # add file to stage
git add <filename> # grouping files like this(*,f*,*txt) or using `.` to add all files

git commit -m "message" -> make version 
git commit -am "message" # TODO: Description
fit commit --amend # TODO: Description
```
## Undoing
```bash
git rm --cached fileName # TODO: Description

git restore filename # TODO: Description
git restore --staged file #to unstage file

git reset --soft <Hash> # TODO: Description

git reset  <Hash> # TODO: Description

git reflog # TODO: Description

```
## viewing History
```bash
git log # see history
git log --oneline # summarize each commit
git log --oneline file.txt # see commits for specific file
git log --oneline -n number # TODO: Description
git log --oneline --graph # list a clear path for every branch
git log --oneline --decorate --graph --all # TODO: Description
```

## differences
```bash
git diff # display changes of files (before stage)
git diff --staged # display changes of files(that are in stage area)

git diff SHA1..SHA1 # TODO: Description
gi diff SHA..HEAD # TODO: Description
git show SHA1 # TODO: Description

```

## Git Branching

```bash
git branch branchName # create new branch
git branch # to show branches
git switch branchName # move to the branch

# or you can use checkout to switch
git checkout branchName
git checkout -b branchName <startPoint> # TODO: Description
```


## Merging
```bash
git merge branchName # merge branch, NOTE (you should be at branch that you to merge in)
```
- There is three types of Merging based on changes that done in commit at both two branches.

**1. Fast Forward Merge**
 - it happens when there is no new commit in master (or what you merge in).
 - In this case, Git just move the master branch pointer to point to the last commit in other branch

 ![alt text](images/fastF.png)

```bash
git branch --merged # TODO: Description
git branch --no-merged # TODO: Description

git branch -d branchName # TODO: Description
```

### Divergent History

![[Pasted image 20231203092011.png]]

```
git merge testing
```

>to graph logs | git log --oneline --decorate --graph --all



### Working With Remote

##### Clone
Take a copy from original project directly and edit on the copy, then push or pull(fetch)

```
 git clone ./fileName/ writeName
 -> git clone then(url)

git remote -> if origin that mean this repo from remote repo

git remote -v -> to now where the remote-repo and from where this clone was taken

git branch -r > branches from origing

git remote add <url> writeName -> more than one remote

git fetch origin(of you have more one remote git name)   ->to git all updates from remote repo
git merge -> merge updating

git status -> to know if you update or not and differneces of computer
```

`making branch in local repo and put in it`
⇾ git push -u `name of branch`
⇾ git branch --v

>making alias
>alias name=command
>alias graph="git log --online --all --graph --decorate"

⇾ **push**
```
 
```

### GitHub
**Push local repo to GitHub**
- First (HTTPS)
```
git remote add origin url
git branch -M main -> to rename master branch (from master to main)
git push -u origin main(name of branch)-> to push repo




```
- Second (SSH)


delete repo 
rm -rf .git/
```
