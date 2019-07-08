git cmds
===

// git config
```shell
git config --list
```

// getting clone of existing repo
```shell
git clone git@github.com:scottywakefield/docs.git
```

// make new repo in current dir
```shell
git init
git add .
```

// getting remote branch
```shell
git pull/git fetch
git checkout <branch_name>
```

// What are the diffs between my branch and master
```shell
git diff --name-status master..<branch_name>
```

// update git submodule
```shell
git submodule update --init
```

// list existing branches:
```shell
git branch
git branch -r // for remote
```

// what are the remote servers
```shell
git remote
git remote -v //verbose
```

// create new branch
```shell
git checkout -b <name> new branch with <name>
```

// misc
```shell
git add --all /./u
git commit -m "message"
git status
git push
```

// to make remote branch:
```shell
git push --set-upstream origin <name>
```

// branch management
```shell
git branch -d <name> //deletes local branch

git branch -r // still exists on server

git push origin :<name> // deletes from server
```

// stashing
```shell
git stash
git stash apply
git stash pop
git stash show
git stash list
git stash drop stash@{0}
git stash apply stash@{0}
```

// reset staged but uncommitted changes
```shell
git reset filename
```

// reset committed changes on branch back to master
```shell
git checkout origin/master filename
```

// cherry-picking
```shell
cherry-pick hash
cherry-pick hash1..hashx //this is NOT inclusive of hash1 and hashx
```

// rebase - only do this if no one else is using the same branch, e.g. before push --set-upstream
```shell
git pull --rebase origin master
git push -f
```

// and then when someone IS using your branch and complains that getting your branch doesn't work after you've force pushed, they should:
```shell
git reset --hard origin/your_branch
```

// or if they have made changes
```shell
git merge origin/your_branch
```

// remove all .orig files (PS)
```ps
Get-ChildItem . -recurse -include *.orig | Remove-Item
```
// with console output
```ps
Get-ChildItem . -recurse -include *.orig | % { $file = $_; Remove-Item $file.FullName; "Deleted file: $($file.FullName)" }
```
