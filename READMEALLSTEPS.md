# Getting Started

Follow the steps below to set up your Git repository and make initial commits.

---

## 1️⃣ Create a New Git Repository

1. Go to **GitHub** and click on **New Repository**.
2. Enter a repository name (e.g. `Gym-Git-Exercise-Solutions) and create it.
3. Clone the repository to your local machine:

```bash
git clone https://github.com/system-Barinda/Gym-Git-Exercise-Solutions.git
cd Gym-Git-Exercise-Solutions

## 2 Initialize Your Environment

touch test{1..4}.md

## 3 Commit Files Step by Step

git add test1.md
git commit -m "chore: Create initial file"

git add test2.md
git commit -m "chore: Create another file"

git add test3.md test4.md
git commit -m "chore: Create third and fourth files"

## Part 1: Refining Git History (10 Challenges)

###  1. Missing File Fix
## Steps:

```bash
git status         # Check which files are untracked or unstaged
git log --oneline  # Review recent commits

git add test4.md
git commit --amend -m "chore: Add missing test4.md to previous commit"

### 2. Editing Commit History

git rebase -i HEAD~2

# In the editor, change <<pick>> to <<reword>> for the commit you want to modify.
Save and provide a clean message for the combined commit.

###3 . Keeping History Tidy - Squashing Commits:

git rebase -i HEAD~2
Change the second commit from <<pick>> to <<squash>>.
Save and provide a clean message for the combined commit.

###  4. Splitting a Commit

> **"Create third and fourth files"**
But it's better to split it into:
- `"Create third file"`
- `"Create fourth file"`


```bash
git log --oneline         # Identify the commit hash BEFORE the one to split
git reset <hash>  
# Move HEAD back while keeping changes unstaged

git add test3.md
git commit -m "chore: Create third file"

git add test4.md
git commit -m "chore: Create fourth file"

### 5. Advanced Squashing

git rebase -i HEAD~2

Leave the first commit as pick

Change the second to squash (or s)

Write the new combined commit message when prompted

### 6. Dropping a Commit

echo "This is unwanted" > unwanted.txt
git add unwanted.txt
git commit -m "Unwanted commit"

git log --oneline                  //  Identify the commit hash before the unwanted one
git reset --hard <previous-hash>   //  Deletes the unwanted commit entirely


### 7. Reordering Commits

```bash
git rebase -i HEAD~4

In the editor, simply rearrange the lines (each line represents a commit).
Save and exit — Git will replay them in your new order.


### 8. Cherry-Picking Commits

git checkout -b ft/branch
echo "Content for test5" > test5.md
git add test5.md
git commit -m "Implemented test 5"

git checkout dev

** Cherry-pick the commit from ft/branch into main **

git log --oneline ft/branch         # Copy the commit hash of "Implemented test 5"
git cherry-pick <commit-hash>

### 9. Visualizing Commit History (Bonus)

git log --graph --oneline --all

Or use GUI tools like:
GitKraken,Sourcetree,VS Code Git Graph Extension

### 10. Understanding Reflogs (Bonus)

```bash
git reflog

You’ll see entries like:

a1b2c3d HEAD@{0}: commit: Implemented test 5
e4f5g6h HEAD@{1}: reset: moving to previous commit
...



##  Part 2: Branching Basics (10 Challenges)


---

## 1 Feature Branch Creation

Create and switch to a new branch for a feature:

```bash
git checkout -b ft/new-feature

## 2 .Working on the Feature Branch

echo "This is a new feature" > feature.txt
git add feature.txt
git commit -m "Implemented core functionality for new feature"

## 3 Switching Back and Making More Changes

git checkout main
echo "Project Introduction" > readme.txt
git add readme.txt
git commit -m "Updated project readme"

## 4. Local vs. Remote Branches:

git push -u origin ft/new-feature

### 5. Branch Deletion

git branch -d ft/new-feature          // Deletes locally
git push origin --delete ft/new-feature   // Deletes remotely (optional)

### 6. Creating a Branch from a Specific Commit

git log --oneline                     // Copy the commit hash (2 commits back)
git checkout -b ft/new-branch-from-commit <commit-hash>

### 7. Branch Merging

git checkout dev
git merge ft/new-branch-from-commit

### 8. Branch Rebasing

git checkout ft/new-branch-from-commit
git rebase dev

### 9. Renaming Branches

git branch -m ft/new-branch-from-commit ft/improved-branch-name

### 10. Detached HEAD

git checkout <commit-hash>


##  Part 3: Advanced Workflows (10+ Challenges)

This section covers **real-world scenarios** involving stashing, conflict resolution, tagging, ignoring files, and remote collaboration.

---

### 1️⃣ Stashing Changes

Save your uncommitted work temporarily:

```bash
git stash

### 2️⃣ Retrieving Stashed Changes

git stash pop

### 3️⃣ Simulating Merge Conflicts

git checkout main
git merge <branch-name>

### 4️⃣ Using a Merge Tool (Optional)

git mergetool

### 5️⃣ Understanding Detached HEAD

git checkout <commit-hash>
git checkout dev








