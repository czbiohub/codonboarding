# Github Repository

## Create A New Repository:
In your github account online select the + icon in the top right of the screen and select "New Repository"

#### Specifications for your repository
1) **Select "initialize with a README"**

2) **Select Git ignore parameters**-this tells git to ignore certain files that are generated in the process of some of the code you may run. Ex. you may want to select Python in order to ignore small extra files that are generated in the process of running your code. 

3) **Select license type**-You need a license otherwise all code you write is considered copy written and cannot be used by others. We ususally select MIT License.

	a) Simple and permissive (ex MIT License). This makes you not liable for any ways your code is used. 
	b) Patents-usually does not apply to our use cases.
	c) Copy left-anyone who uses your code must make it available under the same conditions that you did. 
	
## Access And Make Changes To An Existing Repository:

### Make a copy of the chosen respository from github

This downloads the respoitory you want in its current state as well as the history of that entire respoitory (all the changes that have been made, when and by whom). 

1) On your terminal navigate to the directory that you want to download the repository into.

2) On the github page for the chosen repository select "clone or download"- this will give you the link you will need to provide in the command line to clone this repository to your local computer. 

3) In the terminal type `git clone <copied link from github page>` 

ex. `git clone https://github.com/czbiohub/codonboarding.git`

4) In terminal navigate to this folder. In this folder you will be on the master branch of the repository folder that we made on our local computer for the repository we cloned. 

### Make changes to the respository 

1) **Make a new branch**-Use `git checkout -b branchname` to make a branch off of the master in the repository you downloaded. This makes an exact copy of the entire master that you will make changes to. You use the -b because you want to go to a branch that you are also creating. You can also use just `git checkout <branchname> in order to move to a branch that already exists if you want to move between branches once they have been created.  

2) **Look at what is in your branch**-Use `git status`-This will show you what files are in the branch you are on and if they are being tracked or not by github. It will tell you the difference between what you have changed on your local branch and the last commits that were made and tracked by Github. If you have made a change to the repostory on your local computer that you have yet to commit the result is:

On branch <branch name>

Untracked files:

(use "git add <file name>" to include in what will be committed)


<untracked file or change>

nothing added to commit but untracked files present (use "git add" to track).

3) **Track changes made on your branch**-Use  `git add <file>`  

to have your changes be tracked by github. This adds the changes you made on your branch on your local computer in order to have github track these changes. 

4) **Commit the changes from your branch to github**-Use `git commit -m"messagetoyourselfaboutchange" ` 

This is how you ask to commit a change you have made to the branch you are in. Adding a message will be important so you can remember the purpose of each change. It will output what you have added to the branch. If you say `git status` it will show you that you have made all the commits available to be made. These are the commits that git stores and uses to remember what has been changed, when and by whom. You can also use:

 `git commit -a`
 to make a batch of commits at once. 

5) **Add these changes (push them) back to github** Use `git push origin <Branch Name>` 

This is where we ask to push our changes up to github.Once this has happened we need to go onto github to actual merge this "pull request". If you have two additions that that are in conflict you have to resolve them by hand as is prompted on the website. 

6) **Return from your branch to the master** Use `git checkout master`. 

You will want to return to master so that once you have merged your changes in github you can update your local version of the repository from your local master branch. Once the pull request has been merged you can update these changes without re cloning the repository by running 

`git pull` from the master branch. 

7) **Merge your commits to github (pull request)** Return to Github website and refresh your repository. You will see an option to select "compare and merge request". When you select this option in takes you to a new screen that allows you to write a small description of your change. Here you select the next option to continue your pull request. Once you have successfull merged your request with the master you will have the option to delete the merged branch.

8) **Update your cloned repository** In your master branch on the terminal use `git pull` to upload the newest version of the repository to your local computer. 




