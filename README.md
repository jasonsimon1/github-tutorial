# GitHub Tutorial

_by Jason Simon_

---
## Git vs. GitHub
Git does not require GitHub and takes "screeshots" of your work. It keeps track of your changes.   
GitHub is an online cloud that automatically saves your work. You can access it anywhere, on any computer. Think about any online [Google](https://www.google.com/) services. It does requires Git.



---
## Initial Setup
In order to get the boat moving, you're going to  need a [Github](https://github.com/) account. You only need to create **one** Github account.The setup process is similiar to that of any other (if you know how to make an Instagram account, this should be a piece of cake). In the case that you're using [c9.io](https://aws.amazon.com/cloud9/?origin=c9io), you will need to set up a bridge between both programs. You do this by getting the SSH key from **c9** (settings > SSH Keys > Second Box > Copy). Finally, go to **GitHub** (Settings > SSH KEYS AND GPG KEYS > New SSH Key > Paste). You've done it! You can now push/pull/fork or clone from Cloud9 to GitHub or Github to Cloud9.


---
## Repository Setup
`git init` initializes (starts) a new workspace. This command is to be used only once, at the start of your code. When you're ready to add and commit, you'd need to head on over to [Github](https://github.com/) and create a new repo. `git remote add origin URL` will set up a "bridge" between your local and remote repository.


---
## Workflow & Commands
* `git status` will become one of the most important parts of your code. It allows you to check for any errors you may encounter along the way and even tells you what commands you'd need to use in order to fix it. If your changes aren't staged for commit, you will see red. If they have been staged, you will see green.
* `git add .`will add the current directory you worked on to the staging area.  
* `git commit -m` will commit to the staging area. 
* `git push` will send your commits to [GitHub](https://github.com/). From there, you'll be able to see your changes.  

Heres an example:  
```
cd file_name
git add .  
git status  
On branch master  
Your branch is up-to-date with 'origin/master'.  

  
  Changes to be committed:  
    (use "git reset HEAD <file>..." to unstage)  
                modified:     README.md
git commit -m"change the text"  
[master 0089f4d] change the details  
1 file changed, 20 insertions(+), 10 deletions(-)
git push
```



---
## Rolling Back Changess
Assume you want to change the name of your Repo. You would need to **delete** your work from your local repository. This is the easiest way to renaming a project without having to use a billion confusing commands.  
`rm -rf file_name` will delete your project.  
Next, go to [GitHub](https://github.com/) and rename your repo.  
Clone the [Github](https://github.com/) repo to your local directory by clicking the green _clone or download_ option. Make sure its set on clone (with SSH) and copy it.  
Finally, go to your workspace by using the command `cd ../`   
`git clone git@github.com:yourusername/file-name.git` will bring back the repo to you Cloud9. **Make sure you CD into it everytime.** You can edit what you please and then add, commit, and push all over again.  



#### So you want to clone someone elses work?  
Go to the Github repo you wish to have and **fork** it. This will give you a copy of _their_ repo to _your_ Github account. It doesn't go straight to your local repository because when you go to push the changes you made, they won't show up at all. So, after you forked it (there is a button on the top right) clone that version down to your local repository.