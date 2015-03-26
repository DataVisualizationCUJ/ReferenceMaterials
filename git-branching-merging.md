# Branching and merging with Git

### When should I branch?
You should branch when you want to create new features or experiment with something new. 

### The 5-step process of branching and merging
1. Switch to a new branch, make & commit changes
2. Switch back to master & pull from GitHub to make sure it's all up-to-date
3. Switch to branch and merge master into branch
4. Test to make sure everything still works!!!
5. Switch back to master, merge the branch back into master, and then push back up to GitHub

### Commands
| What you want to do        | Command           
| ------------- |:-------------:
| List branches    | `git branch`
| Create a new branch (this creates a new branch and switches you into it)      | `git checkout -b <branchName>`
| To switch branches    | `git checkout <branchName>`
| To merge branches     | Switch into the branch you want to merge stuff into. Then `git merge <branchToMerge>`
| To push branches to Github    | `git push origin <branchName>`
| To pull branches from Github  | git fetch
| To delete local branches  | Switch to a branch you don’t want to delete. Then `git branch -D <branchToDelete>`
| To delete branches on Github  | `git push origin :<branchToDelete>`