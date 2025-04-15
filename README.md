# QA Bootcamp Git Exercises

This repository contains exercises for learning Git fundamentals as part of the QA Bootcamp program.

## Exercise Instructions for Students

These instructions are specifically designed for Windows Command Prompt users. Follow each step carefully to complete the exercise.

### Prerequisites

- Git installed on your Windows machine
- GitHub account
- Basic familiarity with Command Prompt

### Exercise Steps

#### Initial Setup

1. Open Command Prompt:
   - Press `Win + R`
   - Type `cmd` and press Enter

2. Clone the repository:
   ```
   git clone https://github.com/azka-art/qa-bootcamp-git-exercises.git
   ```

3. Navigate to the cloned repository:
   ```
   cd qa-bootcamp-git-exercises
   ```

4. Create the `learn_git_again` folder:
   ```
   mkdir learn_git_again
   ```

5. Navigate into the new folder:
   ```
   cd learn_git_again
   ```

#### Git Repository Setup

6. Initialize a new git repository:
   ```
   git init
   ```

7. Create the first file:
   ```
   echo. > third.txt
   ```

8. Add the file to staging:
   ```
   git add third.txt
   ```

9. Make your first commit:
   ```
   git commit -m "adding third.txt"
   ```

10. View your commit history:
    ```
    git log
    ```

#### Additional File Operations

11. Create another file:
    ```
    echo. > fourth.txt
    ```

12. Add it to staging:
    ```
    git add fourth.txt
    ```

13. Make your second commit:
    ```
    git commit -m "adding fourth.txt"
    ```

14. Remove the first file:
    ```
    del third.txt
    ```

15. Stage the removal:
    ```
    git add --all
    ```
    (Or specifically: `git rm third.txt`)

16. Commit the removal:
    ```
    git commit -m "removing third.txt"
    ```

17. Check your commit history again:
    ```
    git log
    ```

#### Branch Creation & Management

18. Create a feature branch with your name:
    ```
    git checkout -b feature/your-name
    ```

19. Create a new file in your branch:
    ```
    echo This is my student work > student-work.txt
    ```

20. Add the new file to staging:
    ```
    git add student-work.txt
    ```

21. Commit the new file:
    ```
    git commit -m "adding student work in feature branch"
    ```

#### Git Configuration

22. Set the global pager configuration:
    ```
    git config --global core.pager cat
    ```

23. List all global git configurations:
    ```
    git config --global --list
    ```

#### Pushing Your Work

24. Push your branch work:
    ```
    git checkout master
    ```
    (Note: This repository has both `main` and `master` branches. If you initialized with `git init`, you'll likely be on `master`)

25. Push to the remote repository:
    ```
    git push -u origin master
    ```
    (This will push your master branch. The repository also has a main branch by default on GitHub)

26. Push your feature branch:
    ```
    git checkout feature/your-name
    git push -u origin feature/your-name
    ```

### Verification Steps

27. Verify your commits match requirements:
    ```
    git log --oneline
    ```
    You should see exactly 3 commits with the exact messages in your master branch:
    - "removing third.txt"
    - "adding fourth.txt"
    - "adding third.txt"
    
    And in your feature branch, you should also see the commit:
    - "adding student work in feature branch"

28. Verify your branches:
    ```
    git branch -a
    ```
    You should see three branches:
    - `master` (your working branch from git init)
    - `main` (default branch on GitHub)
    - `feature/your-name` (your feature branch)

29. Optional: Create a Pull Request
    - If you want to complete the full Git workflow, you can create a pull request by clicking the "Compare & pull request" button on GitHub
    - This step is not required for the exercise but provides good practice with GitHub's collaboration features

### Troubleshooting Common Windows Issues

- If you encounter permission issues:
  ```
  git config --global --add safe.directory "*"
  ```

- If you have line ending issues (common on Windows):
  ```
  git config --global core.autocrlf true
  ```

- If Command Prompt doesn't show UTF-8 characters correctly:
  ```
  chcp 65001
  ```

- If you need to provide credentials:
  ```
  git config --global credential.helper wincred
  ```

- If you're trying to set a remote and getting "remote already exists" error:
  ```
  git remote remove origin
  git remote add origin https://github.com/azka-art/qa-bootcamp-git-exercises.git
  ```

## Exercise Criteria

For successful completion, ensure your work meets these criteria:

- [ ] Successfully cloned the repository
- [ ] Made exactly the commits specified in the instructions (3 commits on master branch)
- [ ] Created feature branch with your name (e.g., feature/Azka)
- [ ] Added and committed student work to your feature branch
- [ ] Successfully pushed all changes to the remote repository (both master and feature branches)
- [ ] Configured Git global settings as specified

## Additional Resources

- [Git Documentation](https://git-scm.com/doc)
- [GitHub Guides](https://guides.github.com/)
- [Git Cheat Sheet](https://education.github.com/git-cheat-sheet-education.pdf)
- [Rithm School Git Basics Exercises](https://www.rithmschool.com/courses/git/lessons/git-github-git-basics-exercises/)
