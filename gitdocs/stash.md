## to stash files
- git stash 

## to add name to the stash
- git stash push -m "name of stash"

## to add name to the stash and choose files
- git stash push -m "nsme of stash" -- <file1> <file2>

## stashes only the unstaged changes and keeps the staged changes
- git stash --keep-index 

## to retrive the stash (recently)
- git stash pop

## to retrive specific stash
- git stash pop stash@{0}

## lsit all stashes
- git stash list

## list the names of the files in a stash
- git stash show --name-only stash@{n}

## The command displays the changes of the stash entry
- git stash show -p stash@{n} 
