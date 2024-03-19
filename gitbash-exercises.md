# Git-Exercises-Write-ups

## Master
using the command git push we can push the file along with the committed message

## Commit-one-file
I only want to add certain changes to A. I add A.txt, stage it and then write my git commit and then verify

```
git checkout
git add A.txt
git commit -m "commit only for A"
git push
```

## Commit-one-file-staged
use git status to see what files are staged, use git reset to clear the stage, use git add to add one specific file, use git commit followed by git push

```
git status
git reset
git add A.txt
git commit -m "commit2"
git push
```


## Chase-branch
git checkout to verify if we are on the chase-branch, use the command git merge escaped to make chase-branch to point to the same commit as the escaped branch.

```
git merge escaped
```


## Ignore-them
create a .gitignore file and add all the extensions you want to ignore, as specified: *.exe, *.o, *.jar, libraries/
add your file to the stage and add your commits and verify.

```
touch .gitignore
git add
git commit -m "ignore"
```

## Merge-conflict
when merging the branches, there was a conflict in equation.txt.
open the file, use 2+3=5 as your equation, add file then commit and then merge branches

```
git merge another-piece-of-work
open file.txt
git add equation.txt
git commit -m "commit"
```




## Save-your-work
save your work without committing it using git stash, remove your bug and commit the changes. recover your previous changes and commit.

```
git stash
cat bug.txt
git add .
git commit -m “bug fixed”
git stash pop
cat bug.txt
git add .
git commit -m “done”
```

## Change-branch-history

by using the command below, the exercise can be completed

```
git rebase hot-bugfix
```

## Remove-ignored
we can remove the file from working directory as well as the staging area by the command below.

```
git rm ignored.txt
git add .
git commit -m “commit”

```
## Case-sensitive-filename
we can rename the file name to a case sensitive name by the below command.

```
git mv FILE.txt file.txt
git commit -m “commit”
```

## Fix-typo
first, we have to open the file, stage it and combine the staged commits along with the previous commits into a single commit.

```
cat file.txt
git add .
git commit –amend -m “commit”
```

## Forge-date
for forging a date, we can use the command below
```
git commit –amend –no-edit –date= “1987-01-01”
```

## Fix-old-typo
start by rebasing in interactive mode, change the pick into edit for the commit where the typo is. Modify file.txt and commit it's changes using commit --amend and change your commit message to "Add Hello world". Use git rebase --continue. Resolve the merge conflict in file.txt, add it and finally commit

```
git rebase -i HEAD^^
git commit --amend
git rebase --continue
git add file.txt
```



