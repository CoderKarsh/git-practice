# Learning Git

This repository is solely made for the purposes of learning Git. I will be following the instructions in the following book:
[Pro Git by Scott Chaconand Ben Straub](https://git-scm.com/book/en/v2)

I intend to finish Chapters 2 - 7 in 2 weeks. I'll also be documenting my learning in this README.md file.

---

## :one: Day 1: 20-04-2025

Lessons Completed:
- 2.1 Getting a Git Repository
- 2.2 Recording Changes to the Repository

Things Learnt:
### Basic Git Workflow
1. `git init`: Creates a .git hidden subdirectory which contains all necessary repository files.
2. `git add`: Starts tracking the specified file(s), stages modified files to be commited.
3. `git commit`: Commits the staged files to the branch.

### Life Cycle of File status
1. Untracked: Files that are local to your drive but Git is not trackcing changes made to them.
2. Unmodified: Files that are being tracked by Git and no changes have been made to them since the last commit.
3. Modified: Files that are being tracked by Git and some modifications have been made to them since the last commit.
4. Staged: Newly tracked / modified files that are staged to be commited (using `git add`) for the next commit. 
5. After a recent commit, all the staged files now become unmodified.
6. Removing an unmodified file(`git rm`) or a modified/staged file(`git rm -f`) causes them to be either deleted or untracked but still available locally(`git rm --cached`)

### Checking Status of Files
We use `git status` to get information about the status of the files in the current working tree and the branch we are on.
What information it gives us:
- The branch we are on
- Changes to be commited (new file, modified, deleted, renamed)
- Changes not staged for commit (modified, deleted, renamed)
- Untracked files

Since `git status` can be quite verbose, we can use an option flag to shorten the status  `git status -s`. The following terms appear on the left side fo the files:
- ??: Untracked
- A: Staged
- M: Modified (unstaged)
- D: Deleted
- MM: Modification staged but also 
