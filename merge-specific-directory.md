# Merging Only a Specific Directory into Main

### 1. Switch to the Feature Branch
Make sure you’re on the feature branch where the changes are made.

git checkout your-feature-branch

### 2. Stage Changes for the `specified-branch` Directory
Add only the `example-dir` folder to the staging area.

git add example-dir/

### 3. Commit Changes
Commit the changes for `example-dir` with a meaningful message.

git commit -m “Update example-dir directory”

### 4. Switch to `main` Branch
Move back to the `main` branch.

git checkout main

### 5. Merge the Feature Branch into `main`
Merge the changes from the feature branch into `main`. The `--no-ff` option ensures a separate merge commit, preserving history.

git merge –no-ff your-feature-branch

### 6. Push the Changes to Remote
Push the merged changes to the remote repository.

git push origin main

---

By following these steps, only the changes made in the `example-dir` directory will be merged into the `main` branch, and the other directories will remain unaffected.
