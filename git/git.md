### To use changes from one Git branch in another branch while keeping the current branch unchanged,
```bash
# Stash your changes in the current branch:
git stash
```
```bash
#Checkout to the target branch where you want to use the changes:
git checkout target-branch-name
```
```bash
#Apply the stashed changes to the target branch:
git stash pop
```
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
# WARNING: First commit or stash your current changes, or you will lose them.
git rm -r --cached .
git add .
git commit -m "fixed untracked files"
```

<br></br>

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