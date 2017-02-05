
## 'Team of one'

- Clone a repository and check its history
- Simple workflow: Make changes to working directory, add, commit
- Lifecycle of a file: Untracked, Staged, Committed, Modified
- Undoing changes with reset
- Local branches

### Exercises

For the purpose of these exercises, we will be simulating a host repository and two downstream ones. It is probably best to put these in their own directory. 

1. Create the host repository with `git clone https://github.com/katjad/gitws17-exercises.git --bare origin.git`
2. Next, clone from this repo into a *myself* directory: `git clone origin.git myself`
3. Clone into a third directory called *co-worker* or a co-worker's name: `git clone origin.git mary` 

You should now have three repos in the directory, *myself*, *co-worker* and *origin.git*

**Adding and committing files**
- `Cd` into the *myself* directory. Type `ls` to check what files there are. Use `git log` to check the history.
- Start a server with `python -m SimpleHTTPServer`. You can see the site in the browser at localhost:8000.
- Add a new category directory (e.g. food) with an index.html file inside. 
- Now add the new files using `git add`
- Check that they were added to the staging area with `git status`
- Make sure food/index.html has the same html as, say, books.html. Change the title and h1 to 'Food'. 
- Do a `git status` again. The index file is listed twice. Why?
- Add the index file again and commit all the changes. 

**Undoing changes**
- We would like to have an about section on our site. Add a file `about.html` in the root. Change the *Books* link on the index page to *About* and link it to the file. You could also change the colour of the circle. 
- Do a `git status`. We will have an untracked and a modified file
- You suddenly think this wasn't a good idea at all. You have not committed anything yet, but want to get rid off all the changes. Use `git reset` to achieve this. (check `git help reset`)
- Tip: To get rid of untracked files use `git clean -f`

**Branching**
- Create a directory called news with an index.html file in it. Add anything you like to the index file.
- Add and commit your changes - you can use `git add -p` to go through each chunk one by one
- Now checkout the master branch and do `git merge news`
- Check the commit history with `git log`
