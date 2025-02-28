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
$ git add -A  (This stages all changes, including deleted files.)
```

2. git reset: Unstages a file (reverts it to the working directory).
This command unstages a file, i.e., it removes it from the staging area but leaves the changes in the working directory.
```
$ git reset file.txt
```

3. git commit --amend: Modifies the last commit (can change the commit message or add changes).
This command allows you to amend the most recent commit. You can use it to change the commit message or add new changes to the commit.
Important: You can only amend the last commit in your local repository (before it has been pushed to a remote).
```
$ git commit --amend -m "Updated commit message"
```

4. git commit --all: Automatically stages tracked files and commits them.
This command automatically stages all modified and deleted files that are already tracked (i.e., files that have been previously added to Git). It then commits them in one step.
```
$ git commit --all -m "Commit all tracked changes"
```

5. git commit -a: Stages and commits all modified files.
This is shorthand for git commit --all. It stages all modified and deleted tracked files and commits them in one step.
```
$ git commit -a -m "Staging and committing all modified files"
```

6. git commit --no-verify: Skips pre-commit hooks while committing.
This command skips the execution of pre-commit hooks, which are typically used to run tests, linters, or other checks before committing. Use this if you want to bypass those checks.
```
$ git commit --no-verify -m "Commit without pre-commit hooks"
```

7. git reset --soft HEAD~1: Moves the HEAD pointer back one commit but leaves your changes staged.
This command moves the HEAD pointer (and the current branch) back by one commit, but it keeps the changes you made in the working directory and staged. This is useful if you want to edit the last commit or amend it.
```
$ git reset --soft HEAD~1
```

8. git reset --hard HEAD~1: Moves the HEAD pointer back one commit and discards changes in the working directory.
This command resets the HEAD pointer back by one commit, and discards all changes in the working directory and the staging area. This is a destructive operation as it permanently removes uncommitted changes.
```
$ git reset --hard HEAD~1
```

## Viewing and Comparing Changes (Inspecting changes) 
| Command                                 | Description                                                             | Example Command                                  |
|-----------------------------------------|-------------------------------------------------------------------------|-------------------------------------------------|
| **`git diff`**                          | Shows changes between your working directory and the index (unstaged changes). | `git diff`                                      |
| **`git diff --staged`**                 | Shows changes between the staged files and the last commit.              | `git diff --staged`                             |
| **`git diff <commit_id>`**              | Shows the differences between the working directory and a specific commit. | `git diff abc1234`                              |
| **`git log`**                           | Displays the commit history.                                             | `git log`                                       |
| **`git log --oneline`**                 | Displays the commit history in a simplified one-line format.             | `git log --oneline`                             |
| **`git log --graph`**                   | Displays the commit history as a graph.                                  | `git log --graph`                               |
| **`git log --author="name"`**           | Filters commits by a specific author.                                    | `git log --author="John Doe"`                   |
| **`git log --since="2 weeks ago"`**     | Filters commits made after a specific date.                              | `git log --since="2 weeks ago"`                 |
| **`git blame <file_path>`**             | Shows line-by-line annotations for a file, telling who last modified each line. | `git blame README.md`                          |
| **`git show <commit_id>`**              | Shows details of a specific commit, including diff and metadata.        | `git show abc1234`                              |
| **`git show <commit_id>:<file_path>`**  | Shows a specific file at a particular commit along with the diff.        | `git show abc1234:README.md`                    |

## Reverting and Resetting (Undoing changes)
| Command                                      | Description                                                                 | Example Command                                          |
|----------------------------------------------|-----------------------------------------------------------------------------|---------------------------------------------------------|
| **`git reset <commit_id>`**                  | Moves HEAD to a specific commit, leaving your working directory intact.     | `git reset abc1234`                                      |
| **`git reset --hard <commit_id>`**           | Resets your working directory, index, and HEAD to a specific commit (all changes will be lost). | `git reset --hard abc1234`                               |
| **`git reset --soft <commit_id>`**           | Resets only the HEAD to a specific commit, leaving staged changes.         | `git reset --soft abc1234`                               |
| **`git reset --mixed <commit_id>`**          | Resets the HEAD and index to a specific commit but keeps the working directory unchanged. | `git reset --mixed abc1234`                              |
| **`git revert <commit_id>`**                 | Creates a new commit that undoes the changes of the specified commit.      | `git revert abc1234`                                     |
| **`git restore <file_path>`**                | Restores the file(s) in the working directory from the index or a commit.  | `git restore README.md`                                  |
| **`git restore --staged <file_path>`**       | Removes a file from the staging area.                                       | `git restore --staged README.md`                         |
| **`git clean -f`**                           | Removes untracked files in the working directory.                          | `git clean -f`                                           |
| **`git clean -fd`**                          | Removes untracked files and directories.                                   | `git clean -fd`                                          |
