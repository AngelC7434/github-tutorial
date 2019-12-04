# GitHub Tutorial

_by Angel Chen_

---
## Git vs. GitHub
**git** = a programming language that allows the developer to keep snapshots of code and back-track previouse codes  

**github** = a place where coding is stored, specifically git.
Github also tracks the changes made.


---
## Initial Setup
config = shape/put together/arrage/order

Use **git config --global user.email "you@example.com"**  
  * Example: git config --global user.email "angelc7434@hstat.org"

Then type **git config --global user.name "Your Name"**  
  * Example: git config --global user.name "Angel Chen"

Do **cd** to make sure you are in the root directory after you did git config
Type in **ssh-keygen -t rsa -b 4096 -C "you@example.com"**
Then slowly press `Enter` repeatedly until you see something like
![GitHub Logo](key's-randomart.png)  
ls `-al ~/.ssh`, you should now see a file named **id_rsa.pub**  

Go to **https://github.com/settings/keys** then **New SSH Key**
1. title it ide50
2. where is says **key** paste your ssh key
3. press the green **Add** SSH key button
4. return to your cs50 IDE, type **sudo nano ~/.ssh/config** and paste...
* **`Host github.com`  
    `Hostname ssh.github.com`  
    `Port 443`**  
5. do `control`+`X` to exit then press `Y` then `ENTER`  
* `ssh -T git@github.com`  
6. **type yes, press `ENTER`**  
* you should see -> Hi "username"! You've successfully authenticated, but GitHub does not provide shell access.

---
## Repository Setup
1. Use **mkdir "name"** to create a directory  
2. Use **cd** to go into your new directory (you can create anew folders/files inside after cd, remember to cd again to edit inside)  
3. After you cd into it, use **git init** to initialize git before you start anything  
4. Edit/make changes  
5. Type **git add .**  
6. Type **git status** and make sure your newly editted file is green  
7. Type **git command -m "name the change(s)"**  
### Connect It To Your Github
1. Login to github.com
2. Press the **plus sign** at the top right hand corner
3. Press on `New repository`  
4. Name your new repository they same name you gave for your directory in your ide/local  
5. Press `Create repository`  
6. Click on SSH, **not** HTTPS  
7. Copy and paste the line that starts with **git remote add origin _link_...** onto your ide/local  
8. Then do the same thing to the line under the line that starts with **git remote add origin _link_...**


---
## Workflow & Commands  
`git status` = a command that you use to check which changes are ready to be add and committed. When you use git status after you made changes, you should see the file(s) name in which the changes are made in **green**.  

`git add .`/`git add "file name"` = puts up all the changes which are then ready to be commited.  

`git commit -m "name of the change"` = this command does the last step in saving your changes. The changes are names for backtracking in the future if necessary.  

`git push` = this command allows you to transfer your commits on your local(Ex. ide) to your remote(Ex. github)  

---
## Rolling Back Changes

Undo lastest edit/change -> `git checkout -- file-name`

Undo lastest `git add .`/`git add file-name` do `git reset HEAD file-name`

Undo lastes command, save undone changes (`git reset --soft HEAD-1`), or completely delete changes (`git reset --hard HEAD-1`)  

Undo a push -> do...  
1. `git revert "SHA`  
2. `Enter`  
3. `git reset Head^ --hard`  
4. `Enter`
5. `git push origin master`
6. `Enter`


## Collaboration
**Forking** = making a copy of a repository from someone else to your github account. This also allows you to do pull requests where you suggest a change to the original repo to the oner of the repo you forked from  

**Cloning** = makes a copy of a repo to your local repository where you have to do `git clone <url>` and cd into it  

**Pull requests** = the action of asking the owner of the original repo to accept/pull in the changes you have made to their repo after you forked it. The owner can choose to reject or accept those new edits  