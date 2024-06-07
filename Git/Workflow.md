# Git Workflow

## Create a New Branch

1. Navigate to the base branch:
    ```sh
    git checkout <branchName>
    ```
    This step ensures you are on the branch you want to branch off of (e.g., `main`, `master`, or another branch).

2. Create a new branch:
    ```sh
    git checkout -b <newBranchName>
    ```
    This creates a new branch and switches to it.

## Perform Task

- Make your changes. This step involves performing the tasks you need, such as adding features, refactoring code, or fixing bugs.

## Verify Changes

- Check the status:
    ```sh
    git status
    ```
    This shows the changes you have made (untracked, modified, or deleted files).

## Stage Changes for Commit

1. Stage changes:
    ```sh
    git add <fileName>  # For specific files
    git add -A          # For all changes
    ```
    This stages the files for commit.

2. Verify staged files:
    ```sh
    git status
    ```
    Staged files should appear green.

## Commit Changes

- Commit the changes:
    ```sh
    git commit -m "<message>"
    ```
    This creates a commit with a descriptive message about the changes.

## Push Changes to the Feature Branch

- Push the changes:
    ```sh
    git push origin <newBranchName>
    ```
    This uploads your local branch to the remote repository.

## Create a Pull Request (PR)

- Continue to GitHub (or other hosting service) and create a Pull Request from your feature branch to the base branch (e.g., `main`).

## Merging Manually to Main (for Conflict Resolution)

1. Switch to the main branch:
    ```sh
    git checkout main
    ```

2. Update the local version of the main branch:
    ```sh
    git pull origin main
    ```
    
2. Switch back to feature branch:
    ```sh
    git checkout <featureBranchName>
    ```

3. Merge the main branch into the feature branch:
    ```sh
    git merge main
    ```

4. Resolve conflicts if any:
    - Edit the conflicting files to resolve the issues.
    - Mark the conflicts as resolved using:
      ```sh
      git add <resolvedFile> or git add -A
      ```

5. Verify there are no more conflicts:
    ```sh
    git status
    ```

6. Push the changes for new PR:
    ```sh
    git push origin <featureBranchName>
    ```

This workflow ensures that changes are isolated to a specific branch until they are ready to be integrated into the main codebase, facilitating better version control and collaboration.
```
