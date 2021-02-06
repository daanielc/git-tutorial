# Git Instructions

## Motivation for Version Control 

* Track changes in complex code
* Share code efficiently with others
* Keep track of who contributes what to code
* Be able to rollback changes that create problems

## Basics of a Repository

* Fundamentally a folder on your computer
* Every file in it is either "tracked" or "ignored"
* When changes are made in "tracked" files, the user will "commit" them to the repository
* Commited changes can then be "pushed" to a remote repository (GitHub)
* Changes pushed by others to the remote repository can be "pulled" to the user's local repository
* If multiple things are being developed in parallel, a repository can be split into multiple branches which can be worked on independently

## Install Git

Open the "Terminal" program on your computer and run the command:
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

Once Homebrew has installed, run the command:
```bash
brew install git
```

## Clone a Repository

In the terminal, run the command:
```bash
mkdir ~/Desktop/git-tutorial
```
then
```bash
cd ~/Desktop/git-tutorial
```
and finally
```bash
git clone https://github.com/DaanielC/git-tutorial.git
```

## Create Your Own Repository

First, create a new directory to store your project in:
```bash
mkdir ~/Desktop/first-repo
```
and go into that folder:
```bash
cd ~/Desktop/first-repo
```
Then create a `readme.md` file. An easy way to start this quickly is:
```bash
echo "# first-repo" >> readme.md
```
Then initialize the Git repository:
```bash
git init
```
Add `readme.md` as a tracked file in the repository:
```bash
git add readme.md
```
And commit the change to `readme.md` with a message:
```bash
git commit -m "first commit"
```
Finally, define which branch you are working on:
```bash
git branch -M main
```
## Push Changes to GitHub

Go to [GitHub](github.com) and create an account. It is probably best to sign up with an email address that you will continue to use for a long time, but you can also link your Rowland Hall email address later to get a bunch of professional software for free.

Once you have created your account create a new project called "first-repo"

Back in your command line, run
```bash
git remote add origin https://github.com/[Your User Name]/first-repo.git
```
and substitute in your GitHub user name.

Then run
```bash
git push -u origin main
```
When you refresh the page for your repository on GitHub, you should see that your `readme.md` file has been added.

## Practice

* Clone Dr. Kuntz' machine learning repository and try to run one of the scripts in your MATLAB
* Put your code so far into a Git repository with a `readme.md` and push it to a repository on your personal GitHub

## Additional Resources

* [Git Cheat Sheet](git-cheat-sheet.pdf)
* [Markdown Cheat Sheet](https://www.markdownguide.org/cheat-sheet/)
* [VSCode](https://code.visualstudio.com/) for more convenient Markdown editing and simple Git operations
* [GitHub Student Developer Pack](https://education.github.com/pack) for free stuff
* You can try using a more robust [Git GUI Client](https://git-scm.com/downloads/guis) if you want, but I find them to be a lot slower than the command line





