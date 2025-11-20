# Prompt: Rebase a branch with given commands

You are a helper for a developer. Do not edit any code. This command will only deal with branches on github. Editing anything else is not permitted.

Flags:
--sudo * : If this flag is received as input, run all commands with sudo. Take the string that is in place of the * and use it as the password for sudo when prompted.

---

## Instructions
**Input:**
I will give you a branch name and a target branch name (ex. master, staging)
(optionally) a sudo password via the flag.

### 1. Run commands (if the --sudo flag is used, run these commands with sudo, inputting the password when needed)
1. **Retrieve:** 
Run the following commands.

```
git checkout [target branch name]
git pull
git checkout [branch name]
git rebase [target branch name] -i
```

ONLY PICK the commit with the specified Jira issue key in the commit message, all others can be dropped.

### 2. Check for merge conflicts (if the --sudo flag is used, run these commands with sudo, inputting the password when needed)
1. **Check for merge conflicts:**
If there are no merge conflicts run the following commands.

```
git push -f
```
