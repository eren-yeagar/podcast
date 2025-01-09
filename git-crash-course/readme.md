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
````
### HTTPS

```sh
git clone https://github.com/eren-yeagar/podcast.git
```

> You'll need to generate a Personal Acess Token (PAT) 
https://github.com/settings/token

You will use the PAT as your login 

- Give it access to Contents for Commits 

### SSH

```ssh
git clone git@github.com:eren-yeagar/podcast.git

cd folder_name
```
we wil need to create our own ssh rsa key pair

```sh
ssh-keygen -t rsa
```

```sh
eval `ssh-agent`
ssh-add /home/andrew/.ssh/alt-github_id_rsa
```

we can test our connection here :
```
ssh -T git@github.com
```
For WSL users and if you create a non default key you might need to add it

### Github cli

install the cli

eg. linux (ubuntu)
```sh

```

## commits

when we want to commit code we can write git commit which will open up the commit message in the editor  of choice.

```sh
git commit
```

Set the global editor

```
git config --global core.editor emacs
```


## branches

List of branches

```
git branch
```

create new branch

```
git branch branch-name
```

checkou the branch

```
git checkout branch-name
```


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
## Gitconfig file

The gitconfig file is what stores your global config such as email, name, editor.

showing contents of our .gitconfig file
```
git config --list
```
When you first install your git on your machine, you are supposed to set up your name and email

```sh
git config --global user.name "Sriram Merugu"
git config --global user.email example@gmail.com
```
## Log

git log will show recent git commits to the git tree 

## Push



## Reset

Reset allows you to move staged changes to unsatged.
This is useful when you want to revert all files not to be not commited

```
git add .
git reset

```

> git reset will revert a git add

