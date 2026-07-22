# Git Ignore Hands-on Lab

## Overview

This project demonstrates the use of the **.gitignore** file in Git to exclude unnecessary files and directories from version control. It is part of the **Cognizant Digital Nurture 4.0 Java Full Stack Engineer (FSE) Mandatory Hands-on Program**.

The project illustrates how Git ignores log files and folders specified in the `.gitignore` file while tracking only the required project files.

---

## Objectives

- Understand the purpose of the `.gitignore` file.
- Create files and directories that should not be tracked by Git.
- Configure Git to ignore specific file types and folders.
- Verify that ignored files are excluded from version control.
- Commit and push the `.gitignore` configuration to GitHub.

---

## Technologies Used

- Git
- Git Bash
- GitHub
- Notepad++
- Windows 11

---

## Project Structure

```
GitDemo/
│── welcome.txt
│── .gitignore
│── README.md
├── logs/
│   └── app.log
└── error.log
```

> **Note:** The `logs/` folder and `error.log` file are ignored by Git and are not uploaded to the remote repository.

---

## .gitignore Configuration

The `.gitignore` file contains the following rules:

```text
*.log
logs/
```

### Explanation

- `*.log` ignores all files with the `.log` extension.
- `logs/` ignores the entire `logs` directory and its contents.

---

## Git Commands Used

### Navigate to the Repository

```bash
cd ~/Desktop/GitDemo
```

### Create a Log File

```bash
touch error.log
```

### Create a Logs Directory

```bash
mkdir logs
```

### Create a Log File Inside the Directory

```bash
cd logs
touch app.log
cd ..
```

### Check Repository Status

```bash
git status
```

### Create the .gitignore File

```bash
notepad++ .gitignore
```

### Verify the .gitignore File

```bash
cat .gitignore
```

### Stage the .gitignore File

```bash
git add .gitignore
```

### Commit Changes

```bash
git commit -m "Added .gitignore file"
```

### Push to GitHub

```bash
git push
```

---

## Expected Output

Before creating `.gitignore`:

```text
Untracked files:
    error.log
    logs/
```

After creating `.gitignore`:

```text
Untracked files:
    .gitignore
```

This confirms that Git is successfully ignoring the specified files and folders.

---

## Learning Outcomes

After completing this exercise, the following concepts were learned:

- Purpose of the `.gitignore` file.
- Ignoring specific file extensions.
- Ignoring entire directories.
- Managing tracked and untracked files.
- Using Git commands to stage, commit, and push changes.
- Best practices for maintaining clean Git repositories.

---

## Repository

GitHub Repository:

```
https://github.com/Neha-sankeerthana/GitDemo
```

---

## Author

**Neha Sankeerthana**

GitHub: https://github.com/Neha-sankeerthana

---

## Acknowledgement

This project was completed as part of the **Cognizant Digital Nurture 4.0 Java Full Stack Engineer (FSE) Mandatory Hands-on Program** to gain practical experience with Git version control and the use of `.gitignore` for managing untracked files.
