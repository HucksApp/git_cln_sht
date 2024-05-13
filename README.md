# Git Clean Sheet

![git](https://github.com/HucksApp/git_cln_sht/assets/58187974/1c5cea11-dca0-44a3-97f0-b2e77efa1146)


### Key 🔑
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
`git rebase -i <base>` | Interactively rebase current branch onto <base>, transfer completed work from one branch to another

### git remote  🌐📁
commands                |                   Description
------------------------|--------------------------------
`git remote` | View all remote repositories
`git remote add <name> <repo url>` | Create a new connection to a remote repo.
`git remote set-url <name> <repo new url>` | updates the old connection <url> to the new one
`git remote -v` | check remotes <origin> url for push and pull of current repository
`git clone <remote>` | Copy a remote repository to your local directory
### git pull and  git fetch 📁💻 ⇠  ⇠ 🌐📁
commands                |                   Description
------------------------|--------------------------------
`git fetch [<remote>] [<branch>]` | Fetches a specific <branch> or all remote refs
`git fetch [-u, --set-upstream] [<remote>]` | sets the default remote branch for the current local branch and fetches the branch from remote `-u or --set-upstream` sets  `branch.<name>.remote` and `branch.<name>.merge`
`git pull [<remote>] [<branch>]` | Fetch the specified remote’s copy of <branch>  or current branch and immediately merge it into the local copy 
`git pull [-u, --set-upstream] [<remote>]` | sets the default remote branch for the current local branch and pulls the branch from remote
`git pull [<remote>] [<branch>] [options]` | Fetch the specified remote’s copy of <branch>  or current branch
options =>           | ..............
`--rebase` | Fetch the remote’s copy of  <branch> and rebases it into the local copy. Uses git rebase instead of merge to integrate the branches.
`--no-rebase` | Fetch the remote’s copy of <branch> and merges it into the local
copy.

### git push 📁💻 ⇢  ⇢ 🌐📁
commands                |                   Description
------------------------|--------------------------------
`git push [-u, --set-upstream] [<remote>] [<branch>]` | sets the default remote branch for the current local branch and push the branch to remote
`git push [<remote>] [<branch>] [option]` | Push the branch to <remote>, along with necessary commits and objects (snapshot)
options =>           | ..............
`--all` | Push all of your local branches to the specified remote
`--tags` | Tags aren’t automatically pushed when you push a branch or use the --all flag. The --tags flag sends all of your local tags to the remote repo
`--force` | Forces the git push even if it results in a ***non-fast-forward merge***

### git branch ᛘ
commands                |                   Description
------------------------|--------------------------------
`git branch [option]` | View branches in the repo
options =>       |       .................
`-r` |
`--list` | View branches and their details
`<branch name>` | creates a new branch.
`–d <branch name>` | Delete the specified branch.
`-m <old name> <new name>` | Rename a branch
`-u` | sets the default remote branch for the current local branch
`--set-upstream-to <remote-branch>` | sets the default remote branch for the current local branch
`git checkout <branch name>` | Switch to a different branch
`git checkout -b <New branch Name>` | create a local branch if it does not exist in the repository and Switch to it
`git merge <branch name>` | Try to merge/ the current branch with the specified <branch>
`git merge <source branch> <target branch> `| Merge the two given branches
`git rebase <branch name>` | Apply all the commits of the current branch ahead of the specified branch
`git push origin --delete <branch name>` | Delete a remote branch

---------------------------------
## Files 📄


commands                                           |                   Description
---------------------------------------------------|--------------------------------
`git mv <old_file_name> <new_file_name>`      | Rename file
`git diff [option]` | Show unstaged changes between your index and working directory
options =>       |       .................
`--staged` | see any staged changes

### git add 🗄➕📄
commands                                           |                   Description
---------------------------------------------------|--------------------------------
`git add [options]`              | Add files to stagin area in git
options =>       |       .................
`[.] ` | Add all files or changes to files from the local directory to the staging area of GIT
`[<file>]`        | Add the specified file or changes to file from the local directory to the staging area of GIT
`-A`  | Add all changes from the local directory to the staging area of GIT
`-p` | opens an interactive (prompt)

commands                                           |                   Description
---------------------------------------------------|--------------------------------
`git status` | List which files are staged, unstaged, and untracked.Any pending commit, push, or pull
## git stash 🗳
commands                                           |                   Description
---------------------------------------------------|--------------------------------
`git stash `             | Saves the uncommitted changes locally.Move the changes in the working directory into a stash space. This allows you to save your changes for future use, without making a new commit.
`git stash pop` | Recover the stashed changes.Move the changes from the stash back to the working directory


## git commit 🗄♽
commands                                           |                   Description
---------------------------------------------------|--------------------------------
`git commit [options] ` | Commit the staged snapshot
options =>                            | ...........
`-m "<message>"`           | use <message> as the commit message
`-a`                       |  add and commit all tracked files
`--amend`        | modify the most recent commit. Combine staged changes with the previous commit instead of creating an entirely new commit


## git reflog 🗄𝞭

commands                                           |                   Description
---------------------------------------------------|--------------------------------
`git reflog  [options]`    |  Show a log of changes to the local repository’s ***HEAD***
options =>                            | ...........
`--relative-date`        |  show date info
`--all`             | show all refs


### git log 📈 → 📝

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
