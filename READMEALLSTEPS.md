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
