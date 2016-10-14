# Git scenarios Solutions
##1. Hotfix
This exercise was hinting at stashing. But you could of course also commit your changes to your current branch. Check this slide http://slides.com/katjadurrani/deck-1#/24  <br />
So in our example, you are on branch *pub_kensington_arms* and make some changes that add or modify files, so you have a 'dirty' working directory. Then you can do:<br />
```git stash```<br />
to save your changes without having to commit them.<br />
<br />
Then:<br />
```git checkout development```<br />
make changes to styles.css<br />
```git add css/styles.css```<br />
```git commit -m"change heading colour"```<br />
<br />
```git checkout pub_kensington_arms```<br />
```git stash pop```


##2. I should have branched!
This is a situation where you could use the *reset* command. Create a new branch that you can then use to develop your new feature. Take the *development* branch back a few commits to a state before the start of the feature. <br />
```git branch feature```<br />
```git reset --hard HEAD~3```<br />
```git checkout feature```


##3. Merging
You are on the branch *pub_kensington_arms*. ```git merge development``` creates a conflict: <br />
<br />
```Auto-merging index.html```<br />
```CONFLICT (content): Merge conflict in index.html```<br />
```Auto-merging css/styles.css```<br />
```CONFLICT (content): Merge conflict in css/styles.css```<br />
```Automatic merge failed; fix conflicts and then commit the result.```<br />
Open a the files in a text editor, or a diff tool and fix the conflicts. Then add them to the staging area and commit them: <br />
```git add index.html css/styles.css```<br />
```git commit -m"resolve conflicts from merge"```

##4. Clear up that mess
Interactive rebasing! <br />
<br />
So here we want to tidy up the history a bit. You could do<br />
```git rebase -i 15e3d00```<br />
```git rebase -i HEAD~4```<br />
```git rebase -i origin/master```<br />
<br />
Then when your default editor opens, you can pick from various options for each commit, you replace the 'pick' in front of a commit by 'squash'(s), 'edit'(e) etc.<br />
<br />
David gave me the tip that it is a good idea to rebase onto origin/master as then you can be sure that you will not change a commit that you have pushed to remote. <br />
<br />
That is definitely good advice, I have just realised that I introduced some changes to master after branching off, so if you rebase onto master, you will get a conflict! That's actually good for practising but I did not recognise the error message "Could not apply .." as pointing to a conflict when I demonstrated the rebase. Also, Martin got the same error later and at that point I still didn't realise what it meant. See more on this below.<br />
<br />
What we could do in this case to avoid the conflict is rebase onto a commit that definitely is in the linear history of the *cafe_btp* branch, e.g. **15e3d00  add Boston Tea Party**<br />
<br />
Some rules for interactive rebasing:<br />
<br />
- You should always leave the oldest commit which is listed first. If you squash it, git complains about there being no previous commit! (The order of the commits is the reverse of *git log*, from oldest to latest) <br />
<br />
- When you get the error message "Could not apply < commit >" this simply means there is a conflict - you can do ```git status```, resolve the conflict in the files, then ```git add``` and ```git commit``` like you would normally do to resolve a conflict. After that you do ```git rebase --continue``` and then you will be taken further through the process of rebasing.<br />
<br />
- If you want to abort the rebase once the editor has already opened for you to squash, edit etc. the commits, you can just delete all the commits and save, then the rebase will abort. <br />
<br />
- Otherwise, just follow along with the process, when Git asks you, do ```rebase --continue```, the editor will open again etc. till at some point you will get the message "successfully rebased"


