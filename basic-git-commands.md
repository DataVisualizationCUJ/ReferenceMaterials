# Basic actions in git

### Use these commands to create, update and modify files in git

### Commands
| What you want to do        | Command           
| ------------- |:-------------:
| Create a new repo in a folder    | `git init`
| Add a particular file to the repo      | `git add <filename>`
| Commit the file to the repo (so git will track it)    | `git commit -m "Commit message here." <filename>`
| Connect your local git repo to a GitHub repo     | `git remote add origin <linkToRepo>`
| Push local repo changes to GitHub    | `git push origin master`
| Download a copy of a repo stored on GitHub to a new computer   | `git clone <linkToRepo>`
| Download updates on GitHub into a repo you already have on your machine  | `git pull origin master`
| Resolving a merge conflict manually (after updating files)  | `git commit -i -m "Commit message here." <filename>`

### If you have an automatic merge and got automatically put into VIM...
- To rewrite the commit message, type `i` and then type. To save it and quit, click on `ESC`, `:x`.
- If you don't want to rewrite the commit message, just save and quit with `ESC` and `:x`.
