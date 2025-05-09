## 1️⃣ Day 1: 20-04-2025

### **Lessons Completed:**

- 2.1 Getting a Git Repository
- 2.2 Recording Changes to the Repository

### **Learnings:**

### Basic Git Workflow

1. `git init`: Creates a .git hidden subdirectory which contains all necessary repository files.
2. `git add`: Starts tracking the specified file(s), stages modified files to be commited.
3. `git commit`: Commits the staged files to the branch.

### Life Cycle of File status

1. **Untracked**: Files that are local to your drive but Git is not trackcing changes made to them.
2. **Unmodified**: Files that are being tracked by Git and no changes have been made to them since the last commit.
3. **Modified**: Files that are being tracked by Git and some modifications have been made to them since the last commit.
4. **Staged**: Newly tracked / modified files that are staged to be commited (using `git add`) for the next commit.
5. After a recent commit, all the staged files now become unmodified.
6. Removing an unmodified file(`git rm`) or a modified/staged file(`git rm -f`) causes them to be either deleted or untracked but still available locally(`git rm --cached`)

### Checking Status of Files

We use `git status` to get information about the status of the files in the current working tree and the branch we are on. <br />
The information it gives us :

- The branch we are on
- Changes to be commited (new file, modified, deleted, renamed)
- Changes not staged for commit (modified, deleted, renamed)
- Untracked files

Since `git status` can be quite verbose, we can use an option flag to shorten the status `git status -s`. The following terms appear on the left side fo the files:

- **??**: Untracked
- **A**: Staged
- **M**: Modified (staged)
- **D**: Deleted
- **MM**: Modified, staged then modified again(unstaged)

### Tracking new files / Staging changes
We use `git add <new_file_name>` to start tracking a new files. <br />
Or, we can use `git add <modified_file_name>` to stage the changes made in an existing file.

### Seeing changes made
To look at the changes that are not yet staged use `git diff`. Alternatively, to look at the changes made by the current staged files since the last commit, use `git diff --staged`


### Commiting changes
To commit the staged changes, the following syntax is used: `git commit -m "Commit summary" -m "Commit description"`. If we only use `git commit`, the default text editor will open up where we can add the commit sumarry and description.

### Commiting without Staging
If we use `git commit -a -m "Commit message"` this will commit all the files that are changed since the last commit and we skip the staging step.

### Removing Files
If a file is unmodified since the last commit, we can either:
1. Delete the file from the working directory.
2. Use `git rm <file_name>` or `git add <file_name>` to stage the deletion of the file

Or simply use, `git rm <file_name>`.<br />
However, if the file is either modified or staged, we need to use the `-f` flag. So the whole command look something like: 
`git rm -f <file_name>`

### Ignoring files in Git
To stop some files to be commited to Git, we need to set up *.gitignore* files. Glob patterns work in *.gitignore* files:

`*` : Matched zero or more characters. So, `*.exe` will exclude all *.exe* files.

`!` : Can negate a pattern. So, `!main.exe` will allow main.exe to still be commited while other .exe files won't.

`/` : In the beginning avoids recursive calls. So `/assets/*.png` will only exclude the *.png* files in the current directories' assets subdirectory. Even if an assets folder exists somewhere else as well inside.

`/` : In the end specifies all the children of this directory to be excluded.

For good examples of .gitignore files, visit https://github.com/github/gitignore .