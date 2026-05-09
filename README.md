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
# Git Task 2 - Tracking Changes and Commit History

````md id="xv9j2l"
# Git Task 1 - Tracking Changes and Commit History

This documentation demonstrates:
- Checking modified files using Git
- Viewing file differences
- Staging specific changes interactively
- Creating multiple commits
- Viewing commit history

---

# Step 1: Check Git Status

Command:
```bash
git status
````

Output:

```bash id="z5zv8i"
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
        modified:   app.py

Untracked files:
        Git_Push_command.png
        Git_commit_command.png
```

Explanation:

* `app.py` has been modified
* Two image files are untracked
* Changes are not yet staged for commit

---

# Step 2: View File Differences

Command:

```bash id="7j2v6t"
git diff
```
<img width="355" height="132" alt="image" src="https://github.com/user-attachments/assets/e4151b5b-3bb3-483a-a19c-0afad28905d4" />

Output:

```diff id="h5h69h"
diff --git a/app.py b/app.py

-print("Sample Code")
+print("Sample Code")
+print("New Functionality")
```

Explanation:

* `+` indicates newly added lines
* Shows the exact changes made in `app.py`

---

# Step 3: Stage Specific Changes Interactively

Command:

```bash id="6s0f43"
git add -p
```
<img width="482" height="170" alt="image" src="https://github.com/user-attachments/assets/a54d8ff1-ad06-4b54-8036-bb4bdf641d57" />

Output:

```bash id="y9w2m6"
Stage this hunk [y,n,q,a,d,e,p,P,?]? y
```

Explanation:

* `git add -p` enables partial staging
* Allows selecting specific code changes to stage

Common Options:

| Option | Description                    |
| ------ | ------------------------------ |
| y      | Stage current change           |
| n      | Skip current change            |
| q      | Quit staging                   |
| a      | Stage all remaining changes    |
| d      | Do not stage remaining changes |
| e      | Edit patch manually            |

---

# Step 4: Create Second Commit

Command:

```bash id="m5l8z0"
git commit -m "Second Commit"
```
<img width="447" height="59" alt="image" src="https://github.com/user-attachments/assets/48f84784-ef81-404a-bf5b-ccf3bed072c5" />

Output:

```bash id="1lfx0m"
[main e7fcff2] Second Commit
 1 file changed, 2 insertions(+), 1 deletion(-)
```

Explanation:

* Saves the staged changes into Git history
* Commit message: `"Second Commit"`

---

# Step 5: Stage Remaining Files

Command:

```bash id="eqrr7f"
git add .
```

Explanation:

* Adds all remaining modified and untracked files

Files added:

* `Git_Push_command.png`
* `Git_commit_command.png`

---

# Step 6: Create Third Commit

Command:

```bash id="aj9cr7"
git commit -m "Third Commit"
```
<img width="470" height="65" alt="image" src="https://github.com/user-attachments/assets/7069081d-b4bd-4fe9-8c13-f7e14c85fd75" />

Output:

```bash id="x2kr9u"
[main 4ec4888] Third Commit
 3 files changed, 2 insertions(+)

create mode 100644 Git_Push_command.png
create mode 100644 Git_commit_command.png
```

Explanation:

* Commits image files and remaining changes
* Git now tracks the newly added files

---

# Step 7: View Full Commit History

Command:

```bash id="7u8i0q"
git log
```
<img width="413" height="237" alt="image" src="https://github.com/user-attachments/assets/196527c4-f982-4f6c-9fbc-727f030356d6" />

Output:

```bash id="6q3rf5"
commit 4ec4888 - Third Commit
commit e7fcff2 - Second Commit
commit ec0982f - First Commit
```

Explanation:

* Displays detailed commit history
* Includes:

  * Commit ID
  * Author
  * Date
  * Commit message

---

# Step 8: View Short Commit History

Command:

```bash id="mt0sk9"
git log --oneline
```
<img width="308" height="65" alt="image" src="https://github.com/user-attachments/assets/b7a8a946-2363-4d48-80df-0f2d113cdaf6" />

Output:

```bash id="m8g0rr"
4ec4888 Third Commit
e7fcff2 Second Commit
ec0982f First Commit
```

Explanation:

* Displays concise commit history
* Useful for quick reference

---

# Git Commands Summary

```bash id="o5g8zz"
git status
git diff
git add -p
git commit -m "Second Commit"
git add .
git commit -m "Third Commit"
git log
git log --oneline
```

---

# Key Git Concepts

| Command             | Purpose                 |
| ------------------- | ----------------------- |
| `git status`        | Check repository status |
| `git diff`          | View code changes       |
| `git add -p`        | Stage specific changes  |
| `git add .`         | Stage all changes       |
| `git commit`        | Save changes            |
| `git log`           | View detailed history   |
| `git log --oneline` | View short history      |

---

# Conclusion

This task demonstrated:

* Tracking modified files
* Comparing file changes
* Interactive staging
* Creating multiple commits
* Viewing Git commit history

These commands form the foundation of daily Git workflows.

```
```

