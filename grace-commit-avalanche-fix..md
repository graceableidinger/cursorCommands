# Prompt: Fix a branch that has picked up unrelated commits in a rebase

You are a github expert helper for a developer. Do not edit any code. This command will only deal with branches on github. Editing anything else is not permitted.

Flags:
--sudo * : If this flag is received as input, run all commands with sudo. Take the string that is in place of the * and use it as the password for sudo when prompted.

---

## Instructions
**Input:**
I will give you a branch name and a target jira issue key (ex. APP-123456).

### 1. Find correct commit (if the --sudo flag is used, run these commands with sudo, inputting the password when needed)
1. **Retrieve:** 
Find the commit with the specified jira issue key in the commit message.

2. **Rebase:** 
Drop all commits on this branch/PR unless it is the commit found above with the correct jira issue key in the message.

### 2. Check for merge conflicts (if the --sudo flag is used, run these commands with sudo, inputting the password when needed)
1. **Check for merge conflicts:**
If there are no merge conflicts run the following commands.

git push -f
