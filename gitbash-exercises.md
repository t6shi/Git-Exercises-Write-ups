# Git-Exercises-Write-ups

## master
using the command git push we can push the file along with the committed message

## commit-one-file
used checkout to verify my branch, used git add to add the file and then used git commit followed by git push
```
git checkout
git add A.txt
git commit -m "commit1"
git push
```

## commit-one-file-staged
use git status to see what files are staged, use git reset to clear the stage, use git add to add one specific file, use git commit followed by git push
```
git status
git reset
git add A.txt
git commit -m "commit2"
git push
```


## chase-branch
git checkout to verify if we are on the chase-branch, use the command git merge escaped to make chase-branch to point to the same commit as the escaped branch.
```
git merge escaped
```


## ignore-them
create a .gitignore file and add all the extensions you want to ignore, as specified: *.exe, *.o, *.jar, libraries/
```
touch .gitignore
git add
git commit -m "ignore"
```

## merge-conflict
edit your .txt file and then merge. type in the correct equation "2+3=5" and run. add your equation.txt and commit.
```
git merge another-piece-of-work
open file.txt
git add equation.txt
git commit -m "commit"
```




## save-your-work
save your work without committing it using git stash, remove your bug and commit the changes. recover your previous changes and commit.
```
git stash
cat bug.txt
git add .
git commit -m “commit1”
git stash pop
cat bug.txt
git add .
git commit -m “commit2”
```

## change-branch-history

by using the command below, the exercise can be completed
```
git rebase hot-bugfix
```

## remove-ignored
we can remove the file from working directory as well as the staging area by the command below.
```
git rm ignored.txt
git add .
git commit -m “commit”

```
## case-sensitive-filename
we can rename the file name to a case sensitive name by the below command.
```
git mv FILE.txt file.txt
git commit -m “commit”
```

## fix-typo
first, we have to open the file, stage it and combine the staged commits along with the previous commits into a single commit.
```
cat file.txt
git add .
git commit –amend -m “commit”
```

## forge-date
for forging a date, we can use the command below
```
git commit –amend –no-edit –date= “1987-01-01”
```

# Fix-old-typo
start by rebasing in interactive mode, open in editor, use the command git add after adding your changes, fix your old typo and resolve the merge clash.
```
git rebase -i
vim file.txt
git add 
git commit –amend
git rebase –continue
vim file.txt
git add 
git commit -m “comment”
```



