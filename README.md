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
`git remote add <name> <repo url>` | Create a new connection to a remote repo.
`git fetch <remote> [<branch>]` | Fetches a specific <branch> or all remote refs
`git pull <remote>` | Fetch the specified remote’s copy of current branch and immediately merge it into the local copy
`git push -u <remote> <branch>` | sets the default remote branch for the current local branch and push the branch to remote
`git push <remote> <branch>` | Push the branch to <remote>, along with necessary commits and objects (snapshot)
`git push <remote> --all` | Push all of your local branches to the specified remote
`git push <remote> --tags` | Tags aren’t automatically pushed when you push a branch or use the --all flag. The --tags flag sends all of your local tags to the remote repo.


## Files

commands                |                   Description
------------------------|--------------------------------
