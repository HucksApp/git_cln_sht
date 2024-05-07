# Git Clean Sheet

### Key:
  variable ->  `<var>`
  
  optional variable -> `[<var>]`

## USER
commands                                      |                   Description
----------------------------------------------|--------------------------------
`git config --global user.name <name>` | Define the author Username to be used for all commits by the current user
`git config --global user.email <email>` | Define the author email to be used for all commits by the current user
`git config --system core.editor <editor>`| Set text editor used by commands for all users on the machine. <editor> arg should be the command that launches the desired editor (e.g vim)
`git config --global alias. <alias-name> <git-command>` | Create shortcut or alias for a Git command
`git config --global --edit` | Open the global configuration file in a text editor for manual editing

## REPOSITORY
Repo `REMOTE URL` -> `https://<TOKEN>@github.com/<USERNAME>/<REPOSITORY NAME>.git`
commands                |                   Description
------------------------|--------------------------------
`git init [<directory>]` | create a local repository with a default branch in the directory passed or in present directory if dir name is not added
`git remote` | View all remote repositories
`git remote add <name> <repo url>` | Create a new connection to a remote repo.
`git remote set-url <name> <repo new url>` | updates the old connection <url> to the new one
`git remote -v` | check remotes <origin> url for push and pull of current repository
`git fetch <remote> [<branch>]` | Fetches a specific <branch> or all remote refs
`git pull <remote> [<branch>]` | Fetch the specified remote’s copy of <branch>  or current branch and immediately merge it into the local copy 
`git push -u <remote> <branch>` | sets the default remote branch for the current local branch and push the branch to remote
`git push <remote> <branch>` | Push the branch to <remote>, along with necessary commits and objects (snapshot)
`git push <remote> --all` | Push all of your local branches to the specified remote
`git push <remote> --tags` | Tags aren’t automatically pushed when you push a branch or use the --all flag. The --tags flag sends all of your local tags to the remote repo.
`git branch <branch name>` | creates a new branch.
`git branch [--list]` | View branches and their details
`git checkout <branch name>` | Switch to a different branch
`git checkout -b <New branch Name>` | create a local branch if it does not exist in the repository and Switch to it
`git branch -m <old name> <new name>` | Rename a branch.
`git merge <branch name>` | Try to merge/ the current branch with the specified <branch>
`git merge <source branch> <target branch> `| Merge the two given branches
`git branch –d <branch name>` | Delete the specified branch.
`git rebase <branch name>` | Apply all the commits of the current branch ahead of the specified branch
`git push origin --delete <branch name>` | 


## Files

commands                |                   Description
------------------------|--------------------------------
