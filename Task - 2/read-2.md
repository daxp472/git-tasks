
### **Part 1: Git Basics**

#### **Task 1: Install and Configure Git**
**Install Git**: Download and install from.
**Configure Git**: Set your global Git settings using:
  ```
  git config --global user.name "Your Name"
  git config --global user.email "your-email@example.com"
  ```
**Verify Configuration**: Check your configuration with:
  ```
  git config --list
  ```

#### **Task 2: Initialize a Repository**
**Create and Initialize**:
  ```
  mkdir MyProject
  cd MyProject
  git init
  ```
**Purpose**: This creates a `.git` directory to begin tracking your project.

---

### **Part 2: Basic Workflow**

#### **Task 3: Creating and Committing Files**
**Create a File**:
  ```
  echo "Hello Git" > file1.txt
  ```
**Stage and Commit**:
  ```
  git add file1.txt
  git commit -m "Initial commit: Added file1.txt"
  ```

#### **Task 4: Viewing Changes**
**Modify the File**:
  ```
  echo "Git is awesome!" >> file1.txt
  ```

**Check the Status and Differences**:
  ```
  git status
  git diff
  ```

#### **Task 5: Undoing Changes**
**Unstage a Staged File**:
  ```
  git reset file1.txt
  ```
**Discard Uncommitted Changes**:
  ```
  git checkout -- file1.txt
  ```

---

### **Part 3: Branching and Merging**

#### **Task 6: Branch Management**
**Create and Switch to a New Branch**:
  ```
  git checkout -b feature-branch
  ```
**List Branches**:
  ```
  git branch
  ```
**Rename a Branch**:
  ```
  git branch -m feature-branch feature-enhanced
  ```

#### **Task 7: Merging Branches**
**Merge a Branch**:
  ```
  git checkout main
  git merge feature-enhanced
  ```

#### **Task 8: Handling Merge Conflicts**
**Simulate a Conflict**:
Create changes in two branches that modify the same lines.
Merge branches and resolve conflicts manually:
    ```
    git merge <branch-name>
    git add <resolved-file>
    git commit
    ```

---

### **Part 4: Remote Repositories**

#### **Task 9: Remote Setup**
**Add a Remote Repository**:
  ```
  git remote add origin https://github.com/your-username/repo.git
  ```
**Verify Remote**:
  ```
  git remote -v
  ```

#### **Task 10: Push and Pull**
**Push Changes**:
  ```
  git push -u origin main
  ```
**Pull Changes**:
  ```
  git pull origin main
  ```

#### **Task 11: Cloning a Repository**
**Clone a Remote Repository**:
  ```
  git clone https://github.com/your-username/repo.git
  ```

---

### **Part 5: Advanced Git**

#### **Task 12: Stashing Changes**
**Save Uncommitted Changes**:
  ```
  git stash
  ```
**Apply Stashed Changes**:
  ```
  git stash apply
  ```
**Drop the Stash**:
  ```
  git stash drop
  ```

#### **Task 13: Tagging Commits**
**Create and Annotate a Tag**:
  ```
  git tag -a v1.0 -m "Version 1.0 release"
  ```
**Push the Tag**:
  ```
  git push origin v1.0
  ```

#### **Task 14: Rewriting Commit History**
**Interactive Rebase**:
  ```
  git rebase -i HEAD~3
  ```
Replace `pick` with `edit` or `squash` to modify commit messages or combine commits.

#### **Task 15: Cherry-Picking Commits**
**Pick a Commit from Another Branch**:
  ```
  git cherry-pick <commit-hash>
  ```

---

### **Part 6: Collaboration**

#### **Task 16: Forking and Pull Requests**
**Fork a Repo and Clone It**:
  ```
  git clone https://github.com/your-username/forked-repo.git
  ```
**Create a New Branch, Make Changes, and Push**:
  ```
  git checkout -b fix-typo
  echo "Typo fixed" >> README.md
  git commit -m "Fixed a typo"
  git push origin fix-typo
  ```
**Open a Pull Request on GitHub**.

#### **Task 17: Simulating Team Collaboration**
**Simulate a Conflict**: Have two users modify the same file and practice resolving the conflict together.

---

### **Part 7: Ignoring Files**

#### **Task 18: Using .gitignore**
**Create a `.gitignore` File**:
  ```
  echo "node_modules/" > .gitignore
  git add .gitignore
  git commit -m "Added .gitignore"
  ```
**Check Ignored Files**:
  ```
  git status
  ```



### **Part 8: Automation and Cleanup**

#### **Task 19: Cleaning the Repository**
**Remove Untracked Files**:
  ```
  git clean -f
  ```

#### **Task 20: Aliases and Shortcuts**
**Create Git Aliases**:
  ```
  git config --global alias.st status
  git config --global alias.cm commit
  ```
**Use the Alias**:
  ```
  git st
  git cm -m "Message"
  ```
