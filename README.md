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
# Git Task - 3 Branch Merge and Force Delete Documentation

````md id="g8m2xr"
# Git Branch Merge and Force Delete

This documentation demonstrates:
- Creating a feature branch
- Checking available branches
- Committing changes in a branch
- Switching branches
- Merging a feature branch into main
- Verifying merged commits
- Safely deleting a branch
- Creating and force deleting a dummy branch

---

# Step 1: Create a New Feature Branch

Command:
```bash
git checkout -b feature-update
````
<img width="391" height="65" alt="image" src="https://github.com/user-attachments/assets/7009a906-dc33-4e18-a05d-644d8e8f7297" />

Output:

```bash id="o8p9wm"
Switched to a new branch 'feature-update'
```

Explanation:

* Creates and switches to the `feature-update` branch

---

# Step 2: Verify Available Branches

Command:

```bash id="m7pk1o"
git branch
```

Output:

```bash id="4xj6hn"
* feature-update
  main
```

Explanation:

* Displays all local branches
* `*` indicates the currently active branch

---

# Step 3: Stage Changes

Command:

```bash id="khx8a9"
git add .
```

Explanation:

* Adds all modified and new files to staging

---

# Step 4: Commit Changes

Command:

```bash id="8j1xuv"
git commit -m "Fourth Commit"
```

<img width="376" height="116" alt="image" src="https://github.com/user-attachments/assets/98371ee1-cb86-46ad-8b9c-fef2e2cd6a38" />

Output:

```bash id="pq2d1f"
[feature-update 23abb4a] Fourth Commit
```

Explanation:

* Saves staged changes into Git history

Files included:

* Git_log.png
* Git_log_oneline.png
* Second_Commit.png
* Staging_Differences.png
* Staging_specific_Changes.png
* Third_Commit.png
* app.py modifications

---

# Step 5: Switch to Main Branch

Command:

```bash id="rq9l0d"
git checkout main
```

Output:

```bash id="w3p9gs"
Switched to branch 'main'
```

Explanation:

* Switches from `feature-update` to `main`

---

# Step 6: Merge Feature Branch into Main

Command:

```bash id="w8r2bt"
git merge feature-update
```
<img width="409" height="220" alt="image" src="https://github.com/user-attachments/assets/2c6e0bb1-7957-477f-b827-1ef903879e1c" />

Output:

```bash id="b3pxm0"
Updating 4ec4888..23abb4a
Fast-forward
```

Explanation:

* Merges all changes from `feature-update` into `main`
* Fast-forward merge occurred because no conflicting commits existed

---

# Step 7: Verify Merge History

Command:

```bash id="7d4n6y"
git log --oneline
```
<img width="334" height="63" alt="image" src="https://github.com/user-attachments/assets/a4f6d237-f940-4772-833f-90531bb39dc3" />

Output:

```bash id="g5q2he"
23abb4a (HEAD -> main, feature-update) Fourth Commit
4ec4888 Third Commit
e7fcff2 Second Commit
ec0982f First Commit
```

Explanation:

* Displays concise commit history
* Confirms `Fourth Commit` is now part of `main`

---

# Step 8: Delete Feature Branch Safely

Command:

```bash id="7zq0pt"
git branch -d feature-update
```
<img width="383" height="26" alt="image" src="https://github.com/user-attachments/assets/c16437db-6973-424e-9718-2e9fa7bf85d5" />

Output:

```bash id="m4s9ka"
Deleted branch feature-update (was 23abb4a).
```

Explanation:

* Safely deletes the merged branch

---

# Step 9: Create a Dummy Branch

Command:

```bash id="f0v3lm"
git checkout -b dummy-branch
```
<img width="335" height="27" alt="image" src="https://github.com/user-attachments/assets/4a93f2ce-f4af-4757-82aa-bc43eea65402" />

Output:

```bash id="x3y5ru"
Switched to a new branch 'dummy-branch'
```

Explanation:

* Creates a temporary branch for testing force delete

---

# Step 10: Stage Changes in Dummy Branch

Command:

```bash id="v6m8pk"
git add .
```

---

# Step 11: Commit Changes in Dummy Branch

Command:

```bash id="k7j2ow"
git commit -m "dummy commit"
```

Output:

```bash id="h1v9dt"
[dummy-branch e33d2ee] dummy commit
```

Explanation:

* Saves temporary branch changes

---

# Step 12: Switch Back to Main Branch

Command:

```bash id="w4n7qz"
git checkout main
```

Output:

```bash id="d2x8ms"
Switched to branch 'main'
```

---

# Step 13: Force Delete Dummy Branch

Command:

```bash id="t8l1qc"
git branch -D dummy-branch
```
<img width="326" height="44" alt="image" src="https://github.com/user-attachments/assets/d63218bb-08e2-4410-9aa3-2f7a9f292b71" />
Output:

```bash id="n5m3vr"
Deleted branch dummy-branch (was e33d2ee).
```

Explanation:

* Force deletes branch even though it was not merged

---

# Git Commands Summary

```bash id="c6z2qa"
git checkout -b feature-update

