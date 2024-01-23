In Git, `git stash` is a command used to temporarily save changes that you have in your working directory but do not want to commit at the moment. It's a way to "stash away" your changes, allowing you to switch to a different branch or perform other tasks without committing your current changes.

Here are the basic operations you can perform with `git stash`:

1. **Stash Changes:**
   ```bash
   git stash
   ```
   This command stashes your changes, saving them in a new stash entry. Your working directory is then reverted to the state of the last commit.

2. **List Stashes:**
   ```bash
   git stash list
   ```
   This command shows a list of all stashes you have created.

3. **Apply the Latest Stash:**
   ```bash
   git stash apply
   ```
   This command applies the changes from the latest stash to your working directory. The stash entry remains in the stash list.

4. **Apply a Specific Stash:**
   ```bash
   git stash apply stash@{n}
   ```
   Replace `n` with the index of the stash you want to apply. The index is obtained from the `git stash list` command.

5. **Pop the Latest Stash:**
   ```bash
   git stash pop
   ```
   This command applies the changes from the latest stash and removes the stash entry from the stash list.

6. **Pop a Specific Stash:**
   ```bash
   git stash pop stash@{n}
   ```
   Applies the changes from a specific stash and removes that stash entry.

7. **Clear Stashes:**
   ```bash
   git stash clear
   ```
   This command removes all stashes. Be careful as this action is irreversible.

The `git stash` command is particularly useful when you're in the middle of working on something, but need to switch to another branch or perform some other task. It helps you save your changes temporarily and bring them back later without committing them.