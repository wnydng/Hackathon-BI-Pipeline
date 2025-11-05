# Working with Git: Pulling & Pushing to Your Own Branch

When contributing to this project, we should create and use **our own branch** instead of working directly on `main`.

## 1. Clone the repository (first time only)

Choose a folder on your machine where you want the project to live (for example, `Documents/Projects/`).  
Run these commands in your terminal (PowerShell, Git Bash, or Linux shell):

```
git clone https://github.com/LisaNaccache/Security_use_cases_project.git
cd Security_use_cases_project
```

This will:
- **Download (clone)** the repository from GitHub to your computer.  
- **Enter the project folder** so you can start working inside it.  

## 2. Create and switch to your own branch
Replace `<your-branch>` with a meaningful name (use your name or the feature you’re working on):
```
git checkout -b <your-branch>
```

## 3. Pull the latest changes from `main`
Before pushing your updates, always make sure your branch is up to date with the `main` branch:
```
git checkout main
git pull origin main
git checkout <your-branch>
git merge main
```

## 4. Stage and commit your changes
```
git add .
git commit -m "Add my feature or fix"
```

## 5. Push your branch to GitHub
```
git push origin <your-branch>
```

## 6. Open a Pull Request
- Go to the repository on GitHub: https://github.com/LisaNaccache/Security_use_cases_project
- Select your branch and click **New Pull Request**.  
- Once reviewed and approved by the whole team, it will be merged into `main`.

## 7. 🔄 Update your Git branch from main

### a. Move to your working branch
```
git checkout dev_name
# → Your branch is up to date with ‘origin/dev_name’.
```

### b. Fetch the latest updates from the remote repository
```
git fetch origin
```

### c. Rebase your branch's commits on top of the main branch (clean option)
```
git rebase origin/main
# → Successfully rebased and updated refs/heads/dev_name.
```

### d. (Optional) Check that everything is up to date
```
git merge origin/main
# → Already up to date.
```
