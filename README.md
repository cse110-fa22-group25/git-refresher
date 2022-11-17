# git-refresher
## Basic command (you can also use vscode to do these)
- Clone the repo
    ```console
    > git clone https://github.com/cse110-fa22-group25/git-refresher.git
    ```
- Create a new branch
    ```console
    > git checkout -b <your branch name>
    ```
- Check what branch we have
    ```console
    > git branch
    ```
- Visit other branches
    ```console
    > git checkout <branch name>
    ```
- Push changes to remote (in your branch)
    ```console
    > git push
    ```
- Pull changes from remote (Do this every time before starting to work)
    ```console
    > git pull //git fetch + git merge
    ```
    or 
    ```console
    > git pull --rebase //another way to merge
    ```
- Merge two branches (usually need to resolve conflicts)
    ```console
    > git merge <other branch name>
    ```
## Possible Scenarios In Our Workflow
1. You create a branch from main and start working on some new features on that branch, while others are also creating some new branches from main and start working on other features.
   - Results: conflicts.
   - Solution: need to resolve those conflicts
     - Use VS Code


2. You pull your branch to the remote and Github action made some automatic chagnes to your branch. Then you did not notice that and continue to edit your local branch. After that, when you push those changes to the remote, it will fail because your local branch differs from the remote branch. 
   - Solution: 
        ```console
        > git pull --rebase
        ```