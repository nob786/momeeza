# Git Practice Lab for Beginners

## Overview
This practice lab is designed to help beginners learn and understand basic Git commands. Each section contains clear tasks and explanations to enhance your Git skills.

---

## Section 1: Repository Setup & Initialization

### Lab 1.1: Initialize a New Repository
*Objective*: Create a new Git repository.

*Tasks*:
1. *Open your terminal*:
   - On Windows, use Command Prompt or Git Bash. On macOS or Linux, use the Terminal app.

2. *Navigate to your desired directory*:
```
   cd path/to/your/directory
```

3. *Run the command to initialize a new repository*:
```
   git init my-new-repo
```   

4. *Navigate into the new directory*:
```
   cd my-new-repo
```   

5. *Run git status to check the current state of the repository*:
```
   git status
```   

---

---

## Section 2: Tracking and Committing Changes

### Lab 2.1: Stage and Commit Changes
*Objective*: Add changes to the staging area and commit them.

*Tasks*:
1. *Create a new file*:
```
   echo "Hello, World!" > hello.txt
```   

2. *Run git status to see the untracked file*:
```
   git status
```   

3. *Stage the file*:
```
   git add hello.txt
```   

4. *Commit the file with a message*:
```
   git commit -m "Add hello.txt file"
```   

5. *Run git log to view your commit history*:
```
   git log
```   

---

### Lab 2.2: Modify and Recommit
*Objective*: Modify a file and recommit changes.

*Tasks*:
1. *Open hello.txt and add another line*:
```
   echo "This is my first Git lab!" >> hello.txt
```   

2. *Run git status to see modified files*:
```
   git status
```   

3. *Stage and commit the changes*:
```
   git add hello.txt
   git commit -m "Update hello.txt with a new line"
```   

4. *Check your commit history with git log*:
```
   git log
```   

---

## Section 3: Branching and Merging

### Lab 3.1: Create and Switch Branches
*Objective*: Create a new branch and switch to it.

*Tasks*:
1. *Run the command to create a new branch*:
```
   git branch feature-branch
```   

2. *Switch to the new branch*:
```
   git checkout feature-branch
```   

3. *Verify the branch switch*:
```
   git branch
```   

---

### Lab 3.2: Merge Changes from a Branch
*Objective*: Merge changes from one branch into another.

*Tasks*:
1. *Switch back to the main branch*:
```
   git checkout main
```   

2. *Create a new file in the feature branch*:
```
   git checkout feature-branch
   echo "Feature X implemented" > feature.txt
```   

3. *Stage and commit the new file*:
```
   git add feature.txt
   git commit -m "Add feature.txt with Feature X description"
```   

4. *Switch back to the main branch*:
```
   git checkout main
```   

5. *Merge the feature branch into the main branch*:
```
   git merge feature-branch
```   

6. *Verify the merged changes*:
```
   ls
   cat feature.txt
```   

---

## Section 4: Remote Repository Management

### Lab 4.1: Push Local Changes to a Remote Repository
*Objective*: Push local changes to a remote repository.

*Tasks*:
1. *Make sure you are on the main branch*:
```
   git checkout main
```   

2. *Link to your remote GitHub repository*:
```
   git remote add origin <your-repo-url>
```   

3. *Push changes to the remote*:
```
   git push -u origin main
```   

4. *Verify the push on GitHub*:
   - Open your GitHub repository in a web browser to check that the changes are reflected.

---

### Lab 4.2: Pull Latest Changes from a Remote Repository
*Objective*: Fetch and merge changes from the remote.

*Tasks*:
1. *Make changes in the remote repository*.

2. *In your local repository, run git pull*:
```
   git pull origin main
```   

3. *Check for updates*:
```
   git status
   git log
```   

---

## Section 5: Undoing Changes

### Lab 5.1: Unstage Changes
*Objective*: Unstage a file that has been added to the staging area.

*Tasks*:
1. *Create and stage a new file*:
```
   echo "Unstage this" > unstage.txt
   git add unstage.txt
```   

2. *Run git status to see staged files*:
```
   git status
```   

3. *Unstage the file*:
```
   git reset unstage.txt
```   

4. *Verify that the file is unstaged*:
```
   git status
```   

---

### Lab 5.2: Revert a Commit
*Objective*: Revert a specific commit.

*Tasks*:
1. *Run git log to find the commit hash*:
```
   git log
```   

2. *Run the revert command*:
```
   git revert <commit-hash>
```   

3. *Verify the revert commit*:
```
   git log
```   

---

## Section 6: Inspecting Changes

### Lab 6.1: View Changes with Diff
*Objective*: Compare changes in the working directory.

*Tasks*:
1. *Modify hello.txt again*:
```
   echo "Another line added!" >> hello.txt
```  

2. *Run git diff to see changes*:
```
   git diff
```   

---

### Lab 6.2: Blame a File
*Objective*: See who made changes to each line of a file.

*Tasks*:
1. *Run the blame command*:
```
   git blame hello.txt
```   

---

## Section 7: Stashing Changes

### Lab 7.1: Stash and Apply Changes
*Objective*: Temporarily save and apply changes.

*Tasks*:
1. *Create and modify a file*:
```
   echo "Temporary changes" > temp.txt
```   

2. *Run git stash*:
```
   git stash
```   

3. *Verify that the changes are stashed*:
```
   git status
```   

4. *Run git stash pop to reapply changes*:
```
   git stash pop
```   

5. *Check the file to ensure changes are restored*:
```
   cat temp.txt
```   

---

## Section 8: Collaborating with Teams

### Lab 8.1: Fetch and Merge Changes
*Objective*: Fetch changes from a remote repository and merge them.

*Tasks*:
1. *Run git fetch origin*:
```
   git fetch origin
```   

2. *Merge changes from the remote*:
```
   git merge origin/main
```   

3. *Resolve any merge conflicts* if they arise:
   - Git will highlight conflicts in the files. Open the conflicted files and manually resolve them, then stage and commit the resolved files.

---

## Conclusion
At the end of each lab session, reflect on your tasks and outcomes. Feel free to ask questions if you encounter difficulties, ensuring you understand each command's purpose and application. This structured practice lab will help you build confidence and proficiency in using Git effectively.