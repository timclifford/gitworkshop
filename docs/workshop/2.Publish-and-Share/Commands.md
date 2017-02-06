

## Commands used in 'Publish and share'

**git fetch**    
git fetch origin branch     
git fetch --all (this does *not* mean fetch all branches, but fetch one branch  from all remotes!)      
git fetch --tags     

**git pull**     
git pull     
git pull --rebase      

**git push**      
git push origin branch     
git push origin --delete branch      

**git diff**     

**git merge**     
git merge --abort (there's always a way out if things go wrong!)    
git merge --no-ff     
git merge -X ours       

**git reflog** (search for lost commits!)     
Opens a history of each commit you made in the last 60 days    
Use git show `<commit>` to check what's inside a commit      
and `git reset HEAD@{index}` to go back to it     

***Process of dealing with a conflict:***                
`git status` - tells you what files are affected        
Open those files and choose the chunks that you want to be included. Get rid of the markers (<<<<<<, >>>>>, HEAD and so on). Save the file(s).      
Next, `git add` the file(s)           
Then, type `git commit` - your editor will open with a default commit message. Save. That's it.          





