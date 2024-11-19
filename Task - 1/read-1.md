
### **Task 1: Introduction to Version Control and Git**

#### **Task 1: Install and Configure Git**

  1. Install Git.
  2. Configure Git with your username and email:  
     ```
     git config --global user.name "daxp472"  
     git config --global user.email "daxpatel.cg@gmail.com"  
     ```
  3. checking configuration:  
     ```
     git config --list
     ```

  Configuration is essential for identifying commits. The `--global` flag applies these settings globally across your system.

---

#### **Task 2: Initialize a Repository**

  1. Created a new folder:  
     ```
     mkdir MyProject && cd MyProject  
     ```
  2. Initialize Git repository:  
     ```
     git init  
     ```
 
  Running `git init` creates a hidden `.git` folder, signaling that the directory is now version-controlled.

---

#### **Task 3: Create a File and Make Multiple Commits**

  1. Create a new file and add content:  
     ```
     echo "My First Project" > README.md  
     git add README.md  
     git commit -m "Initial commit: Added README.md"  
     ```
  2. Modify the file and commit again:  
     ```
     echo "Added a description" >> README.md  
     git add README.md  
     git commit -m "Updated README with a description"  
     ```

  Git tracks changes in stages:
  - **Working Directory**: Where files are edited.
  - **Staging Area**: Files staged using `git add`.
  - **Repository**: Changes committed via `git commit`.

---

#### **Task 4: Check Status and Log**

  1. Check the repository's status:  
     ```bash
     git status  
     ```

  2. View the commit history:  
     ```
     git log --oneline --graph --decorate  
     ```
 
  - `git status` helps identify staged or unstaged changes.  
  - `git log` shows the commit history and branch structure.

---

#### **Task 5: Create and Clone a Repository**

  1. Created a GitHub repo  **Advance-Tasks**.

  2. Clone it:  
     ```bash
     git clone <url>  
     ```
 
  `git clone` copies a remote repository to your local.

---

#### **Task 6: Understanding the Git Workflow**

  1. Make changes:  
     ```bash
     echo "Workflow example" > workflow.md  
     git add workflow.md  
     git commit -m "Added workflow example"  
     ```
 
  The Git workflow consists of making changes, staging them, and committing them to the repository.

---



#### **Task 7: Branching and Merging**

  1. Create and switch to a new branch:  
     ```
     git checkout -b feature-login  
     ```

  2. Add a file and commit:  
     ```
     echo "Login Page" > login.html  
     git add login.html  
     git commit -m "Added login page"  
     ```

  3. Merge the branch into `main`:  
     ```bash
     git checkout main  
     git merge feature-login  
     ```
 
  Branching enables working on new features independently, and merging integrates them into the main codebase.

---

#### **Task 8: Handling Merge Conflicts**

  1. Create conflicting changes in branches `branch-A` and `branch-B`.

  2. Merge them into `main`, resolve conflicts
  manually, and commit:  
     ```
     git add README.md  
     git commit -m "Resolved merge conflict"  
     ```
 
  Merge conflicts occur when two branches edit the same part of a file. Resolving them manually ensures code consistency.

---

#### **Task 9: Renaming and Deleting Branches**

  1. Rename a branch:  
     ```
     git branch -m old-branch-name new-branch-name  
     ```

  2. Delete a branch:  
     ```
     git branch -d feature-login  
     ```

  Renaming and deleting branches.

---



#### **Task 10: Using Git Stash**

  1. Save unfinished work:  
     ```
     git stash  
     ```
  2. View and apply the stash:  
     ```
     git stash list  
     git stash apply  
     ```
  
  Stashing temporarily saves changes, allowing you to switch branches without committing.

---

#### **Task 11: Rewriting History with Interactive Rebase**

  1. Create multiple commits.

  2. Squash them using:  
     ```
     git rebase -i HEAD~3  
     ```
 
  Interactive rebasing edits commit history for a cleaner and more concise log.

---

#### **Task 12: Cherry-Picking Commits**

  1. Pick a specific commit from another branch:  
     ```
     git cherry-pick <commit-hash>  
     ```

  Cherry-picking applies specific commits from one branch to another.

---

#### **Task 13: Tagging Commits**

  1. Tag a commit:  
     ```
     git tag -a v1.0 -m "Version 1.0 release"  
     ```
  2. Push the tag:  
     ```
     git push origin v1.0  
     ```
 
  Tags mark specific commits as important, often for release versions.

---

#### **Task 14: Working with Remote Repositories**

  1. Add a remote repository:  
     ```
     git remote add origin <repo-url>  
     ```
  2. Push changes:  
     ```
     git push origin main  
     ```

  Remote repositories enable collaboration by syncing local changes online.

---

#### **Task 15: Forking and Contributing**

  1. Fork a repository, clone it, make changes, and push a new branch.
  2. Open a pull request on GitHub.
 
  Forking and pull requests contribute to open-source projects collaboratively.

---



#### **Task 16: Simulate Team Collaboration**
 
  

#### **Task 17: Git Ignore**

  1. Create a `.gitignore` file for ignored files like `node_modules/`.
  
  `.gitignore` prevents sensitive or unnecessary files from being tracked.

---