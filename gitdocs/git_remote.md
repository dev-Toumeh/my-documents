## add new remote:
git remote add "origin" git@github.com:User/UserRepo.git

## change url of an existing remote repository:
git remote set-url "origin" git@github.com:User/UserRepo.git

## push your code to the master branch of the remote repository defined with "origin"
git push -u origin main

## -u (or --set-upstream):
Sets the default tracking relationship between your local branch (e.g., main)
and the remote branch (origin/main). After this, you can simply use git push or
git pull without specifying the remote and branch explicitly.
 Example: (git push -u origin main)

## the best solution i found
1- git init
2- git commit -m "init commit"
3- git remote add "origin" git@github.com:User/remote-repo.git
4- git push --force origin local-branch-name:main
