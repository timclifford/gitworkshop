
## 'Team of one'

- Clone a repository and check its history
- Simple workflow: Make changes to working directory, add, commit
- Lifecycle of a file: Untracked, Staged, Committed, Modified
- Undoing changes with reset
- Local branches

### Configuration 

Is there anything you would like to change in your configuration? If you have not done so yet, you could add an SSH key to your Github account. 

### Exercises

Remember, the documentation at `git help <command>` is pretty good!

**Clone the Git workshop respository**    
Fork the repository - https://github.com/CodeHubOrg/gitworkshop - to your own Github account. Look up the url for your copy, then run `git clone <url-repo>`.

**Adding and committing files**
- Create a random new file and add some text to it.
- Now add it using `git add`
- Check that it was added to the staging area with `git status`
- Now write some more text and run `git status` again. The file is listed twice. Why?
- Add the index file again and commit all the changes. 

**Undoing changes**
- You do not really want to keep the file you just commited. How can you restore things to the last commit before yours? (use `git reset`)
- Now, add a paragraph to the index.html page in the root of the project. Then add a random file.
- Run `git status`. We will have an untracked and a modified file
- You suddenly think this wasn't a good idea at all. You have not committed anything yet, but want to get rid off all the changes. Use abother `git reset` to achieve this. 
- Tip: To get rid of untracked files use `git clean -f`, if you want to include untracked directories `git clean -df`

**Branching and merging**
- Check you are on the master branch and your working directory is clean with `git status`.
- Create a branch *train-master*. Then check out *train-development*. Merge *train-development* into *train-master*: `git merge train-development`

More exercises at [2. README](../2.Publish-and-Share/README.md)
