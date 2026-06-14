## History of Git:  
GIT - Global information tracker  
Devloped by the linus torvald to track the code and maintain the version of the  code.  

`git remote add origin <url>`  
**Purpose:** Creates a new remote connection named origin pointing to the given repository URL.  
**When used:** The first time you connect your local repo to a remote (e.g., GitHub).

`git remote set-url origin <url>`  
**Purpose:** Updates the URL of an existing remote (like origin).  
**When used:** If you already have origin defined but want to change its URL (e.g., switch from HTTPS to SSH, or point to a different repo).

`git rebase`  
Definition: Moves your branch’s commits to the tip of another branch (usually main or master).  
Effect: Rewrites commit history so it looks like your work was built directly on the latest base branch.  
Creates linear history by rewriting commits. 
