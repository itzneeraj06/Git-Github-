# Git & GitHub Notes 
* git software h or GitHub service.
* yeh version control system hai jo files ko track krta hai
* matlab software ke updates ko checkpoint me divide kr deta h jisse pichle update pr ja skte hai 
* they don’t call it a folder, they call it a repository
* timeline X  branch √ (sabka apna alg alg bolne ka tarika hai).
  
```git status```
status command se check kr skte h ki git me track h ki ni folder ka
init short form of initialisation is command se repo ko initailize krte hai.

```git init```
init krne se files track hona start hoti hai.

**Flow** 
### Write -> Add -> Commit

`Git init` -> add code in stage but not commit.

`Git commit -m` -> stage code commit into repo.

`add .` dot se saari files stage ho jaati h. commit yeh karne se file repo me chale jaati h 
syntax `git commit -m "message"`
(new file bne ya fir existing file me change krne pr pahle add karke stage area me lana pdega fir usko commit krke repo me send krna pdega)

`git log` yeh command se saare commit ki info mil jati h or kisne commit kra woh bhi 
or `git log --oneline` use krne se short me aa jaati h details 

###### .gitignore 
is file me jis bhi file ka name rahta h woh untracked rahti hai that means koi confidential file ho like .env toh woh upload na ho  
###### .gitkeep 
yeh file yadi empty folder ko git me commit krna h toh isliye banate h

### Branches
* yeh kindoff timeline hoti h
  
`git branch` - This command lists all the branches in the current repository.
`git branch bug-fix` - This command creates a new branch called bug-fix.
`git switch bug-fix` - This command switches to the bug-fix branch.
`git log` - This command shows the commit history for the current branch.
`git switch master` - This command switches to the master branch.
`git switch -c dark-mode` - This command creates a new branch called dark-mode. the -c flag is used to create a new branch.
`git checkout orange-mode` - This command switches to the orange-mode branch

(img not found) 
black wali main branch h or baki saari branches h  
git branch isse current branch pta chalti h 
git branch name >>> isse new branch bn jaati h 
git switch branchname  isss branch change ho jati h 
git checkout yeh automatically create nhi krta h new branch
git branch -d branchname 

**Head yeh current branch ko point krta h**

yeh main branch me kisi diffrent branch ka code add karta hai
`git merge temp` 
other branch ka work main me merge krna ho toh git merge branchname (pahle main branch pr aana pdega )
`git merge bug-fix` - This command merges the **bug-fix** branch into the **main** branch.

merge krne me **Conflicts** aate hai mtlb yadi do alg alg branch me ek file pr changes kiye ho or merge kr rhe ho 
toh ko sa change main branch pr save hoga 
isko manually solve krna pdta h 

for rename branch `git branch -m <old-branch-name> <new-branch-name>`
for delete branch `git branch -d <branch-name>`

**rebase** yadi mene ek branch banayi hai or uspr kaam kiya h usi ke sath mene ya kisi or ne main branch pr bhi kaam kiya h or woh changes meko meri branch me bhi chaiye usi ke liye hi rebase use kiya h 
yha mene merge nhi kiya h bss rebase change kiya h 
(use to change base of branch)

Recover lost commits or changes
`git reflog <commit-hash>` `git reset --hard <commitid>` yadi kuch glt commit ho jaye toh commit revert krne ke liye 

### GitHub ka commands
git branch -M main (yha master branch ko rename kra h main)
remote url setting: `git remote -v` (to check upload or download connection) `git remote add origin "htts://github.com/path"`
* yeh command se remote location pr.ek.branch bn jayegi origin name se

upstream ka matlab jb bhi main pr koi push ho automatically origin(GitHub) pr bhi push ho jaaye 
-U se bhi yhi hota h upstream set
