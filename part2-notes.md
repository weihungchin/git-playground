## Revert
To undo a specific commit, `git revert shaOfCommit`, eg: `git revert 543ebe80`

## Undo changes
Undoing changes in own (feature branch), commits that are not yet merged to shared branch (typically master/main/develop).

## Git Reset
To go back in time to a specific commit,

### With hard reset
1. `git reset --hard HEAD~` to go back 1 commit in time.
2. This will remove the last commit (together with all the changes). 
3. This command is destructive (all uncommitted local changes is gone).
4. To go back 2 commits in time (i.e remove the latest 2 commits), use `git reset --soft HEAD~2`, and so on.

### With soft reset
1. `git reset --soft HEAD~` to go back 1 commit in ime.
2. This will remove the latest commit in this history, but the changes are still in the staging area. This means you still have the changes, but those changes are not committed yet (not git commit yet)
3. To go back 2 commits in time (i.e remove the latest 2 commits), use `git reset --soft HEAD~2`, and so on.

### When to use git revert, git reset or drop commit ?
1. Is the changes you want to undo in a shared/published branch ? (eg. a commit in master branch). If yes, `git revert`.

2. Do you want to remove a specific commit (a commit that only exists in feature branch) ?  Use `drop` in `git rebase -i HEAD~` and choose the commit to drop.


3. Do you want to go back in time in feature branch (only on those commits that are not in master branch) ?  use git reset
