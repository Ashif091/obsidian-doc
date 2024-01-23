The `git revert` command in Git is used to create a new commit that undoes the changes made in a previous commit. It is a safe way to reverse the effect of a commit without rewriting the commit history. Unlike `git reset`, which discards commits and can rewrite history, `git revert` generates new commits to reverse the changes.

Here's the basic syntax of the `git revert` command:

```bash
git revert <commit_hash>
```

- `<commit_hash>` is the hash of the commit you want to revert.

For example:

```bash
git revert abcdef123
```

This command creates a new commit that undoes the changes introduced by the commit with the hash `abcdef123`.

You can also specify a range of commits to revert:

```bash
git revert <start_commit>^..<end_commit>
```

This will revert all the commits in the range from `start_commit` to `end_commit`.

After running `git revert`, Git opens an editor for you to enter a commit message describing the revert. Once you save and close the editor, Git creates a new commit that effectively undoes the changes made in the specified commit(s).

Keep in mind that `git revert` doesn't remove the original commit; instead, it creates a new commit that negates the changes. This is useful in situations where you want to maintain a clear and linear history without rewriting it.