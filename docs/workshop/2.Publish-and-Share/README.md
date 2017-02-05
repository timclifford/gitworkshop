
## 'Publish and Share'

- Using git diff
[- Reset a branch to a few commits back
- Reflog
- Check single commits and cherry-pick  ]
- Three-Way Merge and possible conflict
- Rebasing
- Publishing

**Merging again**


**Adding a new feature from a branch - rebasing**
There is a branch called `blog` in the repo. Check it out. Also check the view in the browser. We are back to the old style but with one green blob, and the item names have moved around a bit. Switch to master again. We decide that we want all purple squares now with the exception of Blog in first position. Blog should be in a green circle. How best to achieve that? We would also like the changes from the blog branch to sit on top of the master branch. 


**Reflog**
If you have accidentally lost a commit or commits, use the Reflog. This is a list of all the commits you have made in the past 60 days. Check it out!
`git reflog` You can use `git show <commit>` to look what is inside a commit. And you can do `git reset <commit>` to go back to it. 

**Push to remote**
We would like to push our changes to the remote now. Use `git push origin <branchname>` for that or `git push --all`.




How to simulate host and two workers 






