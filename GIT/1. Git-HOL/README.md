# GitDemo

## Overview

GitDemo is a simple Git hands-on project created as part of the **Cognizant Digital Nurture 4.0 Java FSE Mandatory Hands-on Lab**. The project demonstrates the basic workflow of Git version control, including repository initialization, file tracking, committing changes, and pushing the project to a remote GitHub repository.

---

## Objectives

- Install and configure Git.
- Configure Git user information.
- Set Notepad++ as the default Git editor.
- Initialize a local Git repository.
- Create and track files.
- Commit changes to the local repository.
- Connect the local repository to GitHub.
- Push the project to a remote GitHub repository.

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
└── README.md
```

---

## Git Commands Used

### Check Git Version

```bash
git --version
```

### Configure Git Username

```bash
git config --global user.name "Your Name"
```

### Configure Git Email

```bash
git config --global user.email "youremail@example.com"
```

### Initialize Repository

```bash
git init GitDemo
```

### Navigate to Repository

```bash
cd GitDemo
```

### Create File

```bash
echo "Welcome to the version control" > welcome.txt
```

### Check Repository Status

```bash
git status
```

### Add File to Staging Area

```bash
git add welcome.txt
```

### Commit Changes

```bash
git commit -m "Initial commit"
```

### Connect Remote Repository

```bash
git remote add origin https://github.com/<your-username>/GitDemo.git
```

### Rename Branch

```bash
git branch -M main
```

### Push to GitHub

```bash
git push -u origin main
```

---

## Output

- Successfully initialized a Git repository.
- Created and tracked the `welcome.txt` file.
- Committed the project to the local repository.
- Connected the project to GitHub.
- Successfully pushed the project to the remote repository.

---

## Repository

GitHub Repository:

```
https://github.com/Neha-sankeerthana/GitDemo
```

---

## Learning Outcomes

- Understood the fundamentals of Git version control.
- Learned Git configuration and repository initialization.
- Gained experience with staging and committing files.
- Learned how to connect a local repository to GitHub.
- Successfully pushed a project to a remote repository.

---

## Author

**Neha Sankeerthana**

GitHub: https://github.com/Neha-sankeerthana

---

## Acknowledgement

This project was completed as part of the **Cognizant Digital Nurture 4.0 Java Full Stack Engineer (FSE) Mandatory Hands-on Program** to gain practical experience with Git and GitHub version control.
