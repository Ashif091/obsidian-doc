The `git commit` command is used to record changes to the repository. It captures a snapshot of the project's currently staged changes. This command creates a new commit object in the Git repository that contains a pointer to a tree object (which represents the root of the directory structure) and pointers to parent commits [1](https://git-scm.com/docs/git-commit).

Here are some common usages of `git commit`:

- `git commit`: This starts the commit process, and your default text editor will be opened for you to create the commit message.
- `git commit -m "commit message"`: This starts the commit process, and allows you to include the commit message at the same time.
- `git commit -am "commit message"`: In addition to including the commit message, this option allows you to skip the staging phase. The `-a` option will automatically stage any files that are already being tracked by Git.
- `git commit --amend`: This replaces the most recent commit with a new commit [3](https://github.com/git-guides/git-commit).

Remember, prior to executing `git commit`, the `git add` command is used to stage changes to the project that will be stored in a commit [2](https://www.atlassian.com/git/tutorials/saving-changes/git-commit).



![[Pasted image 20240123140955.png]]