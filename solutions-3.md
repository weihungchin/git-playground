## To squash (combine) multiple commits into a single commit, we can:

1. on feature branch, `git rebase -i HEAD~n`, n can be any number > 1. It means how many commits we want to squash into 1. Lets say we want to squash 3 commits, we will run `git rebase -i HEAD~3`.
2. after step 1, you will see the scary VIM editor, press `i`, leave the first line unchanged, change the 'pick' into 'squash' for second and thrid line.
3. press 'Esc' key, and enter `:wq`.
4. this will enter another vim editor to edit the commit messge, simply press `i` then `Esc`, and enter `:q`.
5. this shld now squash all the commits 