# 3️⃣ Day 3: 02-05-2025

### **Lessons Completed:**

- 2.3 Viewing the Commit History (continued and completed)

### **Learnings:**

### Limiting log output

`git log` has many options. Some of them are listed below:

- `--since`, `after`: We can specify a date; either absolute (2023-01-15) or relative(2 years 1 day 1 minute ago); and all logs from that date to current date will be logged.
- `--until`, `--before`: Limits the date upto which logs are shown.
- `--author`: To specify some author and only their commits are logged.
- `--committer`: To specify some committer and only their commits are logged.
- `--path/to/file`: A specific file/folder can be specified.
- `--grep`: If we remember parts of a git message, we can use this option.
- `-S`: Used to log the commit that changed some specific code.

### **Additional Learnings:**

### Saving a format in global config

We can save a specific pretty format string as default using global configs.
Example: `git config --global format.pretty '%h | %ad  [%an] | %s'`

Source: [githowto.com/history](https://githowto.com/history)

### Time travelling in Git

To return to how the repository was at some specific commit. We can use `git checkout <hash>`. Then:

- If we wish to return to the main branch, we can use `git switch main`.
- If we wish to make changes to that state and save them, we can put them in a separate branch using `git switch -c <new branch name>`.