git branch

git add .

git commit -m "Fourth Commit"

git checkout main

git merge feature-update

git log --oneline

git branch -d feature-update

git checkout -b dummy-branch

git add .

git commit -m "dummy commit"

git checkout main

git branch -D dummy-branch
```

---

# Important Git Concepts

| Command             | Purpose                  |
| ------------------- | ------------------------ |
| `git checkout -b`   | Create and switch branch |
| `git branch`        | View branches            |
| `git add .`         | Stage all files          |
| `git commit -m`     | Save changes             |
| `git merge`         | Merge branches           |
| `git log --oneline` | View commit history      |
| `git branch -d`     | Safe branch delete       |
| `git branch -D`     | Force branch delete      |

---

# Safe Delete vs Force Delete

| Option | Description                     |
| ------ | ------------------------------- |
| `-d`   | Deletes merged branches safely  |
| `-D`   | Force deletes unmerged branches |

---

# Conclusion

This task demonstrated:

* Branch creation
* Branch switching
* Merging branches
* Viewing commit history
* Safe branch deletion
* Force deleting temporary branches

These operations are essential for effective Git branch management workflows.

```
```
# Git Task - 4 Stash, Reset, Revert, and Commit History Documentation

````md id="z8q4vp"
# Git Stash, Reset, Revert, and Commit History

This documentation demonstrates:
- Stashing changes
- Viewing stash list
- Applying stashed changes
- Creating commits
- Undoing commits using reset
- Reverting commits safely
- Verifying commit history

---

# Step 1: Save Changes Using Git Stash

Command:
```bash
git stash
````
<img width="425" height="28" alt="image" src="https://github.com/user-attachments/assets/e5eb0507-00e8-4991-a3df-5b103616c659" />

Output:

```bash id="q7w2rm"
Saved working directory and index state WIP on main: 23abb4a Fourth Commit
```

Explanation:

* Temporarily saves uncommitted changes
* Cleans the working directory

---

# Step 2: View Stash List

Command:

```bash id="j5t8xp"
git stash list
```
<img width="311" height="27" alt="image" src="https://github.com/user-attachments/assets/87cc72b1-1ae5-45d1-bac3-78d4da98cb46" />

Output:

```bash id="v1m6zk"
stash@{0}: WIP on main: 23abb4a Fourth Commit
```

Explanation:

* Displays all saved stash entries
* `stash@{0}` is the latest stash

---

# Step 3: Apply Stashed Changes

Command:

```bash id="t8x3nv"
git stash apply
```
<img width="440" height="276" alt="image" src="https://github.com/user-attachments/assets/1114ecab-2730-40f0-9f2c-aaa0a0c7a52f" />

Output:

```bash id="h9p4lw"
Changes not staged for commit:
        modified:   app.py

Untracked files:
        Fourth_Commit.png
        Git_log_oneline2.png
        Merge_with_main_branch.png
        New_branch.png
        Safe_delete.png
        dummy_branch.png
        force_delete_branch.png
```

Explanation:

* Restores stashed changes back into the working directory
* Keeps the stash entry saved

---

# Step 4: Stage Restored Changes

Command:

```bash id="p6w1jr"
git add .
```

Explanation:

* Adds all restored and modified files to staging

---

# Step 5: Create Fifth Commit

Command:

```bash id="f2n9xd"
git commit -m "Fifth Commit"
```
<img width="359" height="130" alt="image" src="https://github.com/user-attachments/assets/002824ae-d070-4028-b432-cf50be0d2706" />

