# GIT
GIT is version control tool that provides a set of commands to manage the source code. 
some operations involve. 
```
  * cloning the existing repo
  * creating a new branch
  * commiting the code.
  * pull/fetch the code from the remote branch.
  * push the code.
  * resolving the merge conflicts.
  * rebase the code. 
```

## Basic GIT Commands <br>

1. git init: Initializes a new Git repository in the current 
directory. <br>
```
$ git init
```

2. git clone: Clones a repository from a remote 
URL to your local machine. <br>
```
$ git clone <repo_url>
```

3. git status: Shows the working directory status (which files are 
modified, staged, etc.). <br>
```
$ git status
```
4. git add : Stages a file or files to be committed. <br>
```
$ git add *
$ git add filename1 filename2
```

5. git commit -m "message": Commits staged changes to the 
local repository with a message. <br>
```
$ git commit -m "sample commit message"
```

6. git push: Pushes committed changes to the remote repository. <br>
```
$ git push origin main
$ git push origin <branch_name>
$ git push
```

7. git pull: Fetches and merges changes from the remote <br>
repository to your local working directory. <br>
```
$ git pull origin main
$ git pull origin <branch_name>
$ git pull
```

8. git fetch: Downloads objects and refs from another repository 
(without merging). <br>
```
$ git fetch origin main
$ git fetch origin <branch_name>
$ git fetch --all
```

9. git merge : Merges changes from the specified branch into the 
current branch. <br>
```
$ git merge origin main
$ git merge <feature_branch>
```

10. git log: Shows the commit history of the repository. <br>
```
$ git log
$ git log -n 5 (shows last 5 commits)
$ git log feature-branch (commit history for specific feature branch)
$ git log --oneline (for compact view)
$ git log --oneline -n 5 (shows last 5 commits in oneline)
$ git log --author="Alice" (commits by a specific Author)
$ git log --since="2025-01-01" (commits from the Date)
$ git log --until="2025-02-01" (commits before a specific date)
```

11. git diff: Shows the differences between your working 
directory and the index (staged changes). <br>
```
$ git diff
$ git diff --staged (difference between staged changes and last commit) 
$ git diff <commit1> <commit2> (difference between 2 commits)
$ git diff main..feature-branch (difference between main branch and Feature branch)
$ git diff path/to/file.txt (shows changes made to a specific file)
$ git diff --word-diff (shows the word by word differences)
$ git diff --stat (to show the summary of changes)
```



## Branching Commands
1. git branch: Lists all branches in your repository. <br>
```
$ git branch
```
2. git branch <branch_name>: Creates a new branch. <br>
```
$ git branch feature-branch
```
3. git checkout <branch_name>: Switches to an existing 
branch. <br>
```
git checkout feature-branch
```
4. git checkout -b <branch_name>: Creates and switches to a 
new branch in one step. <br>
```
git checkout feature-branch
git checkout -b new-feature
```
5. git merge <branch_name>: Merges changes from the 
specified branch into the current branch.  <br>
```
$ git merge feature-branch
```
6. git rebase <branch_name>: Applies changes from one 
branch onto another branch (instead of merging). <br>
```
$ git rebase feature-branch
```
7. git branch -d <branch_name>: Deletes the specified branch 
(locally). <br>
```
$ git branch -d feature-branch
```
8. git branch -D <branch_name>: Forcefully deletes a branch 
(locally). <br>
```
$ git branch -D feature-branch
```
9. git remote set-head origin <branch_name>: Sets the 
default branch for the remote repository. <br>
```
$ git remote set-head origin feature-branch
```

##  Remote Commands (Managing remotes and syncing with the cloud) 
1. git remote -v: Shows the remote repository URLs. 
```
$ git remote -v
```
2. git remote add : Adds a new remote repository. 
```
$ git remote add origin https://github.com/username/repository.git
```
3. git remote remove : Removes a remote repository. 
```
$ git remote remove origin
```
4. git push origin <branch_name>: Pushes a branch to a remote repository. 
```
$ git push origin feature-branch
```
5. git push -u origin <branch_name>: Pushes a branch to a remote repository and sets the upstream for the branch. 
```
$ git push -u origin feature-branch
```
6. git pull origin <branch_name>: Fetches and merges a branch from the remote repository. 
```
$ git pull origin feature-branch
```
7. git fetch origin: Downloads objects and refs from the remote repository. 
```
$ git fetch origin
```
8. git remote show origin: Displays detailed information about a remote repository.
```
$ git remote show origin
```

## Staging and Committing (Managing changes) 

1. git add .: Stages all modified files in the working directory.
This command stages all the changes in your working directory, including modified and newly created files (but not deleted files).
```
$ git add .
```
