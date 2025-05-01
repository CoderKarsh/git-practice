## 1️⃣ Day 2: 23-04-2025

### **Lessons Completed:**

- 2.3 Viewing the Commit History (partially)

### **Learnings:**

### Viewing the commit history
We can view the commit history by using the `git log` command. There are many options associated with it: 
- `- <n>`: Limits the number of logs shown.
- `--patch` or `-p`: Shows the difference introduced in each commit.
- `--stat`: After each commit log, it shows a list of files changed and the number of lines added/deleted from them.
- `--pretty=<format>`: Changes the format of the log. Eg: `--pretty=oneline` prints each log in a single line. We have a lot of flexibility with the format by using `--pretty=format:"<format specifiers>"`. We can specify which pieces of information to display. The specifiers are listed [here](https://git-scm.com/book/en/v2/Git-Basics-Viewing-the-Commit-History#pretty_format).
- `--oneline`: Shortcut for the above command if oneline format is required.
- `--graph`: Uses ASCII characters to reprsent branching and merging. Apprarently, its use case will be clearer in future lessons.
- To look at more options, go [here](https://git-scm.com/book/en/v2/Git-Basics-Viewing-the-Commit-History#log_options).

### Limiting log output

`git log` is a query command. Naturally, it must have options to fetch only a few entries based on some criteria. Here's a short list:
- `-<n>`: Limits the number of logs shown.