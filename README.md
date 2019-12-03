# GitHub Tutorial

_by Angel Chen_

---
## Git vs. GitHub
* Git = a programming language that allows the developer to keep snapshots of code and back-track previous codes  
* Github = a place where coding is stored, specifically git. Github also tracks the changes made.


---
## Initial Setup

config = shape/put together/arrage/order

Use **git config --global user.email "you@example.com"**
Example: git config --global user.email "angelc7434@hstat.org"

Then type **git config --global user.name "Your Name"**
Example: git config --global user.name "Angel Chen"

Do **cd** to make sure you are in the root directory after you did git config
Type in **ssh-keygen -t rsa -b 4096 -C "you@example.com"**
Then slowly press **Enter** repeatedly until you see something like
![GitHub Logo](key's-randomart.png)  
**to get all steps for setup click this link: [https://github.com/hstatsep/ide50]**
---
## Repository Setup



---
## Workflow & Commands
1. Use **mkdir "name"** to create a directory  
2. Use **cd** to go into your new directory (you can create anew folders/files inside after cd, remember to cd again to edit inside)  
3. After you cd into it, use **git init** to initialize git before you start anything  
4. Edit/make changes  
5. Type **git add .**  
6. Type **git status** and make sure your newly editted file is green  
7. Type **git command -m "name the change(s)"**


---
## Rolling Back Changes