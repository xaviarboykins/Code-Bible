# Git Workflow

## Create a New Branch

1. **Create a New Branch**
    ```sh
    git checkout <branchName>
    ```
    - **Note**: Ensure `<branchName>` is the correct base branch, like `main` or `master`.

    ```sh
    git checkout -b <newBranchName>
    ```
    - **Note**: This combines branch creation and checkout into one command.

2. **Perform Task**
    - Make necessary changes (add features, refactor code, or fix bugs).

3. **Verify Changes**
    ```sh
    git status
    ```
    - **Note**: This shows the status of your working directory and staging area.

## Stage and commit changes

4. **Stage Changes for Commit**
    ```sh
    git add <fileName>  # For specific files
    git add -A          # For all changes
    ```
    - **Note**: Stages changes for commit.

    ```sh
    git status
    ```
    - **Note**: Confirm staged files appear green.

5. **Commit Changes**
    ```sh
    git commit -m "<message>"
    ```
    - **Note**: Commit changes with a descriptive message.

## Push file to repo

6. **Push Changes to the Feature Branch**
    ```sh
    git push origin <newBranchName>
    ```
    - **Note**: Push your local branch to the remote repository.

7. **Create a Pull Request (PR)**
    - **Note**: Go to GitHub (or other hosting service) and create a Pull Request from your feature branch to the base branch (e.g., `main`).
  
## Merge conflicts

8. **Merging Manually to Main (for Conflict Resolution)**
    ```sh
    git checkout main
    git pull origin main
    git checkout <featureBranchName>
    git merge main
    ```
    - **Note**: Switch to the main branch, pull the latest changes, switch back to the feature branch, and merge the main branch into the feature branch.

9. **Resolve Conflicts if Any**
    - Edit conflicting files to resolve issues.
    - Mark conflicts as resolved using:
      ```sh
      git add <resolvedFile> or git add -A
      ```

10. **Verify There Are No More Conflicts**
    ```sh
    git status
    ```

11. **Push the Changes for New PR**
    ```sh
    git push origin <featureBranchName>
    ```
    - **Note**: Push changes to update the PR.

This workflow helps keep changes organized and manageable, improving version control and collaboration.
