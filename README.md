> # Get Git
<br>

## **Goal**
Install Git on your computer and configure your name and email.

<hr><br>

## Git

Git is free  **open source software**  (the  [source code is public](https://github.com/git/git)) written by Linus Torvalds who also wrote the Linux operating system's kernel.

Git is a program for keeping track of changes over time, known in programming as  **version control**. If you've used a track changes feature in a text editing software then you're already familiar with the concept!

<hr><br>

## Install Git

We recommend installing Git on your computer by installing the  [latest version](https://git-scm.com/downloads)  from the Git website.

-   **Windows**: Use the  **Git Shell**  for your terminal.
-   **Mac**: You can use the  **terminal**  app as your terminal.

Already have Git or not sure? Type  `git --version`  in your terminal and if it returns a version number higher than  `1.7.10`, you're set! For more information, visit the  [Git website](http://git-scm.com).

<hr><br>


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

<hr><br>


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


<hr><hr><br>

> # REPOSITORY
<br>

## **Goal**
Install Git on your computer and configure your name and email.

<hr><br>

## Repositories

A  **repository**  is a collection of related items. In our case, when writing software, it is a collection of files related to a software project. You can imagine it as a project folder with all the relevant files inside of it. In fact, that's what it will look like on your computer anyways. Sometimes they're called 'repos' for short

***Repositories just look like normal folders on your computer. However there is an important difference: Their content is beeing tracked by Git.***

You tell Git what your project is and Git will start tracking all of the changes to that folder. This makes it a Git repository: a folder of items being tracked by Git. Git tracks when files are added, subtracted or even a single letter in a single file is changed. All of this plus who did it and when is tracked by Git. In software, tracking changes like this is called version control.

<hr><br>

## Using Terminal

**Terminal**  (or Bash) is a way to instruct your computer to do things by typing commands rather than clicking applications with your mouse. You can rename files, open files, create new folders, move between directories (folders) and more all by running typed commands. You can even use a text editor for code (like  [Vim](http://en.wikipedia.org/wiki/Vim_(text_editor))) in your terminal an never have to leave!

Besides navigating your computer, you can also use programs in Terminal that have a  **command-line interface (CLI)**, meaning they can be run with commands in terminal. Git is one of these. The first part of the command lets your computer know you're talking to Git. The parts following that are the commands and the different options you want Git to act on.

In Git-it you'll learn a few basic command-line actions (in addition to Git commands) for navigating your computer. They're described within the steps.

<hr><br>

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


<hr><hr><br>

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

<hr><br>


### Step: Make More Changes

Now add another line to 'readme.txt' and save the file again.

In terminal, you can view the  **diff**erence between the file now and how it was at your last commit.

Tell Git to show you the  **diff**:

`git diff`

Now with what you just learned above, commit this latest change.


<hr><hr><br>

> # CONNECTING GITHUB
<br>


## Working Better, Together

The repository you've created so far is just on your computer, which is handy, but makes it pretty hard to share and work on with others. No worries, that's what GitHub is for!

GitHub is a website that allows people everywhere to upload what they're working on with Git so that everyone can easily work together on the same project. GitHub which acts as the central repository for you and everyone else to share. You push your changes to it and pull down changes from others.

<hr><br>

### Create a GitHub Account

Visit  [github.com](https://github.com)  and sign up for a free account.  **High five, welcome!**

<hr><br>

### Add GitHub username to Git

Add your GitHub username to your Git configuration. We'll do this just for the sake of Git-it; it makes it easier to verify the upcoming challenges. Save it exactly as you created it on GitHub and  **capitalize where capitalized**. Note, you don't need to enter the "<" and ">".

Add your GitHub username to your Git configuration:

`git config --global user.username <UserName>`

You can double check what you have set in your Git config by typing:

`git config --global user.username`



<hr><hr><br>

> # REMOTE CONTROL
<br>


## Remotes

When you put something on GitHub that copy lives on one of GitHub's servers. This makes it a  **remote**  repository because it is not on your computer, but on a server, "remote" and somewhere else. By  **pushing**  your  **local**  (on your computer) changes to it, you keep it up to date.

Others can always then get the latest from your project by  **pulling**  your changes down from the remote (and onto their computer). This is how everyone can work on a project together without needing access to your computer where your local copy is stored.

*The illustration shows a server (e.g. by GitHub), holding the **remote** repository and two computers, each of them holding a **local** copy of the repository. You can either access and edit the remote repository with your browser or edit the repository locally and tell your computer (on **terminal**) to talk to the server.*

<hr><br>

### Create a Remote Repository

You want to sync your  **local**  version with one stored on GitHub.com. First create a new  **remote**  repository on GitHub.com.

-   Go to  [github.com](https://github.com), log in, and click the '+' in the top right and then click 'New repository'.
-   Give it a name that matches your local repository's name, 'hello-world', and a short description.
-   Make it public. This means it'll be listed on your public profile.
-   Don't initialize with a README because we already have a file, locally, named 'readme.txt'. This is a helper option from GitHub if you hadn't already made it.
-   Don't initialize with '.gitignore' or a license, we won't use them in this tutorial.
-   Click create repository!

<hr><br>


## Readmes, .gitignores and Licenses

These are common files in open source projects so to make starting a new project easier, GitHub provides an option for creating them for you.

A  **readme**  explains what the project is, how to use it, and often times, how to contribute (though sometimes there is an extra file, 'CONTRIBUTING.md', for those details).

A  **.gitignore**  is a list of files that Git should  _not_  track, for instance, files with passwords!

A  **license**  file is the type of license you put on your project. This lets others know how they can use it. Information on the types is here:  [choosealicense.com](https://choosealicense.com).

<hr><br>

### Connect your Local to your Remote

Now you've got an empty repository started on GitHub.com. At the top you'll see 'Quick Setup', make sure the 'HTTPS' button is selected and copy the address—this is the address of your repository on GitHub's servers.

Back in your terminal, and inside of the 'hello-world' folder that you initialized as a Git repository in the earlier challenge, you want to tell Git to remember the address of the remote version on GitHub's servers. You can have multiple remotes so each requires a name. The primary remote is typically named  `origin`.

To add a remote named 'origin' to your repository:

`git remote add origin <URLFROMGITHUB>`

Your  **local**  repository now knows where your  **remote**  repository, named 'origin', lives on GitHub's servers. Think of it as adding a name and address on speed dial—now when you need to send something there, you can.

<hr><br>

**Windows Users:**

If you have  **GitHub Desktop**  on your computer, a remote named 'origin' is automatically created in your local repository. In that case, you'll just need to tell it what URL to associate with 'origin'. Use this command instead of the 'add' one above:

`git remote set-url origin <URLFROMGITHUB>`

<hr><br>


### Push Work to your Remote

Next you want to  **push**  (send) everything you've done locally to your remote repository on GitHub. This is something you'll do often so that your remote version is up to date and matching the state of your local version.

Git has a branching system so that you can work on different parts of a project at different times. We'll learn more about that later, but by default the first branch is named 'master'. When you push (and later pull) from a project, you tell Git the  **branch name**  you want and the name of the  **remote**  that it lives on.

In this case, we'll send our branch named 'master' to our remote on GitHub named 'origin'.

`git push origin master`

Now go to your remote repository's page on GitHub.com and refresh the page.  **Wow!**  Everything is now the same locally as it is remotely. Congrats on your first public repository!

<hr><br>

