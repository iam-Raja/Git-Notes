# Git-Notes

### What Is Git :
- Git is a distributed version control system (DVCS).
Features:
- Version Control: Git helps track changes made to files over time, allowing you to recall specific versions later if needed.
- Distributed: Each developer's working copy of the code is also a repository that can contain the full history of all changes.
- Branching and Merging: Git makes it easy to create branches (independent lines of development), merge changes from one branch to another, and manage conflicts that may arise.
- Speed and Efficiency: Git is known for its speed in committing changes, branching, merging, and comparing revisions.
- Open Source: Git is free and open-source software, which means it is developed and maintained by a community of contributors worldwide.
- Popular Platforms: Git is supported on all major platforms (Windows, macOS, Linux) and integrates with many IDEs and development tools

### Git Branching :
- Main/master - points to prod
- Release - Go live changes
- Feature - New features to main(mostly used)
- Hot-Fix - Release new changes on emergency

### Git Merging & Branching :
- Cherry-pick : Allows you to select specific commits from one branch and apply them to another branch, creating new commits.
- Merge :  Integrates all changes from one branch into another, preserving the commit history.
- Rebase : Rebasing is another way to integrate changes from one branch into another but rewrites the commit history(main branch commits) to make it appear as if changes were made on top of the target branch.(rebase commit id is gets added at top of commit history).commits applies on top of another branch, resulting in a linear history

### Git lifecycle:
- The Git lifecycle refers to the typical sequence of steps and operations that occur when managing files and projects using Git. Here's a concise overview of the Git lifecycle:
- To add files to the staging area: git add <file>
- To commit changes to the local repository: git commit -m "Commit message"
- To push your committed changes to a remote repository: git push origin <branch>
- To create a new branch: git checkout -b <branch-name>
- To switch between branches: git checkout <branch-name>
- To merge changes from one branch into another: git merge <branch-name> , git rebase <branch-name>
- To fetch and merge changes: git pull origin <branch>
### Git Conflict :
* If git find outs 2 different content in the same line, so git can't take decision. Now, we need to sit together with developers and resolve the issue
### Git reset and revert :
- Reset: Reset will undo the changes, But it is destructive operation as it will changes the history & commit id's.
- Revert: Revert creates new commit that undoes the chnages from a prev commit, reset creates new history.

### Git Stach,Fetch,pull,push :
- Stach : The git stash command is used to temporarily store changes that you haven't committed yet, allowing you to work on something else or switch branches without committing half-done work.(list,apply,pop)- Temporarily saves changes for later use.
- Fetch : The git fetch command is used to retrieve changes from a remote repository without merging them into your own branches.- Retrieves changes from a remote repository without merging.
- Pull: The git pull command is used to fetch changes from a remote repository and integrate them into your current branch. It's a combination of git fetch followed by git merge - Retrieves changes from a remote repository and merges them into the current branch.
- Push: The git push command is used to send your committed changes to a remote repository. It updates the remote repository with the changes made in your local branch.-Sends committed changes to a remote repository
### Git Clone & Fork :
- Clone : Taking a copy of main repo, if we do git pull remote chnages are updated in local repo
- Fork : Taking a copy of main repo, if we do git pull remote chnages are not updated in local repo, unless we do new commits/changes
### Github cloning :
- HTTPS - Authenicate with passwords
- SSH - Authenicate with key's
### Git commands:
- git init: Initializes a new Git repository in the current directory.
- git clone <repository-url>: Clones a repository from a remote server to your local machine.
- git status: Shows the current state of the working directory and staging area
### Committing Changes :
* - git add <file>: Adds changes in a specific file to the staging area.
- git commit -m "Commit message": Commits staged changes to the local repository with a message describing the changes.
- git commit --amend: Amends the last commit with any changes in the staging area or new commit message
### Viewing Changes:
- git branch: Lists all local branches in the repository.
- git branch <branch-name>: Creates a new branch with the specified name.
- git checkout <branch-name>: Switches to the specified branch.
- git merge <branch-name>: Merges changes from the specified branch into the current branch.
- git rebase <branch-name>: Reapplies commits from one branch onto another branch
### Remote Repositories :
- git remote add <name> <url>: Adds a remote repository reference with a specified name and URL.
- git remote -v: Lists all remote repositories along with their URLs.
- git fetch <remote>: Retrieves changes from a remote repository.
- git pull <remote> <branch>: Fetches changes and merges them into the current branch from a remote repository.
- git push <remote> <branch>: Pushes committed changes from the local repository to a remote repository
### Undoing Changes:
 - git reset <file>: Unstages changes for a specific file from the staging area.
- git reset --soft HEAD~1: Moves HEAD to a previous commit, keeping changes staged.
- git reset --hard HEAD~1: Resets HEAD to a previous commit, discarding all changes in the working directory and staging area.
- git revert <commit>: Creates a new commit that undoes changes made by a previous commit
### Stashing:
- git stash: Temporarily stores changes that haven't been committed yet.
- git stash list: Lists all stashes.
- git stash apply: Applies the most recent stash to the working directory without removing it from the stash list.
- git stash pop: Applies the most recent stash and removes it from the stash list

