## to stash files
- git stash 

## to add name to the stash
- git stash save "name"

## to add name to the stash and choose files
- git stash push -m "Your custom message" -- <file1> <file2>

## to retrive the stash (recently)
- git stash pop

## to retrive specific stash
- git stash pop stash@{0}

## lsit all stashes
- git stash list
