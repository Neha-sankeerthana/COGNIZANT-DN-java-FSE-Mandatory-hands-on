# Git Hands-on Lab 3 - Branching and Merging

## Objective

This project demonstrates how to work with Git branches by creating a new branch, making changes, comparing branches, merging changes into the main branch, and deleting the feature branch.

---

## Tools Used

- Git
- Git Bash
- GitHub
- Notepad++

---

## Project Structure

```
GitDemo/
│
├── welcome.txt
├── branch.txt
├── .gitignore
├── error.log
└── logs/
    └── app.log
```

---

## Tasks Performed

### 1. Created a new Git branch

```
git branch GitNewBranch
```

---

### 2. Switched to the new branch

```
git checkout GitNewBranch
```

---

### 3. Created a new file

```
branch.txt
```

Content:

```
This file is created in GitNewBranch
```

---

### 4. Added and committed the file

```
git add branch.txt
git commit -m "Added branch.txt in GitNewBranch"
```

---

### 5. Compared branches

```
git diff main GitNewBranch
```

---

### 6. Merged the branch into main

```
git checkout main
git merge GitNewBranch
```

---

### 7. Viewed commit history

```
git log --oneline --graph --decorate
```

---

### 8. Deleted the merged branch

```
git branch -d GitNewBranch
```

---

### 9. Verified repository status

```
git status
```

---

### 10. Pushed changes to GitHub

```
git push
```

---

## Git Commands Used

```
git branch GitNewBranch
git checkout GitNewBranch
echo "This file is created in GitNewBranch" > branch.txt
git add branch.txt
git commit -m "Added branch.txt in GitNewBranch"
git checkout main
git diff main GitNewBranch
git merge GitNewBranch
git log --oneline --graph --decorate
git branch -d GitNewBranch
git status
git push
```

---

## Learning Outcomes

- Created a Git branch
- Switched between branches
- Added and committed changes
- Compared branches using Git Diff
- Merged a branch into the main branch
- Viewed commit history
- Deleted a merged branch
- Pushed changes to GitHub

---

## Repository

GitHub Repository:
https://github.com/Neha-sankeerthana/GitDemo

---

## Author

**Neha Sankeerthana**
