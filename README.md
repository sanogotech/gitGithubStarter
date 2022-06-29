** Use git bash for  touch filename and  vim  filename 
** git init


**  type null > README.md

** git add *

** git status  #  status des ajouts et motifications

** git  commit -m  "Add README file"

*** git remote add origin https://github.com/sanogotech/gitdemosample.git
**  git push -u origin master

** git log # uniquement le log des commits

**  git  branch  # Display  only one branch  "Master"

**  git  branch  mabranch   # create new branch

**  git  checkout  mabranch  # change branche

//Switched to branch 'mabranch'

**  Change  README and  commit -add

** git log
```
$ git branch -vv
 branch  808b598 [origin/branch] Initial commit                                                                                                                         master  808b598 [origin/master] Initial 
git push -u origin branch   # ajout branche sur le remote repository
git  checkout master
git merge  mabranch # merge de mabranch vers master
```
** OU À vous de tester parmi les nombreux outils existants : vimdiff, meld, opendiff, kdiff3, tkdiff, xxdiff, tortoisemerge, gvimdiff, diffuse, ecmerge, p4merge, araxis, emerge

** git mergetool vimdiff

** git log

```
** Pour retrouver qui a modifié une ligne précise de code dans un projet

** git blame  monfichier.ext

```
