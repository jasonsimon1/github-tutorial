# GitHub Tutorial

_by Jason Simon_

---
## Git vs. GitHub
Git does not require GitHub and takes "screeshots" of your work.  
GitHub is an online cloud that automatically saves your work. You can access it anywhere, on any computer. Think about any online [Google](https://www.google.com/) services. It requires Git.



---
## Initial Setup
In order to get the boat moving, you'd need a [Github](https://github.com/) account. You would only need to create **one** Github account. In the case that you're using [c9.io](https://aws.amazon.com/cloud9/?origin=c9io), you're going to need to set up a bridge between both programs. You do this by getting the SSH key from **c9** (settings > SSH Keys > Second Box). Finally, go to **GitHub** (Settings > SSH KEYS AND GPG KEYS > New SSH Key)


---
## Repository Setup
`git init` initializes (starts) a new workspace. This command is to be used only once, at the start of your code. When you're ready to add and commit, you'd need to head on over to _Github_ and create a new repo. `git remote add origin URL` will set up a "bridge" between your local and remote repository.


---
## Workflow & Commands
* `git status` will become one of the most important parts of your code. It allows you to check for any errors you may encounter along the way and even tells you what commands you'd need to use in order to fix it.  
* `git add .`will add the current directory you worked on to the staging area.  
* `git commit -m` will commit to the staging area. 
* `git push` will send your commits to GitHub. From there, you'll be able to see your changes.


---
## Rolling Back Changess
Assume you want to change the name of your Repo. You would need to delete your work from your local repository. `rm -rf file_name` will delete your project.  
Next, go to **GitHub** and rename your repo.  
Clone the Github repo to your local directory by clicking the green _clone or download_ option. Make sure its set on clone with SSH and copy it.  
Finally, go to your workspace by using the command `cd ../`   
`git clone git@github.com:yourusername/file-name.git` will bring back the repo to you Cloud9. **Make sure you CD into it everytime.** You can edit what you please and then add, commit, and push 