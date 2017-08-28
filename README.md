Git cheat sheet
=======================================
- [Resources](#resources)
- [Installation](#installation)
- [Snapshotting](#snapshotting)
- [Backtracking](#backtracking)
- [Branching and merging](#branching-and-merging)
- [Working with remotes](#working-with-remotes)



Resources
---------------------------------------

- [Interactive tutorial](https://try.github.io/levels/1/challenges/1)
- [Git reference book](https://git-scm.com/book/en/v2)


Installation
---------------------------------------

Download from here: [http://git-scm.com/download/]([http://git-scm.com/download/)

Add `/usr/local/bin` to your $PATH environment variable if not already present.  For mac open `~/.bash_profile` and this line to the file:

```
export PATH=$PATH:/usr/local/bin
```

Confirm installation:
```bash
$  git --version
```
Set your name:
```bash
$ git config --global user.name “First Last"
```
Set email: 
```bash
$ git config --global user.email "your_email@example.com"
```

Snapshotting
---------------------------------------

Create a repository in an existing directory:

`git init`


Stage individual files:

`git add filename`


Stage everything:

`git add --all`


Check status of staging area compared to code in working directory:

`git status`


Record a snapshot of the files and open a vim editor to write commit message:

`git commit`


Write a commit message from the command line:

`git commit -m “message”`


Untrack a file and delete it from the working directory:

`git rm filename`


Untrack a file without deleting:

`git rm --cached filename`


Untrack all files in a directory:

`git rm --cached -r directoryName`


Remove a file from staging:

`git reset HEAD fileName`


Go to a previous commit:

`git checkout commit#`


Create a branch of a previous commit:

`git checkout -b branchName commit#`


Backtracking
---------------------------------------

Revert to a previous commit:

`git reset commit#`


Unstage files and undo changes since last commit:

`git reset --hard commit#`


Discard changes in the working directory:

`git checkout HEAD filename`


Unstage file changes in staging area:

`git reset HEAD filename`


Branching and merging
---------------------------------------

Show branches:

`git branch`


Create a new branch:

`git branch branchName`


Switch branch:

`git checkout branchName`


Create branch and change to it:

`git checkout -b branchName`


Delete a local branch:

`git branch -d branchName`


Merge another branch into current working branch:

`git merge branchName`


Working with remotes
---------------------------------------

Copy an existing repository:

`get clone urlOfRepository`
 

https clone - requires authentication by username and password

`git clone https://github.com/username/reponame.git`


ssh clone -requires authentication by ssh keys

`git clone git@github.com:username/reponame.git`

 
Show the name of the remote repository:

`git remote`


Show the name and url of the remote:
 
`git remote -v`


Show information about the remote repository (i.e. urls, tracking etc)

`git remote show remoteName`


Add a remote repository:

`git remote add remoteName url`

Example: `git remote add origin https://github.com/username/reponame.git`


Rename a remote:

`git remote rename originalName newName`


Update a remote’s url:

`git remote set-url remoteName url`

Example:` git remote set-url origin git@github.com/username/repo_name.git`


Remove a remote:

`git remote rm remote_name`


Pull data to local repository:

`git fetch remote_name`


Fetch data from remote server and merge with working branch:

`git pull`


Deploy changes to server: 

`git push remote_name branch_name`

Example: `git push -u origin master`



