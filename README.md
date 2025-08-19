# Git and GitHub

## What is Git?

- An open-source and free source control management (SCM). Used to manage changes to files over time. It also allows you to recall specific versions later or even go back to see what those changes were.

## Git and GitHub Key Concepts and Benefits

1. Tracking Changes:

   - Meticulously records every modification to a file or set of files, creating a history of changes.

2. Reverting to Previous Versions:

   - If a mistake is made or a previous version is needed, git allows you to easily revert to a specific point in the project's history.

3. Collaboration:

   - Git enables multiple team members to work on the same project simultaneously, tracking who made which changes and facilitating the merging of contributions.

4. Branching:

   - It allows for the creation of branches, which are separate lines of development, enabling teams to work on new features or bug fixes without affecting the main codebase.

5. Conflict Resolution:

   - When merging changes from different branches, conflicts can arise. Git provides tools to resolve these conflicts, ensuring that the final code is consistent and functional.

6. Reproducibility:

   - Helps ensure that a project can be reproduced at any point in its history, which is crucial for testing, debugging, and maintaining consistent results.

7. Reduced Development Time:

   - By streamlining collaboration and providing tools for efficient code management, it can significantly reduce development time and increase productivity.

8. Enhanced Code Quality:

   - Encourages developers to be more mindful of their changes, leading to better code quality and fewer errors.

9. Backup and Recovery

   - Acts as a backup system, allowing you to recover lost or corrupted files and revert to a previous working state

## Git basics

- **clone** – Copy a remote repository to your local machine.
  `git clone <repository-url>`
- **branching** – Create separate lines of development.
  `git branch <branch-name>`
- **checkout** - Switch from one branch to another. `git checkout <branchname>`
- **add** – Stage changes to be included in the next commit.
  `git add <filename>`. If the changes are in a single file, simply use `git add .`
- **commit** – Save staged changes to the local repository with a descriptive message.
  `git commit -m "your message"`. The `-m` notes that you're adding a description of the commit you've made.
- **push** – Upload your local commits to a remote repository. `git push -u origin <branchname>` when you're creating the branch for the first time and it's not already on the remote repo. Use `git push` to an already created branch.
- **pull** – Fetch and merge changes from a remote repository to your local copy. Use
  `git pull` when working from the same branch. `git pull origin <branchname>` when fetching from a different branch.

## GitHub workflows

- **Forks** – Create a personal copy of the original or someone else's repository. Useful for proposing changes or experimenting without affecting the original project.
- **Pull Requests** – Submit your changes for review and merging into the original repository. Enables collaboration and code review.
- **Issues** – Track bugs, feature requests, and tasks. Issues help organize and prioritize work within a repository.

## Conflict resolution and merge strategies

- **Conflicts** occur when changes in different branches affect the same lines of code. Git will pause the merge and ask you to resolve these differences manually.
- **Resolving conflicts:** Open the affected files, look for conflict markers (`<<<<<<<`, `=======`, `>>>>>>>`), and edit the code to keep the desired changes. After resolving, stage and commit the file.

- **Merge strategies:**
  - _Fast-forward_: Moves the branch pointer forward when there are no divergent changes.
    - Performed automatically when you run `git merge <branch>` and the current branch has not diverged from the target branch.
  - _Three-way merge_: Combines changes from two branches and their common ancestor.
    - Occurs when branches have diverged. Run `git merge <branch>`, and Git will create a new merge commit.
  - _Squash merge_: Combines all changes from a branch into a single commit before merging. - Use `git merge --squash <branch>`, then `git commit` to create a single commit with all changes

Use `git status` to identify conflicts and `git log` to review merge history.

## Git CheatSheet

-[Git cheatsheet](https://education.github.com/git-cheat-sheet-education.pdf)
