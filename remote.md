# Remote repsitory
* to achieve collaboration on git projects you must interact w/remote rpositories versions of a project 
residing online or on a network. teams can also use this to push and pull data from it.


## so what we will cover is how to push and add data so you can see add to temamtes work

(owner$ cd codefellows
### codefellows$: *ls*
### 102
### codefellows$: *cd 1028
### 102$: *ls*
### pojects
### 102$: *cd pojects*
### pojects$: *ls*
### learning-journal
### pojects$: *cd learning-journal*
### learning-journal[master ?]$: *git status*
### On branch master
### Your branch is up to date with 'origin/master'.

### Untracked files:
 ### (use "git add <file>..." to include in what will be committed)

    remote

### nothing added to commit but untracked files present (use "git add" to track)
learning-journal[master ?]$)



* if you make the changes you will have to push the info to get the code to (origin master) 
### learning-journal[master ?]$ git push origin master
### Username for 'https://github.com': josephlee3454
### Password for 'https://josephlee3454@github.com':
### Everything up-to-date

*  so we pushed everything to git hub now we need to add 
learning-journal[master ?]$ git status
On branch master
Your branch is up to date with 'origin/master'.

#### Untracked files:
  #### (use "git add <file>..." to include in what will be committed)

     remote.md

#### nothing added to commit but untracked files present (use #### "git add" to track)
#### learning-journal[master ?]$: *git add remote.md*
 #### learning-journal[master +]$ *git commit*
#### Aborting commit due to empty commit message.
#### learning-journal[master +]$ *git commit -m "created remot.md/added notes"*
#### [master b8d2702] created remot.md/added notes
 #### 1 file changed, 34 insertions(+)
 #### create mode 100644 remote.md
#### learning-journal[master *]$ 

* so what we have done was add the remote.md file to our site and we made a commit so everyone knows what we did
