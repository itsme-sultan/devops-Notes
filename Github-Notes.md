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

```bash
A → B → C (main)  
     \  
      D → E (feature)
After Rebase (git checkout feature & git rebase main or origin/main)  
A → B → C → D' → E'
```

Cons:  
Rewrites commit hashes (dangerous if branch is shared).  
Should only be used on local/private branches

## `git merge`  
Definition: Combines two branches by creating a new commit that ties their histories together.  
Effect: Preserves the full history, including all diverging paths.  
Note : If we are merging features branch changes in main and there is no new commit in the manin brnach since feature branch  
get diverge then it mereg as a fast forward and their will be no new commit.

```bash
A → B → C (main)  
     \  
      D → E (feature)  

After git merge feature
A → B → C → M  
     \     /  
      D → E
```

Pros:  
Safe, non-destructive (no history rewrite).  
Good for shared/public branches.


## `git merge --ff-only feature`  
it sync the main branch with feature branch or just slide the commit of the feature branch to the tip of the main branch to get sync.  
ff is only possible when there is no commit in main branch since feature branch get diverged.  
```bash
git checkout main
git merge --ff-only feature
```


