
## 'Open Source'

- GitHub, forking, adding an upstream repo, pull requests
- Use commands like stash, cherry-pick, rebase

**Pubs and Cafes directory - New features**
Check out the branch *new-features*. Look at the history with `git log`.
There are commits for three new features in the branch: Menu, About page and Index. Choose a feature to work on. Create a new branch and try to get just the commits onto it that belong to your chosen feature. Work on the feature. When you are finished, merge the changes into *master*. 
(Try adding a pub or cafe to the directory inbetween. Stash what you are working on in the meantime.)

**Keep in sync with an upstream repo**
If you work with somebody else, designate one of the team's repo as the upstream repo and push to that. Keep your own repo updated with the upstream changes. When you pull, do a `pull --rebase`.

**Pubs and Cafes directory - Add a cafe or pub**
What is your favourite pub or cafe in Bristol? Add it to the root *index.html*, and create a `<cafe_or_pub>.html` file in the pubs or cafe folder. You can also add more than one, of course. Add and commit the files directly to the *master* branch. 

**Pull requests**
Create a pull request on the 'central' repo both for the feature and for the pub/cafe.
