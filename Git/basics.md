# Git Learning Notes (Basic → Intermediate → Advanced)

---

# 🟢 BASIC LEVEL

### **1. Introduction to Git**

* What is Git?
* Why use version control?
* Difference between Git and GitHub

### **2. Git Installation & Setup**

* Install Git
* Configure user details:

  ```bash
  git config --global user.name "Your Name"
  git config --global user.email "you@example.com"
  ```

### **3. Basic Git Commands**

* Initialize repository

  ```bash
  git init
  ```
* Check status

  ```bash
  git status
  ```
* Add files

  ```bash
  git add .
  ```
* Commit changes

  ```bash
  git commit -m "message"
  ```
* View commit history

  ```bash
  git log
  ```

### **4. Understanding the Git Workflow**

* Working Directory
* Staging Area
* Local Repository

### **5. Basic Undo Operations**

* Unstage file:

  ```bash
  git reset HEAD file
  ```
* Undo last commit (keep changes):

  ```bash
  git reset --soft HEAD~1
  ```

---

#  🟡 INTERMEDIATE LEVEL

### **1. Branching**

* Create branch:

  ```bash
  git branch feature-login
  ```
* Switch branch:

  ```bash
  git checkout feature-login
  ```
* Create + switch:

  ```bash
  git checkout -b feature-login
  ```
* List branches:

  ```bash
  git branch
  ```

### **2. Merging**

* Merge a branch into main:

  ```bash
  git checkout main
  git merge feature-login
  ```
* Fast-forward vs non-fast-forward merge

### **3. Collaboration (Remote Repos)**

* Add remote:

  ```bash
  git remote add origin URL
  ```
* Push commits:

  ```bash
  git push origin main
  ```
* Push branch:

  ```bash
  git push origin feature-login
  ```
* Pull changes:

  ```bash
  git pull
  ```
* Clone repo:

  ```bash
  git clone URL
  ```

### **4. Git Ignore**

* Create `.gitignore`
* Ignore files & folders:

  ```
  node_modules/
  .env
  *.log
  ```

### **5. Basic Conflict Resolution**

* Why conflicts occur
* Conflict markers:

  ```
  <<<<<<< HEAD
  Your changes
  =======
  Incoming changes
  >>>>>>> branch-name
  ```
* Steps to resolve:

  1. Edit file
  2. Remove markers
  3. Add file
  4. Commit merge

---

#  🔵 ADVANCED LEVEL

### **1. Rebasing**

* Rebase is used to rewrite commit history and make it cleaner.
* What rebase does:
    1. Moves your commits on top of another branch.
    2. Makes history linear and clean.
* Rebase branch with main:

  ```bash
  git checkout feature-login
  git rebase main
  ```
* Fix conflicts during rebase
* Abort rebase:

  ```bash
  git rebase --abort
  ```

### **2. Cherry Pick**

* Cherry-pick lets you take a specific commit from one branch and apply it to another.
* Apply specific commit to another branch:

  ```bash
  git cherry-pick <commit-id>
  ```

### **3. Stashing**
* Stash temporarily saves your work without committing.
* Example : You are changing a file but suddenly need to switch branches. 

* Save work temporarily:

  ```bash
  git stash
  ```
* Apply stashed work:

  ```bash
  git stash apply
  ```
* List stashes:

  ```bash
  git stash list
  ```

### **4. Advanced Undo Operations**
* Soft reset:
    * Keeps your code, only removes commit.
    ```bash
    git reset --soft HEAD~1
    ```

* Hard reset:
    * Deletes code and commit
  ```bash
  git reset --hard HEAD~1
  ```
* Revert commit (safe):
    * Safely undo a commit by creating a new commit.
  ```bash
  git revert <commit-id>
  ```

### **5. Version Tagging**

* Tags are like milestones or release markers in a project.
* Tags in Git are like bookmarks or labels that you attach to specific commits.

    ### How Tagging Works Internally:
    * A tag always points to a single commit, NOT a branch.

    * So even if your code changes later, the tag remains at the exact commit.

    ```bash {.bg-black}
        A---B---C---D---E (main)
                    |
                tag: v1.0
    ```

    * Even if new commits F, G, H come, v1.0 still stays on commit C.

* Create annotated tag:

  ```bash
  git tag -a v1.0 -m "Release 1.0"
  ```
* Push tags:

  ```bash
  git push origin --tags
  ```
* Delete tag:

  ```bash
  git tag -d v1.0
  git push origin :refs/tags/v1.0
  ```

### **6. Git Workflows**

* Git Flow
* Trunk-based development
* Feature branching

### **7. Pull Requests (PRs)**

* Code review process
* Squash & merge
* Rebase & merge

---

# 📌 Summary Checklist

### **Basic**

* Git init, add, commit, log, status
* Staging & repository concepts

### **Intermediate**

* Branching & merging
* Collaboration with GitHub
* Handling conflicts

### **Advanced**

* Rebasing, cherry pick, stash
* Tags & release management
* PR workflows

---
