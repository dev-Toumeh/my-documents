### This shows the differences between the current state of the file and the last commit. If you want to see changes that have already been staged for commit, add the --staged option:
- git diff --staged <file_path>

### To remove cached files from Gitignore
```bash
git rm -r --cached .
```
### to see commits log
```bash
git log
```
### to see repository’s Files
```bash
git ls-files
```

### fix gitignore tracking problem
```bash
# Adding point to .gitignore could lead to a problem recognizing the files or folders, if you want to add files start with src instead of ./src
# WARNING: First commit or stash your current changes, or you will lose them.
git rm -r --cached 
git add .
git commit -m "fixed untracked files"
```
### undo File changes
    git checkout -- <file>



## Git Remote
### lists all the remote connections you have to other repositories along with the URLs
```bash
git remote -v 
```
### add remote repository 
```bash
git remote add repository-name git@gitremote-service.com:myremote-repository.git
```
### fetch and merge the content from the existing repository into local repository.
```bash
git pull repository-name branch-name --allow-unrelated-histories
```
### push to not default remote branch
```bash
# adding -u mean this repository will be the default repository in future pushes
git push -u repository-name branch-name
```

### remove unwanted commints from the remote
  hints
  - you need to know which commit you want to move back to it "HEAD~2 or HEAD~3 etc"
  - the branch should have remote tracking branch associated with it
  - git reset --hard HEAD~<number-of-commit>
  - git push origin <branch-name> --force 







