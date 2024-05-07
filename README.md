# Git Clean Sheet

### Key 🔑:
  variable ->  `<var>`
  
  optional variable -> `[<var>]`

## USER 👥
commands                                      |                   Description
----------------------------------------------|--------------------------------
`git config --global user.name <name>` | Define the author Username to be used for all commits by the current user
`git config --global user.email <email>` | Define the author email to be used for all commits by the current user
`git config --system core.editor <editor>`| Set text editor used by commands for all users on the machine. <editor> arg should be the command that launches the desired editor (e.g vim)
`git config --global alias. <alias-name> <git-command>` | Create shortcut or alias for a Git command
`git config --global --edit` | Open the global configuration file in a text editor for manual editing

## REPOSITORY 📁
Repo `REMOTE URL` -> `https://<TOKEN>@github.com/<USERNAME>/<REPOSITORY NAME>.git`
commands                |                   Description
------------------------|--------------------------------
`git init [<directory>]` | create a local repository with a default branch in the directory passed or in present directory if dir name is not added

### remote  🌐📁
commands                |                   Description
------------------------|--------------------------------
`git remote` | View all remote repositories
`git remote add <name> <repo url>` | Create a new connection to a remote repo.
`git remote set-url <name> <repo new url>` | updates the old connection <url> to the new one
`git remote -v` | check remotes <origin> url for push and pull of current repository
`git clone <remote>` | Copy a remote repository to your local directory
### Pull and Fetch 📁💻 ⇠  ⇠ 🌐📁
commands                |                   Description
------------------------|--------------------------------
`git fetch <remote> [<branch>]` | Fetches a specific <branch> or all remote refs
`git fetch [-u, --set-upstream] <remote>` | sets the default remote branch for the current local branch and fetches the branch from remote `-u or --set-upstream` sets  `branch.<name>.remote` and `branch.<name>.merge`
`git pull <remote> [<branch>]` | Fetch the specified remote’s copy of <branch>  or current branch and immediately merge it into the local copy 
`git pull [-u, --set-upstream] <remote>` | sets the default remote branch for the current local branch and pulls the branch from remote

### Push 📁💻 ⇢  ⇢ 🌐📁
commands                |                   Description
------------------------|--------------------------------
`git push [-u, --set-upstream] <remote> <branch>` | sets the default remote branch for the current local branch and push the branch to remote
`git push <remote> <branch>` | Push the branch to <remote>, along with necessary commits and objects (snapshot)
`git push <remote> --all` | Push all of your local branches to the specified remote
`git push <remote> --tags` | Tags aren’t automatically pushed when you push a branch or use the --all flag. The --tags flag sends all of your local tags to the remote repo.

### branch ᛘ
commands                |                   Description
------------------------|--------------------------------
`git branch <branch name>` | creates a new branch.
` git branch -u` | 
`git branch [--list]` | View branches and their details
`git checkout <branch name>` | Switch to a different branch
`git checkout -b <New branch Name>` | create a local branch if it does not exist in the repository and Switch to it
`git branch -m <old name> <new name>` | Rename a branch.
`git branch --set-upstream-to <remote-branch>` | sets the default remote branch for the current local branch
`git merge <branch name>` | Try to merge/ the current branch with the specified <branch>
`git merge <source branch> <target branch> `| Merge the two given branches
`git branch –d <branch name>` | Delete the specified branch.
`git rebase <branch name>` | Apply all the commits of the current branch ahead of the specified branch
`git push origin --delete <branch name>` | Delete a remote branch

---------------------------------
## Files 📄

commands                                           |                   Description
---------------------------------------------------|--------------------------------
`git add [.] [<file>]` | Add the specified file, changes to file or all files if `.` is used from the local directory to the staging area of GIT
`git add -A`  | Add all changes from the local directory to the staging area of GIT
`git status` | List which files are staged, unstaged, and untracked.Any pending commit, push, or pull
`git stach`


### git log 📈 -> 📝

commands                                           |                   Description
---------------------------------------------------|--------------------------------
`git log  [options]`                 | View a list of all the commits made to a repository
`options` =>              | ..............
`--summary`               | View a detailed log of all the commits made to a repository
`--oneline`               | Condense each commit to a single line.
`--graph`                 | draws a text based graph of commits on left side of commit msgs.
`--decorate`              |  adds names of branches or tags of commits shown.
`--after='<Date YYYY-MM-DD>'` |  Only view commit logs after the specified date.
` -<limit>`              | Limit number of commits by <limit>
`-p`     | Display the full diff of each commit
`--stat` | Include which files were altered and the relative number of lines that were added or deleted from each of them
`--author='<pattern>'` | Search for commits by a particular author
`--grep='<pattern>'`    | Search for commits with a commit message that matches <pattern>
`<since>..<until>`     | Show commits that occur between <since> and <until>. Args can be a commit ID, branch name, HEAD, or any other kind of revision reference
`-- <file>` | Only display commits that have the specified file

------------------------------------
