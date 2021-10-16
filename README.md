# COMPLETE GIT HANDBOOK 📚

<br>

## Git

Git is free  **open source software**  (the  [source code is public](https://github.com/git/git)) written by Linus Torvalds who also wrote the Linux operating system's kernel.

Git is a program for keeping track of changes over time, known in programming as  **version control**. If you've used a track changes feature in a text editing software then you're already familiar with the concept!

<br>

## Install Git

We recommend installing Git on your computer by installing the  [latest version](https://git-scm.com/downloads)  from the Git website.

-   **Windows**: Use the  **Git Shell**  for your terminal.
-   **Mac**: You can use the  **terminal**  app as your terminal.

Already have Git or not sure? Type  `git --version`  in your terminal and if it returns a version number higher than  `1.7.10`, you're set! For more information, visit the  [Git website](http://git-scm.com).

<br>

### Configure Git

Once Git is installed, open your  **terminal**. You can verify that Git is really there by typing:

`git --version`

This will return the version of Git on your computer and look something like this:

`git version 1.9.1`

Next, configure Git so it knows to associate your work to you:

Set your name:

`git config --global user.name "Your Name"`

Now set your email:

`git config --global user.email "youremail@example.com"`

You're done with your first challenge! Click the 'Verify' button to check the challenge.

<br>

### Configure Git

Once Git is installed, open your  **terminal**. You can verify that Git is really there by typing:

`git --version`

This will return the version of Git on your computer and look something like this:

`git version 1.9.1`

Next, configure Git so it knows to associate your work to you:

Set your name:

`git config --global user.name "Your Name"`

Now set your email:

`git config --global user.email "youremail@example.com"`

You're done with your first challenge! Click the 'Verify' button to check the challenge.

<br>

> # REPOSITORY

<br>

## **Goal**
Install Git on your computer and configure your name and email.

<br>

## Repositories

A  **repository**  is a collection of related items. In our case, when writing software, it is a collection of files related to a software project. You can imagine it as a project folder with all the relevant files inside of it. In fact, that's what it will look like on your computer anyways. Sometimes they're called 'repos' for short

![git_repository_image](https://github.com/ad1tya-v3rma/hackober-repo--1/blob/main/images/repo.PNG)

*Repositories just look like normal folders on your computer. However there is an important difference: Their content is beeing tracked by Git.*

You tell Git what your project is and Git will start tracking all of the changes to that folder. This makes it a Git repository: a folder of items being tracked by Git. Git tracks when files are added, subtracted or even a single letter in a single file is changed. All of this plus who did it and when is tracked by Git. In software, tracking changes like this is called version control.

<br>

## Using Terminal

**Terminal**  (or Bash) is a way to instruct your computer to do things by typing commands rather than clicking applications with your mouse. You can rename files, open files, create new folders, move between directories (folders) and more all by running typed commands. You can even use a text editor for code (like  [Vim](http://en.wikipedia.org/wiki/Vim_(text_editor))) in your terminal an never have to leave!

Besides navigating your computer, you can also use programs in Terminal that have a  **command-line interface (CLI)**, meaning they can be run with commands in terminal. Git is one of these. The first part of the command lets your computer know you're talking to Git. The parts following that are the commands and the different options you want Git to act on.

In Git-it you'll learn a few basic command-line actions (in addition to Git commands) for navigating your computer. They're described within the steps.

<br>

### Create a Repository

You're going to create a new project folder and then initialize it as a Git repository. We'll name the folder 'hello-world' in this challenge, but you can choose a different name if you already have a folder named this (it's a common first project name).

Time to open your terminal!

In your terminal window, type these commands, one at a time, pressing enter/return after each.

First, make a new folder:  
Tip: mkdir stands for  _make directory_

`mkdir hello-world`

Then go into that folder:  
Tip: cd stands for  _change directory_

`cd hello-world`

Finally, tell Git to initialize (start tracking) the folder you are now in:

`git init`

The last command should return something starting with 'Initialized empty Git repository'. The others commands do not return anything.

You did it! If you want to be double-sure that it's a Git repository, type  `git status`  and if it doesn't return 'fatal: Not a git repository...', you're golden!


<br>

> # COMMIT TO IT

<br>

## Commits

Commits are core to using Git. They are the moments in which you save and describe the work you've done. They are the ticks in the timeline of your project's history.

### Create a New File

Now that you've got a repository started let's add a file to it.

Open your text editor and create a new empty file. Now write a little bit of text, perhaps type "Hello!", and save the file as 'readme.txt' in the 'hello-world' folder you created in the last challenge.


### Check Status + Add and Commit Changes

Next check the  **status**  of your repository to find out if there have been changes. You know you have changed something, but does Git?

Make sure you're still within your 'hello-world' directory when you're running these commands. Use Git to see what changed in your repository:

First, check the status:

`git status`

Git should tell you that a file has been added.

Then  **add**  the file you just created so that it becomes a part of the changes you will  **commit**  (aka save) with Git:

`git add readme.txt`

Finally,  **commit**  those changes to the repository's history with a short (m) message describing the updates.

`git commit -m "Created readme"`

<br>


### Step: Make More Changes

Now add another line to 'readme.txt' and save the file again.

In terminal, you can view the  **diff**erence between the file now and how it was at your last commit.

Tell Git to show you the  **diff**:

`git diff`

Now with what you just learned above, commit this latest change.


<br>

> # CONNECTING GITHUB

<br>


## Working Better, Together

The repository you've created so far is just on your computer, which is handy, but makes it pretty hard to share and work on with others. No worries, that's what GitHub is for!

GitHub is a website that allows people everywhere to upload what they're working on with Git so that everyone can easily work together on the same project. GitHub which acts as the central repository for you and everyone else to share. You push your changes to it and pull down changes from others.

<br>

### Create a GitHub Account

Visit  [github.com](https://github.com)  and sign up for a free account.  **High five, welcome!**

<br>

### Add GitHub username to Git

Add your GitHub username to your Git configuration. We'll do this just for the sake of Git-it; it makes it easier to verify the upcoming challenges. Save it exactly as you created it on GitHub and  **capitalize where capitalized**. Note, you don't need to enter the "<" and ">".

Add your GitHub username to your Git configuration:

`git config --global user.username <UserName>`

You can double check what you have set in your Git config by typing:

`git config --global user.username`


<br>

> # REMOTE CONTROL

<br>

## Remotes

When you put something on GitHub that copy lives on one of GitHub's servers. This makes it a  **remote**  repository because it is not on your computer, but on a server, "remote" and somewhere else. By  **pushing**  your  **local**  (on your computer) changes to it, you keep it up to date.

Others can always then get the latest from your project by  **pulling**  your changes down from the remote (and onto their computer). This is how everyone can work on a project together without needing access to your computer where your local copy is stored.

![git_remote_image](https://github.com/ad1tya-v3rma/hackober-repo--1/blob/main/images/remote.PNG)

*The illustration shows a server (e.g. by GitHub), holding the **remote** repository and two computers, each of them holding a **local** copy of the repository. You can either access and edit the remote repository with your browser or edit the repository locally and tell your computer (on **terminal**) to talk to the server.*

<br>

### Create a Remote Repository

You want to sync your  **local**  version with one stored on GitHub.com. First create a new  **remote**  repository on GitHub.com.

-   Go to  [github.com](https://github.com), log in, and click the '+' in the top right and then click 'New repository'.
-   Give it a name that matches your local repository's name, 'hello-world', and a short description.
-   Make it public. This means it'll be listed on your public profile.
-   Don't initialize with a README because we already have a file, locally, named 'readme.txt'. This is a helper option from GitHub if you hadn't already made it.
-   Don't initialize with '.gitignore' or a license, we won't use them in this tutorial.
-   Click create repository!

<br>


## Readmes, .gitignores and Licenses

These are common files in open source projects so to make starting a new project easier, GitHub provides an option for creating them for you.

A  **readme**  explains what the project is, how to use it, and often times, how to contribute (though sometimes there is an extra file, 'CONTRIBUTING.md', for those details).

A  **.gitignore**  is a list of files that Git should  _not_  track, for instance, files with passwords!

A  **license**  file is the type of license you put on your project. This lets others know how they can use it. Information on the types is here:  [choosealicense.com](https://choosealicense.com).

<br>

### Connect your Local to your Remote

Now you've got an empty repository started on GitHub.com. At the top you'll see 'Quick Setup', make sure the 'HTTPS' button is selected and copy the address—this is the address of your repository on GitHub's servers.

Back in your terminal, and inside of the 'hello-world' folder that you initialized as a Git repository in the earlier challenge, you want to tell Git to remember the address of the remote version on GitHub's servers. You can have multiple remotes so each requires a name. The primary remote is typically named  `origin`.

To add a remote named 'origin' to your repository:

`git remote add origin <URLFROMGITHUB>`

Your  **local**  repository now knows where your  **remote**  repository, named 'origin', lives on GitHub's servers. Think of it as adding a name and address on speed dial—now when you need to send something there, you can.

<br>

**Windows Users:**

If you have  **GitHub Desktop**  on your computer, a remote named 'origin' is automatically created in your local repository. In that case, you'll just need to tell it what URL to associate with 'origin'. Use this command instead of the 'add' one above:

`git remote set-url origin <URLFROMGITHUB>`

<br>


### Push Work to your Remote

Next you want to  **push**  (send) everything you've done locally to your remote repository on GitHub. This is something you'll do often so that your remote version is up to date and matching the state of your local version.

Git has a branching system so that you can work on different parts of a project at different times. We'll learn more about that later, but by default the first branch is named 'master'. When you push (and later pull) from a project, you tell Git the  **branch name**  you want and the name of the  **remote**  that it lives on.

In this case, we'll send our branch named 'master' to our remote on GitHub named 'origin'.

`git push origin master`

Now go to your remote repository's page on GitHub.com and refresh the page.  **Wow!**  Everything is now the same locally as it is remotely. Congrats on your first public repository!

<br>

# MORE ABOUT GIT

> ## Forks

<br>

So far you have made a project locally and pushed it to GitHub, but that's only half the fun! The other half is working with other people and other projects.

When you  **fork**  a repository, you create a copy of it on your GitHub account. Your forked copy begins its own life as a  **remote**  repository. Forks are used for creating your own version of a project and - if desired - for contributing your changes back to the original project (such as bug fixes or new features).

To get a forked repository from your GitHub account onto your computer you  **clone**  it. This cloning action copies the remote repository onto your computer so that you can work on it locally.


![git_fork_image](https://github.com/ad1tya-v3rma/hackober-repo--1/blob/main/images/fork.PNG)

*By **forking** a foreign repository, you create a copy of the project as a new **remote** repository on your own GitHub Account. After **cloning** this new repository to your computer, you can work on it, **push** your changes to the server and even **pull** other peoples changes to your local copy. You can of course pull changes from the original repository too, but - as long as you don't have write-access - you can not push your changes there. We'll learn more on pulling later on.*

<br>

### Fork the Patchwork Repository

The project we'll work with is at  [github.com/jlord/patchwork](https://github.com/jlord/patchwork). Go to that page and click the 'Fork' button at the top right. Once the forking animation is complete, you have a copy on your account. Copy your fork's HTTP URL from the address bar in your browser, this is the address of your fork on GitHub's servers.

<br>

### Clone Your Fork Locally

Now, in terminal, you'll clone the repository onto your computer. It will automatically create a new folder for the repository so there is no need to create one yourself. But make sure you aren't cloning it inside of another Git repository folder!

So be sure you're not inside of the 'hello-world' directory from the previous challenges. To back out and leave this folder so that you can clone, follow these steps:

Back out of your 'hello-world' folder:  
Tip: the two dots mean step out of a directory one level

`cd ..`

Now that you're no longer in another Git repository, clone your fork:

`git clone <URLFROMGITHUB>`

Go into the folder it created for your local copy of the fork (in this case, named 'patchwork').

`cd patchwork`

Now you've got a copy of the repository on your computer and it is automatically connected to the remote repository (your forked copy) on your GitHub account. Type  `git remote -v`  to see that the address to the fork is already set up.

<br>

### Connect to the Original Repository

What if the original repository you forked happens to change? You'll want to be able to  **pull**  in those changes too. So let's add another remote connection, this time to the original,  [github.com/jlord/patchwork](https://github.com/jlord/patchwork), repository with its URL.

You can name this remote connection anything you want, but typically people use the name 'upstream'; let's use that for this.

`git remote add upstream https://github.com/jlord/patchwork.git`

To be sure you have the correct remotes set up, type  `git remote -v`  to list out the addresses you have stored.  **You should have an 'origin' remote with your fork's address and then an 'upstream' remote with the address to the original, the URL noted above in this step.**


<br>

> ## Branches

<br>

Git repositories use branches to isolate work when needed. It is common practice when working together on a project to create a  **branch**  to keep your working changes in. This allows different changes to be developed on separate branches without interfering with each other. When the work on your branch is finished, you merge your changes back into the main branch (commonly named 'master'). This main branch thus always contains a stable version of the project.

![git_branch_image](https://github.com/ad1tya-v3rma/hackober-repo--1/blob/main/images/branch.PNG)

*The diagram illustrates how you can branch off of your 'master' branch (the straight black line in the middle), do your work on a branch (dots illustrate commits) and then merge those changes back into 'master'. You can even branch off of a branch if you need to, the 'master' branch doesn't have to be the base.*
For a great visualization on how branches work in a project, see this GitHub Guide:  [guides.github.com/overviews/flow](http://guides.github.com/overviews/flow/)

<br>

## GitHub Pages

GitHub will automatically serve and host static website files in branches named 'gh-pages'. This free service is called  [GitHub Pages](http://pages.github.com). Since the project you forked creates a website, its main branch is named 'gh-pages' instead of 'master'. All repositories that have a 'gh-pages' branch with website files can be found, live online, using this pattern for the URL:

`http://githubusername.github.io/repositoryname`

<br>

### Create a branch

While still inside of your local 'patchwork' repository, type  `git status`  to see what branch you're currently on. Git should reply that you're on the 'gh-pages' branch.

Now create a new branch and name it "add-username", where 'username' is your username. For instance, "add-jlord".  **Branches are case-sensitive so name your branch exactly the way your GitHub name appears**.

`git branch <BRANCHNAME>`

Now you have a new branch that is identical to 'gh-pages' but has a new name.

To go into that branch and work on it you  **checkout**  a branch. Go on your new branch:

`git checkout <BRANCHNAME>`

<br>

### Step: Create a new file

Back in your text editor:

-   Create a new file named "add-username.txt", where 'username' is your username. For instance, "add-jlord.txt".
-   Then, just write your GitHub username in it, that's it and that's all. For instance, I'd type 'jlord'.
-   Save this file in the 'contributors' folder in Patchwork:  **Patchwork/contributors/add-username.txt**
-   Next, check in your changes (see below).

<br>

### Check-in

You already know the steps for checking in your changes:

`git status`

`git add <contributors/FILENAME>`

`git commit -m "commit message"`

Now push your update to  **your fork**, 'origin', on GitHub:

`git push origin <BRANCHNAME>`


<br>

> ## Didn't Pass?
 
<br>

#### Permission denied...error: 403

You are pushing changes to a repository you don't have write access to. In this case, you're likely pushing to the original 'jlord/patchwork'. Make sure that you're pushing to 'origin' and that it points to your fork's address on GitHub. To check and see what your remotes are and where they point run  `git remote -v`. You should have 'upstream' pointing to 'jlord/patchwork' and 'origin' pointing to 'yourusername/patchwork'.

To fix a remote that is pointing to the wrong place you can re-set its url:  `git remote set-url origin` .

<br>

#### Authentication failed...error: 401

Your identity could not be verified. You may have 2FA (Two Factor Authentication) turned on in which case you must use a personal access token as your password. You can generate one by  [following these instructions](https://help.github.com/articles/creating-an-access-token-for-command-line-use). You'll need to keep this and use it in place of your password when prompted. You can also  [save this access token](https://help.github.com/articles/caching-your-github-password-in-git/)  on your computer so that you don't have to re-enter it.

<br>

#### File NOT in contributors folder

The file you create should be placed inside the existing 'contributors' folder in the Patchwork repository. If you put it somewhere else, simply use Finder or Windows Explorer to move your file into the folder. You can check  `git status`  again and you'll find it sees your changes. Stage and then commit all of these changes (additions and deletions) with the commands below.

`git add -A`

`git commit -m "move file into contributors folder"`

<br>

#### Branch name expected: _____

The branch name should match your user name exactly. To change your branch name:

`git branch -m <NEWBRANCHNAME>`

When you've made your updates, verify again!


<br>
<br>

> ## Social Coding

<br>


Working with others is one of the best things about GitHub because it is easier to work from any place or timezone with someone else.

**Collaborators**  are other GitHub users who are given permission to make edits to a repository owned by someone else. You may also hear the term  **contributor**, this describes another GitHub user who has made contributions, through a Fork and Pull Request, to a project.

[@reporobot](https://github.com/reporobot) is a robot from outer space that loves collaborating on repos.



<br>

### Hello, Repo Robot!

To add collaborators to one of your projects, visit the repository's page on your GitHub account and click the 'Settings' tab in the menu in the upper part of the page. Then select the 'Manage access' option and click on 'Invite a collaborator'. Type the username into the text box, select the right user and finally add the collaborator to your repository by clicking the green button.

**Now go to your forked Patchwork repository's page on GitHub and add 'RepoRobot' as a collaborator.**  The URL should look like this, but with your own username.

`https://github.com/YOURUSERNAME/patchwork/settings/access`

<br><br>

> ## Pulling from a Remote

<br>

If you're working on something with someone else you need to stay up to date with the latest changes. So you'll want to  **pull**  in any changes that may have been pushed to the central GitHub repository.
  

![git_fork_image](https://github.com/ad1tya-v3rma/hackober-repo--1/blob/main/images/remote.PNG)

*If someone else **pushed** changes to the **remote** repository (on GitHub), you might want to **pull** these changes into your **local** repository.*

<br>

### What has Reporobot been up to?

See if Reporobot has made any changes to your branch by pulling in any changes from the remote named 'origin' on GitHub:

`git pull <REMOTENAME> <BRANCHNAME>`

If nothing's changed, it will tell you 'Already up-to-date'. If there are changes, Git will merge those changes into your local version.

Did Reporobot make changes? Git tells you where changes were made. You can open that file and see Reporobot's updates. Surprise, Reporobot is an artist!


<br>
<br>

> ## Pull Requests

<br>

Often when you make changes and improvements to a project you've forked, you'll want to send those changes to the maintainer of the original and  **request**  that they  **pull**  those changes into the original so that everyone can benefit from the updates—that's a  **pull request**.  

![git_pull_request_image](https://github.com/ad1tya-v3rma/hackober-repo--1/blob/main/images/pull%20request.PNG)

*Two files, belonging to the original repository (the red one on the left) and your forked repository (the blue one on the right) respectively. If you want to integrate your changes into the original repository, you'll need to create a pull-request, asking the maintainers to pull your changes over..*

### Create a pull request

We want to add you to the list of workshop finishers, by creating a  **pull request**  to add your username file to the original repository.

Therefore now visit the original repository you forked on GitHub, in this case  [https://github.com/jlord/patchwork](https://github.com/jlord/patchwork).

Often GitHub will detect if you've pushed a branch to a fork and display it at the top of the original's website. If you see that with your 'add-username' branch, you can click to create a Pull Request from there. If not:

-   Click the green 'New pull request' button.
-   Select the branch with the changes you want to submit. It should be the one with 'add-yourusername'.

You'll now see a page with the details of the pull request you're in the process of submitting. This page shows the commits and changes, in the form of a diff, associated with your pull request as compared to the 'gh-pages' branch of the original.

If the original repository has a  **contribution documentation**, GitHub will link to it. This is documentation from repository owners on how to best make contributions to that project—very helpful to read if you'd like to see your changes adopted!

If everything on the page looks good and as you expect it:

-   Click 'Create pull request'
-   Add a title and description to the changes you're suggesting the original author pull in.
-   Click 'Send pull request'!

<br>

**Bingo! You submitted a pull request—take a few seconds to bask in the moment.**

If all is well with your pull request, it will be merged within moments. If it's not merged automatically within a few minutes, you'll then likely have some comments from @reporobot on why it couldn't merge it. If this is the case, close your pull request on GitHub, make the necessary changes to your branch, push those changes back to your fork and reopen (this will poke @reporobot to look over it again) your pull request.


<br>
<br>

> ## Cleaning up

<br>

Once you don't need branches anymore you can delete them locally and remotely. This is helpful so that you don't end up with a pile of old branches.

<br>

### Merge Locally

Your pull request has been merged! Your branch was merged into the 'gh-pages' branch of the original on GitHub. You can merge your branch locally, too.

First, move into the branch you want to merge into — in this case, the branch 'gh-pages'.

`git checkout gh-pages`

Now tell Git what branch you want to merge in — in this case, your feature branch that begins with "add-".

`git merge <BRANCHNAME>`

Tidy up by deleting your feature branch. Now that it has been merged you don't really need it around.

`git branch -d <BRANCHNAME>`

You can also delete the branch from your remote on GitHub:

`git push <REMOTENAME> --delete <BRANCHNAME>`

<br>

### Pull from Upstream

And last but not least, the original has changed since your pull request was merged — Reporobot added your name to the website! If you pull in these changes from upstream you'll be up to date and have that version too. You can actually see it live as well at: yourusername.github.io/patchwork.

To pull from the original upstream:

`git pull upstream gh-pages`

# Congratulations!

> You've created local repositories, remote repositories, worked with a collaborator, pushed, pulled and joined the millions of others developing and enriching open source!
