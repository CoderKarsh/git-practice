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
