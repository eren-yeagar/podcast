## Git Hidden Folder

There is a hidden folder called `.git` which tells you that our project is a git repo.

If we wanted to create a git repo in a new project we create
the folder and then initialize the repo using `git init`

```
mkdir /workspace/tmp/new-project
cd /workspace/tmp/new-project
git init 
touch Readme.md
code Readme.md
git status # shows status of each file
git add Readme.md
# make changes to readme.md
git commit  -m "add readme file"

```

## cloning

we can clone in 3 ways https, ssh, github cli

Since we are using github codespaces, we create a temporary directory in our workspace

```sh
mkdir /workspace/tmp
cd /workspace/tmp

git clone https://github.com/eren-yeagar/podcast.git
```
## commits

when we want to commit code we can write git commit which will open up the commit message in the editor  of choice.

```sh
git commit

```



## branches

## remotes

## stashing

## merging

## add

when we want to stage the changes that will be included in the commit. We can use the . to add all possible files.

```
git add Readme.md
git add .


```
## status

git status will shows us what files will or will not be commited

```
git status

```

## Reset

Reset allows you to move staged changes to unsatged.
This is useful when you want to revert all files not to be not commited

```
git add .
git reset

```

> git reset will revert a git add