Output:

```bash id="g3v7my"
[main 67ef5f6] Fifth Commit
```

Explanation:

* Saves staged files into Git history

Files included:

* Fourth_Commit.png
* Git_log_oneline2.png
* Merge_with_main_branch.png
* New_branch.png
* Safe_delete.png
* dummy_branch.png
* force_delete_branch.png
* app.py changes

---

# Step 6: Add More Changes

Command:

```bash id="s5z8kh"
git add .
```

Explanation:

* Stages additional modifications in `app.py`

---

# Step 7: Create Error Commit

Command:

```bash id="d4q1tn"
git commit -m "error code"
```
<img width="353" height="77" alt="image" src="https://github.com/user-attachments/assets/1df79577-26bb-420a-9f13-5edc48838489" />

Output:

```bash id="l9y3rp"
[main 5b55af4] error code
```

Explanation:

* Creates a commit containing unwanted changes

---

# Step 8: Undo Last Commit Using Reset

Command:

```bash id="x2m6vb"
git reset --hard HEAD~1
```
<img width="355" height="25" alt="image" src="https://github.com/user-attachments/assets/fd64c722-f948-4f13-8be2-54e1e8c56aa0" />

Output:

```bash id="w8n5jk"
HEAD is now at 67ef5f6 Fifth Commit
```

Explanation:

* Removes the latest commit permanently
* Restores repository back to `Fifth Commit`

---

# Step 9: Create Another Commit

Command:

```bash id="c1r7oz"
git add .
```
<img width="375" height="41" alt="image" src="https://github.com/user-attachments/assets/9dafcd4d-5563-428e-81b5-cf7b9043117d" />

```bash id="v5p8da"
git commit -m "error code commit2"
```

Output:

```bash id="m4x0qs"
[main a3a44c8] error code commit2
```

Explanation:

* Creates another commit with changes

---

# Step 10: Revert the Commit Safely

Command:

```bash id="y9k3wv"
git revert HEAD
```
<img width="289" height="38" alt="image" src="https://github.com/user-attachments/assets/9cb2f9f5-043a-4eab-97ff-46df64f26c11" />

Output:

```bash id="e6t1qh"
[main cfb80d8] Revert "error code commit2"
```

Explanation:

* Creates a new commit that reverses the previous commit
* Does not remove commit history

---

# Step 11: Verify Commit History

Command:

```bash id="n7w4pk"
git log --oneline
```
<img width="291" height="121" alt="image" src="https://github.com/user-attachments/assets/1718d5f4-f580-4bab-b4a6-ee932b0669c3" />

Output:

```bash id="u2m8jx"
cfb80d8 Revert "error code commit2"
a3a44c8 error code commit2
67ef5f6 Fifth Commit
23abb4a Fourth Commit
4ec4888 Third Commit
e7fcff2 Second Commit
ec0982f First Commit
```

Explanation:

* Displays concise commit history
* Shows both:

  * Original commit
  * Revert commit

---

# Git Commands Summary

```bash id="o4r2mz"
git stash

git stash list

git stash apply

git add .

git commit -m "Fifth Commit"

git commit -m "error code"

git reset --hard HEAD~1

git add .

git commit -m "error code commit2"

git revert HEAD

git log --oneline
```

---

# Important Git Concepts

| Command                   | Purpose                          |
| ------------------------- | -------------------------------- |
| `git stash`               | Temporarily save changes         |
| `git stash list`          | View stashes                     |
| `git stash apply`         | Restore stashed changes          |
| `git reset --hard HEAD~1` | Remove latest commit permanently |
| `git revert HEAD`         | Create reversing commit          |
| `git log --oneline`       | View commit history              |

---

# Reset vs Revert

| Feature                      | Reset | Revert |
| ---------------------------- | ----- | ------ |
| Removes commit history       | Yes   | No     |
| Creates new commit           | No    | Yes    |
| Safe for shared repositories | No    | Yes    |
| Rewrites history             | Yes   | No     |

---

# Conclusion

This task demonstrated:

* Saving temporary work using stash
* Restoring stashed changes
* Creating commits
* Undoing commits using reset
* Safely reversing commits using revert
* Viewing complete commit history

These operations are essential for advanced Git version control workflows.

```
```


