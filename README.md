# GIT
GIT is version control tool that provides a set of commands to manage the source code. 
some operations involve. 
  * cloning the existing repo
  * creating a new branch
  * commiting the code.
  * pull/fetch the code from the remote branch.
  * push the code.
  * resolving the merge conflicts.
  * rebase the code. 


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
```

11. git diff: Shows the differences between your working 
directory and the index (staged changes). <br>

