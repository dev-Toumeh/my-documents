### To remove cached file
    git rm -r --cached <file name>

### to see commits log
    git log

### to see repository’s Files
    git ls-files

### undo File changes
    git checkout -- <file>

### fetch and merge the content from the existing repository into local repository.
    git pull repository-name branch-name --allow-unrelated-histories

### push to not default remote branches
#### adding -u mean this repository will be the default repository in future pushes
    git push -u repository-name branch-name

### remove unwanted commits from the remote
- you need to know which commit you want to move back to it "HEAD~2 or HEAD~3 etc"
- the branch should have remote tracking branch associated with it
    git reset --hard HEAD~<number-of-commit>
    git push origin <branch-name> --force 

### edit the last commit:Git
    git commit --amend --no-edit

#### if you already pushed and you want to replace the remote commit add -f
    git push --force

### push local branch to the repository and create remote branch based on it
    git push -u origin <local-branch-name>

### To clone all branches of a repository-name
    git clone --bare <repository_url>
    git fetch --all

### to see the differences between the current state of the file and the last commit.
- If you want to see changes that have already been staged for commit, add the --staged option:
    git diff <file_path>
