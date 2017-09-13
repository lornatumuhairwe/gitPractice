# My Git Commands

I have used git for a while now, but when I began collaborating with people seriously, I now realize I have been underutilzing it. 
In this repo, I'll be trying out different git commands without fear of losing my work and I'll document accordingly. 

### Commands 
#### Undoing commits
1. `git log` is used to view the history of commits in that branch
2. `git reset --hard HEAD <COMMIT-ID>` is ued to reset local changes to last commit with `COMMIT-ID`. `git reset --hard HEAD` deletes all uncommitted changes in the current branch and 
is therefore considered dangerous. To use it, make sure the current branch doesn't contain any changes that are still needed. You can use It when you make changes to a branch 
after a commit but you don't need those changes anymore.
3. The previous commit rewrites the history of the branch. That's why `git revert` is preferred. Refer to [this](https://www.git-tower.com/learn/git/ebook/en/command-line/advanced-topics/undoing-things) and [this](https://sethrobertson.github.io/GitFixUm/fixup.html#pushed).
4. If the changes have been published already, you can push the branch with the changed history by using `git push -f`. 
If it fails, use `git config receive.denyNonFastForwards` to enable it receive fast forwards temporarily. 
#### Squashing commits
Checkout this [link](http://gitready.com/advanced/2009/02/10/squashing-commits-with-rebase.html)
`git push -f` if the code was aleady upstream.