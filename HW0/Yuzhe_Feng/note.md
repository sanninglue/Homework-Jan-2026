# HW0 Q&A
### 1. What is the difference between git fetch and git pull?

Git fetch downloads the latest commits from the remote repository but does not modify my local branches. 
Git pull downloads and immediately merges them to current branch. So Git pull is git fetch + git merge.
### 2. What is the difference between git merge and git rebase?

Git merge combines two branches by creating a new merge commit. It is safe, non-destructive, preserves the full history. But too many merge commits can create a cluttered history, harder to read and navigate. 
Git rebase moves commits from one branch on top of another, creating a linear history which is clean and easy-to-read. But you can not rebase commits on the branch that have already been shared with others, it can cause conflict and serious problems.
### 3. How do you resolve merge conflicts in Git?

I use merge tool to resolve conflict. Run git mergetool, it will display my local changes, remote changes, and the base version side by side. I can easily review the differences, select or combine the correct changes, and save the result.
### 4. What is the purpose of .gitignore?

The purpose of the .gitignore file is to specify untracked files and directories that Git should ignore like the generated files, build artifacts, etc. 
It helps the repository stay clean and lightweight. It also helps prevent accidental commits of unnecessary or confidential files.
### 5. How do you undo a commit that has already been pushed?

For a commit that has already been pushed, I usually use git revert because it safely undoes the change without rewriting commit history, which is important for shared branches. 
Alternatively, I would use git reset --hard followed by a force push if it is on a personal or temporary branch, since it rewrites history and can disrupt other collaborators.
### 6. Can you give me some common git commands?

Some common Git commands I use are git init to initialize a repository, git add to stage changes, and git commit to save changes with a message. git branch and git checkout to manage branches, git merge or git rebase to integrate changes, and git pull and git push to sync with a remote repository.