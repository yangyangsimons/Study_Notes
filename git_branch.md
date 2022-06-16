# Introduce to git branch operation
## 1. What is an branch? 
Sometimes there may be multiple people developing functions or fixing bugs for a same software at the same time, there may be multiple Release versions, and each version needs to be maintained.
Git's `branch` function can support the development and version management of multiple functions at the same time.
One branch is not affected by other branches, so modification can be made in the same database at the same time.

## 2. Create a branch
use the command `git branch` to create a new branch
```
git branch <branch name>
```
## 3. Query branch
use `git branch` command without any parameter, it will return all branches for this git repository, the one has a symbol `*` is the current branch
```
% git branch
* <branch name>
<brnach name2>
```
## 4. swtich to a branch and push from this branch
use command `git branch <branch filename>` swtich to a branch and then use `git add` and `git commit` and then push.
```
git branch <branch filename>
...
git add .
git commit -v
git push -u origin <branch filename>
```

