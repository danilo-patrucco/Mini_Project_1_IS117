# Mini_Project_1_IS117

<h3>How does the GitFlow works:</h3>

First of all, what is the Gitflow:

GitFlow is a branching model for Git, created by Vincent Driessen. It has attracted a lot of attention because it is very well suited to collaboration and scaling the development team.<br>

<h4>Gitflow visual representation:</h4>

![GitFlow Image](images/GitFlowHotfixBranch.png)

<h4>Link to a complete explanation of [ GitFlow!](http://google.com)</h4>

<h3>Definitions</h3>

Repository = A repository is a central file storage location. It is used by version control systems to store multiple versions of files.
<br>To create a Git repository users are required to follow these steps are :<br>
- Once git is installed go in the directory where the files that require version control are located.
- Type in the terminal "git init" to initialize the file that will contain the references of what need to be saved.
- To add all the files in the selected folder to the commit the user will have to type "git add .
- The last step to create a repository is to commit the changes (save all the changes made to the repository), to do that the user will have to type the following: git committ -m "your_commit_name"

Clone = git clone is a Git command line utility which is used to target an existing repository and create a clone, or copy of the target repository.

Fork = A fork is a copy of a repository. Forking a repository allows you to freely experiment with changes without affecting the original project.

Branch = A branch in Git is simply a lightweight movable pointer to one of these commits. The default branch name in Git is master.

Commit = The "commit" command is used to save your changes to the local repository.

Merge = Merging is Git's way of putting a forked history back together again.

Checkout = n Git terms, a "checkout" is the act of switching between different versions of a target entity. The git checkout command operates upon three distinct entities: files, commits, and branches.

Push = The git push command is used to upload local repository content to a remote repository. Pushing is how you transfer commits from your local repository to a remote repo.

Pull = git pull is a Git command used to update the local version of a repository from a remote.

Remote Add / Remove / Show = git-remote - Manage set of tracked repositories.
- Add : Adds a remote named `<name>` for the repository at `<url>`.
- Remove : Remove the remote named `<name>`.
- Show : Gives some information about the remote `<name>`.

Status = The git status command displays the state of the working directory and the staging area. It lets you see which changes have been staged, which haven't, and which files aren't being tracked by Git <br>

Master Branch = Is the main branch created in Git, it contains code that is available for deployment. The master branch should be updated only when sure that the software is working correctly and its free of critical bugs. <br>

<h3>Commands and examples</h3>

Command name | Command example | Result
------------ | ------------- | -------------
init | git init | the folder where the git init is executed will be added to a repository.
add . | git add . | will add all the files inside of a directory to the list of files that require version control
clone | git clone --reference_repository directory_name | will clone a reference directory into a new directory
fork | no command, it is clone on server side | fork the repo to allow multiple people to work on them. On GitHub the button fork can be used ---> <img src="https://upload.wikimedia.org/wikipedia/commons/3/38/GitHub_Fork_Button.png" width="100">
branch | git checkout -b branchname | create a new branch with name "branchame", if used with checkout will also move immediately on the branch
commit | git commit -m "your commit name" | commit the changes that were done on the current branch or master
merge | git merge branchname | will merge the branch "branchname" into the currently checked out branch 
checkout | git checkout branchname | will move the HEAD from one branch to the one defined in the checkout command
push | git push origin master | Use git push to push commits made on your local branch to a remote repository
pull | git pull origin master | fetches a copy of the master branch from the original repository, and merges it with the current branch you have checked out
status | git status | the status of the working working directory is displayed
remove | git rm filename | will remove the file or repo called "filename" from the commit list and the filesystem.
show | git show | one or more object will be displayed upon request 
