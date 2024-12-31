# Git Folder Merge Guide

This guide outlines how to merge a specific folder from one branch to another in Git. It is useful when you need to merge only a specific directory (folder) without merging the entire branch.

## Steps to Merge a Specific Folder

### 1. Switch to the Target Branch

First, ensure you're on the branch where you want to merge the folder into (e.g., `main` branch). You can switch branches using the following command:

`git checkout main`

Note: Replace main with the name of the target branch if it's different.

### 2. Ensure Your Target Branch is Up-to-Date

Fetch the latest changes from the remote repository and update your local branch to ensure you’re working with the most recent version.

`git pull origin main`

Note: Replace main with the name of your target branch if necessary.

### 3. Merge the Folder from the Source Branch

Now, use the git checkout command to check out only the folder from the source branch. Replace source-branch with the name of the branch you want to merge from (e.g., portfolio), and path/to/folder with the relative path to the folder you want to merge (e.g., portfolio).

`git checkout source-branch -- path/to/folder`

For example, if you want to merge the portfolio folder from the portfolio branch into the main branch, the command would look like this:

`git checkout portfolio -- portfolio`

### 4. Stage the Changes

After checking out the folder, Git will stage the changes automatically. If for some reason it doesn't, you can manually stage the changes by running:

`git add path/to/folder`

For example:
`git add portfolio`

### 5. Commit the Changes

Once the changes are staged, commit them with a meaningful commit message:

`git commit -m "Merge portfolio folder from portfolio branch"`

### 6. Push the Changes to the Remote Repository

After committing, push the changes to the remote repository:

`git push origin main`
