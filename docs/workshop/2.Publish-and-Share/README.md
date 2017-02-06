
## 'Publish and Share'

- Using git diff
- Three-Way Merge and possible conflict
- Rebasing
- Publishing

**Clone the repository and create a new branch**
If not done yet, fork the repository - https://github.com/CodeHubOrg/gitworkshop - to your own Github account. Look up the url for your fork, then run `git clone <url-repo>`. Inside the cloned project, create a branch *train-master* and merge the branch *train-development* into it. 

**Rebasing**       
- We want the *train-master* branch to include the latest changes from master, but keep a linear history. Rebase it onto master: `git rebase master`
Tip: Rebasing onto origin/master makes sure you are not overwriting history that has been published
- Check the differences between *train-master* and *master* using `git diff`.
- There should be a secret folder with and index.html file in it. Add a paragraph in the body of that file. Add and commit the changes to *train-master*.

**Another merge or rebase**       
We would like to get the changes from another branch into *train-master*. The branch is called *train-secret*. If you are still on *train-master*, you can just run `git merge train-secret`. Or you switch to *train-secret* and try to rebase it onto *train-master*, so you can after that switch back to *train-master* and do a fast-forward merge with `git merge train-secret`. (That's not confusing, is it?) Do you get a conflict? Try to resolve it. You can check how to do it on the [Commands page](Commands.md). Once you have done that, check the index file inside secret-folder in the browser.

**Time-travelling -- Reflog**         
If you have accidentally lost a commit or commits, use the Reflog. This is a list of all the commits you have made in the past 60 days. Check it out with `git reflog`! You can use `git show <commit>` to look what is inside a commit. Run `git reset HEAD@{index}` to take the project back to it. 










