## To do a rebase onto the latest main, you can:

1. Checkout the main branch, ie. `git checkout main`
2. Make sure main branch is updated by pulling latest from remote, ie. `git pull`
3. Checkout the feature branch, ie. `git checkout topic-1`
4. Make sure everything is commited, when run `git status`, it should say `nothing to commit`
5. Rebase onto latest main, ie. `git rebase main`

OR you could do everything from 1-5 in 1 command:
1. Make sure you are on feature branch (i.e on topic-1 branch), and run `git pull -r origin main`