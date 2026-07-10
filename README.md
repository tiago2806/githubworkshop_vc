# GitHub Workshop — Branches, Commits, Push and Pull Requests

This repository was created for an introductory workshop about Git and GitHub, with a focus on team collaboration.

The main goal is for all participants to learn how to work with branches, make changes to a project, push those changes to GitHub, and open a Pull Request.
This will increases the efficiency of process of developing the projects.

---

## Workshop Goal

By the end of this workshop, each participant should be able to:

* Clone a GitHub repository.
* Open the project in VS Code.
* Use the VS Code terminal.
* Create a branch.
* Make changes to a file.
* Use `git status` to check changes.
* Use `git add`.
* Create a commit.
* Use `git push`.
* Open a Pull Request on GitHub.
* Understand the review and merge process.
* Update the `main` branch after a merge.

---

## Main Concepts

### Git

Git is a version control tool. It allows you to save the history of changes in a project and collaborate with other people.

### GitHub

GitHub is an online platform where Git repositories can be stored and where teams can collaborate.

### Repository

A repository is the project folder containing the files, code, and history of changes.

### Branch

A branch is a separate line of work. It allows you to make changes without directly affecting the main version of the project.

### Main

The `main` branch is the main branch of the project. It should represent the stable version of the repository.

### Pull Request

A Pull Request is a request to merge changes from one branch into another. It also allows team members to review code, leave comments, and approve changes before merging.

---

## Main Rule

Never work directly on the `main` branch.

The correct workflow is:

```text
main → create branch → make changes → commit → push → Pull Request → review → merge
```

---

## Exercise

This repository has the following structure:

```text
githubworkshop_vc/
│
├── README.md
├── members/
│   └── example.md
├── message.md
└── tasks.md
```

### `members/` Folder

Each participant should create a file with their name inside this folder.

Example:

```text
members/jaime.md
members/maria.md
members/joao.md
```

---

## Part 1 — Clone the Repository

Open the terminal in VS Code or on your computer and run:

```bash
git clone repository_url
```

Then enter the project folder:

```bash
cd githubworkshop_vc
```
Nota: cd means "change directory". It allows to move between folders. It is like clicking in a folder in your pc.

Open the project in VS Code:

```bash
code .
```

---

## Part 2 — Check the Current Branch

To see which branch you are currently on:

```bash
git branch
```

To move between branches (ex: move to main):

```bash
git checkout main
```

Update the `main` branch:

```bash
git pull origin main
```

---

## Part 3 — Create a Branch

Each participant should create their own branch.

Example:

```bash
git checkout -b feature/add-jaime
```

Replace `jaime` with your own name.

Other examples:

```bash
git checkout -b feature/add-maria
git checkout -b feature/add-joao
git checkout -b docs/update-readme
```

---

## Part 4 — Create Your Profile File

Inside the `members/` folder, create a .py file with your name.

Example:

```text
members/jaime.py
```

Inside the file, write something like:

```md
# Jaime

print("Hello my name is Jaime")
```

---

## Part 5 — Check Your Changes

After creating or editing the file, run:

```bash
git status
```

This command shows the files that have been changed.
Shows if you have any changes that you still need to push (send online) and if there are changes online that you still haven't pulled (get that online changes into your local pc)

---

## Part 6 — Add Your Changes

To prepare all changed files for the commit:

```bash
git add .
```

---

## Part 7 — Create a Commit

Create a commit with a clear message:

```bash
git commit -m "Add Jaime profile"
```

Examples of good commit messages:

```bash
git commit -m "Add member profile"
git commit -m "Update workshop instructions"
git commit -m "Fix typo in README"
```

Avoid vague messages like:

```bash
git commit -m "changes"
git commit -m "final"
git commit -m "stuff"
```

---

## Part 8 — Push Your Branch

The first time you push your branch to GitHub, run:

```bash
git push -u origin feature/add-jaime
```

After that, if you make more commits in the same branch, you can simply run:

```bash
git push
```

---

## Part 9 — Open a Pull Request

After pushing your branch, go to GitHub.

Usually, GitHub will show a button saying:

```text
Compare & pull request
```

Click that button and create the Pull Request.

The Pull Request should have:

* A clear title.
* A simple description of what was changed.
* The correct source branch.
* `main` as the target branch.

Example title:

```text
Add Jaime profile
```

Example description:

```md
This Pull Request adds my member profile to the members folder.
```

---

## Part 10 — Review and Merge

After the Pull Request is opened:

1. Another person should review the changes.
2. They can leave comments or suggestions.
3. If everything is correct, the Pull Request can be approved.
4. Then, the Pull Request can be merged into the `main` branch.

After the merge, the branch can be deleted on GitHub.

---

## Part 11 — Update `main` After the Merge

After the Pull Request has been accepted and merged, everyone should update their local `main` branch:

```bash
git checkout main
git pull origin main (it can be just git pull) git pull retrieves all changes from all branches, not only on a specific branch
```

This ensures your computer has the latest version of the project.

---

## Essential Commands

```bash
# Clone repository
git clone REPOSITORY_URL

# Enter project folder
cd github-workshop

# Check file status
git status

# See branches
git branch

# Switch to main
git checkout main

# Update main
git pull origin main

# Create a new branch
git checkout -b feature/task-name

# Add changes
git add .

# Create commit
git commit -m "Clear message"

# Push branch to GitHub
git push -u origin branch-name

# Push new commits after the first push
git push

# Go back to main
git checkout main

# Delete local branch after merge
git branch -d branch-name
```

---

## Best Practices

* Do not work directly on `main`.
* Create one branch for each task.
* Use clear branch names.
* Make small and focused commits.
* Write clear commit messages.
* Run `git pull origin main` before starting a new task.
* Open a Pull Request before merging.
* Ask another person to review your Pull Request.
* Resolve conflicts carefully.
* Delete old branches after they are merged.

---


## Final Workflow to Remember

```text
1. git checkout main
2. git pull origin main
3. git checkout -b feature/task-name
4. Make changes
5. git status
6. git add .
7. git commit -m "Clear message"
8. git push -u origin feature/task-name
9. Open a Pull Request on GitHub
10. Review the Pull Request
11. Merge the Pull Request
12. git checkout main
13. git pull origin main
```

---

## Expected Outcome

By the end of the workshop, all participants should be able to collaborate on a GitHub repository using branches and Pull Requests.

The goal is not to memorize every Git command, but to understand the basic collaboration workflow used in real projects.

