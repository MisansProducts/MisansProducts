## Commands

### Upload

* `git init` - Creates a local git repository.
* `git add .` - Stages all files in a local git repository.
* `git commit -m "[TITLE]" -m "[DESCRIPTION]"` - Saves changes and creates a snapshot of staged files in a local git repository.
* `git remote add origin [URL]` - Creates a connection from a local git repository to GitHub.
* `git branch -M main` - Renames the default branch in a local git repository to "main".
* `git push -u origin main` - Uploads commits from a local repository to GitHub. The "-u" flag automatically sets the upstream to the local repository.

### Revise or Remove

* `git push -f origin HEAD^:main` - Removes the last commit from GitHub.
  * The amount of "^" indicates the amount of commits to remove.
* `git reset --soft HEAD^` - Removes the last commit from a local git repository.
* `git log` - Displays all commits in a local git repository.
* `git status` - Displays staged files that are ready to commit.

### Branching
* `git branch` - Displays all branches in a local git repository.
* `git branch [NAME]` - Creates a new branch in a local git repository.
* `git checkout [NAME]` - Switches to a different branch in a local git repository.
