# Git Task 1 - README Documentation

````md
# Git Task 1

This project demonstrates the basic Git workflow:
- Initializing a Git repository
- Checking repository status
- Staging files
- Creating commits
- Renaming branches
- Connecting to a remote GitHub repository
- Pushing code to GitHub

---

## Step 1: Initialize Git Repository

Command:
```bash
git init
````

Output:

```bash
Initialized empty Git repository in C:/Users/pavan/Git_Task1/.git/
```

Explanation:

* Creates a new local Git repository
* Generates a hidden `.git` folder to track project changes

---

## Step 2: Check Git Status

Command:

```bash
git status
```

Output:

```bash
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        app.py
```

Explanation:

* Shows the current repository status
* Displays untracked files
* Indicates no commits have been created yet

---

## Step 3: Stage Files

Command:

```bash
git add .
```

Explanation:

* Adds all project files to the staging area
* Prepares files for commit

---

## Step 4: Commit Changes

Command:

```bash
git commit -m "First Commit"
```
<img width="385" height="55" alt="image" src="https://github.com/user-attachments/assets/6f0a98ad-d686-4988-a585-403d3f073e83" />

Output:

```bash
[master (root-commit) ec0982f] First Commit
 1 file changed, 1 insertion(+)
 create mode 100644 app.py
```

Explanation:

* Saves the staged files into Git history
* `"First Commit"` is the commit message

---

## Step 5: Rename Branch to Main

Command:

```bash
git branch -m main
```

Explanation:

* Renames the default branch from `master` to `main`

---

## Step 6: Add Remote Repository

Command:

```bash
git remote add origin https://github.com/srinivassriaddepalli-creator/Git_Task1.git
```

Explanation:

* Connects the local repository to the remote GitHub repository
* `origin` is the default remote repository name

---

## Step 7: Push Code to GitHub

Command:

```bash
git push -u origin main
```

<img width="464" height="117" alt="image" src="https://github.com/user-attachments/assets/cc3081f7-af2b-43c7-bbae-dab8f9c38d2e" />

Output:

```bash
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 245 bytes | 81.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)

To https://github.com/srinivassriaddepalli-creator/Git_Task1.git
 * [new branch]      main -> main

branch 'main' set up to track 'origin/main'.
```

Explanation:

* Uploads local repository files to GitHub
* `-u` sets the upstream branch
* Future pushes can be done using:

```bash
git push
```

---

## Git Workflow Summary

```bash
git init
git status
git add .
git commit -m "First Commit"
git branch -m main
git remote add origin <repository_url>
git push -u origin main
```

---

## Technologies Used

* Git
* GitHub
* Python
* VS Code

---

## Author

Pavan

```
```
