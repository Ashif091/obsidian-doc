The `git cherry` command is used to find commits in one branch that have not been applied to another branch. It is particularly useful when you want to identify changes made in one branch that have not yet been merged or applied to another branch.

The basic syntax for `git cherry` is as follows:

```bash
git cherry [-v] <upstream> [<head> [<limit>]]
```

- `<upstream>` is the branch you want to compare against.
- `<head>` is the branch containing commits you want to check.
- `<limit>` is an optional parameter specifying the number of commits to display.

Here's a brief explanation of the options:

- `-v`: Show the commit messages in addition to commit hashes.

Here's an example of how you might use `git cherry`:

```bash
git cherry -v main my_feature_branch
```

This command will show a list of commits in `my_feature_branch` that haven't been applied to `main`. The `-v` option will display the commit messages as well.

The output will typically show lines with a prefix like `+` or `-` to indicate whether a commit has or has not been applied, along with the commit hash and message.

Keep in mind that `git cherry` only looks at the commit hashes and messages to identify changes, so if the commit messages or hashes have changed due to rebasing or amending, it may not provide accurate results.