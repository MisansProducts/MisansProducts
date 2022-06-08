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
* `git remote remove origin` - Removes the connection from a local git repository to GitHub.
* `git log` - Displays all commits in a local git repository.
* `git status` - Displays staged files that are ready to commit.

### Branching
* `git branch` - Displays all branches in a local git repository.
* `git branch [NAME]` - Creates a new branch in a local git repository.
* `git checkout [NAME]` - Switches to a different branch in a local git repository.

## Notes

Do **NOT** use Windows PowerShell to create files. It will take on UTF-16 formatting which will cause some issues. For example, .gitignore files do not work unless they are in UTF-8.

Try to LF normalize all files uploaded to GitHub for cross-platform compatibility with Unix operating systems. There is no reason to keep CRLF on Windows because LF works just fine.

Be aware that on Windows OS, as long as a file has 2 or more lines, it can be saved as a LF end of line sequence. If a file has only 1 line - even if it is saved as a LF EOL sequence - upon reopening the file, it will take on the CRLF EOL sequence. I discovered this when my .gitignore files kept reverting back to CRLF EOL sequence. If a file is 1 line long, then add an extra empty line.

Microsoft Visual Studio Code misspells multi-line pastes the first time through the Git Bash terminal. I need to experiment with this.
