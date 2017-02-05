
## Commands used in 'Team of One'

**git clone**
git clone `[<dir>]`

**git log**
Try: 
git log --stat
git log --oneline
git log -n 4
git log --graph --all --oneline --decorate

**git add**
git add .
git add -A  (adds everything including deleted files)
git add -p  (option to approve each chunk individually)

**git commit**
git commit -m "message"
git commit -am "message" (adds and commits all modified files at the same time)
git commit --amend -m *or* commit --amend --no-edit (amend most recent commit)

**git status**

**git branch**
git branch `<branchname>`
git branch -d `<branchname>` (delete branch)
Also: git checkout -b (creates and checks out a branch at the same time)

**git reset**
git reset --hard HEAD  (reset everything to most recent commit)
git reset --soft HEAD^  (reset to parent while keeping the current files in working area)
Note:
- To move a file from *staged* to the working directory, use `git reset HEAD -- <filename>`
- To change a modified file back to the last commited version, use `git checkout <filename>`