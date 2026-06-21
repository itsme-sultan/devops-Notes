## History of Git:  
GIT - Global information tracker  
Devloped by the linus torvald to track the code and maintain the version of the  code.  

## `git remote add origin <url>`  
**Purpose:** Creates a new remote connection named origin pointing to the given repository URL.  
**When used:** The first time you connect your local repo to a remote (e.g., GitHub).

## `git remote set-url origin <url>`  
**Purpose:** Updates the URL of an existing remote (like origin).  
**When used:** If you already have origin defined but want to change its URL (e.g., switch from HTTPS to SSH, or point to a different repo).

## `git rebase`  
Definition: Moves your branch’s commits to the tip of another branch (usually main or master).  
Effect: Rewrites commit history so it looks like your work was built directly on the latest base branch.  
Creates linear history by rewriting commits. 
Advisable to use in local branch only, do not rebase shared branch since it rewrite the history.

## `git merge --ff-only feature`  
it sync the main branch with feature branch or just slide the commit of the feature branch to the tip of the main branch to get sync.  
ff is only possible when there is no commit in main branch since feature branch get diverged.  
```bash
git checkout main
git merge --ff-only feature
```


