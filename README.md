# Mini_Project_1_IS117
<h3>How the usage of Git, Docker, automated testing, and continuous integration can improve the productivity and competitiveness of a company: </h3>

- Git is a software that allows to handle version control, a way for developer to constantly monitor the deployment and updating of software.
- Docker is  a container engine which uses the Linux Kernel features like namespaces and control groups to create containers on top of an operating system and automates application deployment on the container.
- Automated testing is a process that validates if software is functioning appropriately and meeting requirements before it is released into production. This software testing method uses scripted sequences that are executed by testing tools. Automated testing tools execute examinations of the software, report outcomes and compare results with earlier test runs.
- Continuous Integration (CI) is a development practice where developers integrate code into a shared repository frequently, preferably several times a day. Each integration can then be verified by an automated build and automated tests

All together these software / practices allow a company to constantly monitor and optimize deployment and upgrading of software, reducing the amount of people and time needed to perform tasks.
<br>The final goal is a complete process atomization and reaching a state of instant development and deployment control.

<h3>How does GitFlow works:</h3>

First of all, what is the Gitflow:

GitFlow is a branching model for Git, created by Vincent Driessen. It has attracted a lot of attention because it is very well suited to collaboration and scaling the development team.<br>

There are few benefits in the Gitflow, the most important is parallel development.
Parallel development means that multiple people can all work on the same project without having to worry of what the other developers are doing, mostly thanks to the branching.

<h5>Complete GitFlow process</h5>
New development (new features, non-emergency bug fixes) are built in feature branches<br><br>
![GitFlow Image](images/feature branch 1.png) <br><br>

Feature branches are branched off of the develop branch, and finished features and fixes are merged back into the develop branch when they’re ready for release:<br><br>
![GitFlow Image](images/develop branch 2.png) <br><br>

When it is time to make a release, a release branch is created off of develop:<br><br>
![GitFlow Image](images/release branch 3.png) <br><br>

The code in the release branch is deployed onto a suitable test environment, tested, and any problems are fixed directly in the release branch. This deploy -> test -> fix -> redeploy -> retest cycle continues until you’re happy that the release is good enough to release to customers.
<br>
<br>
When the release is finished, the release branch is merged into master and into develop too, to make sure that any changes made in the release branch aren’t accidentally lost by new development.<br><br>

![GitFlow Image](images/release branch merge 4.png) <br>

The master branch tracks released code only. The only commits to master are merges from release branches and hotfix branches.
<br>Hotfix branches are used to create emergency fixes:

![GitFlow Image](images/GitFlowHotfixBranch.png)

They are branched directly from a tagged release in the master branch, and when finished are merged back into both master and develop to make sure that the hotfix isn’t accidentally lost when the next regular release occurs.

<h4>Link to a complete explanation of [ GitFlow!](http://google.com)</h4>



<h3>Definitions</h3>

<h5>Repository</h5>A repository is a central file storage location. It is used by version control systems to store multiple versions of files.
<br>To create a Git repository users are required to follow these steps are :<br>
- Once git is installed go in the directory where the files that require version control are located.
- Type in the terminal "git init" to initialize the file that will contain the references of what need to be saved.
- To add all the files in the selected folder to the commit the user will have to type "git add .
- The last step to create a repository is to commit the changes (save all the changes made to the repository), to do that the user will have to type the following: git committ -m "your_commit_name"

<h5>Clone</h5> git clone is a Git command line utility which is used to target an existing repository and create a clone, or copy of the target repository.

<h5>Fork</h5>A fork is a copy of a repository. Forking a repository allows you to freely experiment with changes without affecting the original project.

<h5>Branch</h5>A branch in Git is simply a lightweight movable pointer to one of these commits. The default branch name in Git is master.

<h5>Commit</h5>The "commit" command is used to save your changes to the local repository.

<h5>Merge</h5>Merging is Git's way of putting a forked history back together again.

<h5>Checkout</h5>n Git terms, a "checkout" is the act of switching between different versions of a target entity. The git checkout command operates upon three distinct entities: files, commits, and branches.

<h5>Push</h5>The git push command is used to upload local repository content to a remote repository. Pushing is how you transfer commits from your local repository to a remote repo.

<h5>Pull</h5>git pull is a Git command used to update the local version of a repository from a remote.

<h5>Remote Add / Remove / Show</h5> git-remote - Manage set of tracked repositories.
- Add : Adds a remote named `<name>` for the repository at `<url>`.
- Remove : Remove the remote named `<name>`.
- Show : Gives some information about the remote `<name>`.

<h5>Status</h5>The git status command displays the state of the working directory and the staging area. It lets you see which changes have been staged, which haven't, and which files aren't being tracked by Git <br>

<h5>Master Branch</h5>Is the main branch created in Git, it contains code that is available for deployment. The master branch should be updated only when sure that the software is working correctly and its free of critical bugs. <br>

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
