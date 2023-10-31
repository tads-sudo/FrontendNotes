# What is Git?

Git is a widely used version control system that allows multiple people to collaborate on software development projects. It keeps track of changes in a project's source code and helps manage different versions of the codebase.

Here are some key concepts and commands related to Git:

1.  **Repository(Repo)**: A repository is a directory or storage space where your project is stored, including all of its files, revisions, and other data

2.  **Clone**: This command is used to create a local copy if a remote repository. For example, if you want to work on a project hosted in GitHub, you would first clone it to your local machine.

    ```
    git clone <repository_url>
    ```

3.  **Commit**: A commit is a checkpoint in the project's history. It records changes to the repository. You need to provide a commit message describing the changes you made.

    ```
    git commit -m "Your commit message"
    ```

4.  **Push**: Pushing means sending your committed changes to a remote repository. This is typically done after you've made a series of local commits and want to share your work.

    ```
    git push
    ```

5.  **Pull**: Pulling means fetching and merging any changes from the remote repository to your local working directory.

    ```
    git pull
    ```

6.  **Branch**: A branch is a separate line of development. You can work on different features or fixes in separate branches without affecting the main codebase.

    ```
    git branch
    ```

7.  **Checkout**: This command is used to switch between different branches or restore files in the working directory to an earlier state.

    ```
    git checkout <branch_name>
    ```

8.  **Merge**: Merging combines changes from different branches into the current branch.

    ```
    git merge <branch_name>
    ```

9.  **Pull Request (PR)**: On platforms like GitHub, a pull request is a way to propose changes to a project's repository. It's a discussion and review mechanism for code changes before they are merged into the main branch.

10. **Remote**: This refers to the version of the repository that is hosted on a server (like GitHub, GitLab, Bitbucket, etc.).
