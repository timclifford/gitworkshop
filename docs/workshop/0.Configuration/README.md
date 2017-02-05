
## Configuration

### Identify yourself

`git config --global user.name "<name>"`      
`git config --global user.email "<email>"` 

Check that these have been added to your settings:       
`git config --list`

### Editor 
`git config --global core.editor nano` (easier to handle than vim!)

### Aliases

For example:      
`git config --global alias.co checkout`      
`git config --global alias.unstage "reset HEAD --"`         
`git config --global alias.lg "log --graph --all --oneline --decorate"`   

You can also add an alias directly in your .gitconfig file (this one is similar to the lg alias above, but adds time and author):      
[alias]     
lg = log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit --date=relative


### SSH Keys

Using ssh keys, you can write to a repo without having to enter username and password:              
https://help.github.com/articles/connecting-to-github-with-ssh/


