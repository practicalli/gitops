# Git tutorial

This tutorial will give you a practical guide to using the Git version control tool to managing changes to source code and configuration files in projects.  The tutorial also covers collaborating on projects using Github public repositories.  You can either read an [overview of Git](overview-of-git.html)

## Setting up Git & Github
- [Choose your git client](choose-your-git-client.html)
- [Identify yourself to Git](identify-yourself-to-git.html)
- [Create an account on Github](create-account-on-github.html)


## Creating Git Projects
* [Creating a Git managed project](chapter05-creating-a-git-managed-project.html)
* [Ignoring files](chapter06-ignoring-files.html)


## Local Git Workflow
* Checking the status - what has changed -- git status, git diff
* Staging changes  - basic add, git add -p, unstaging untracked files, unstaging tracked files, git diff --cached
* Committing a new version
* Git log
* [Chapter 7: The local git workflow](chapter07-local-git-workflow.html)


## Branching & Merging  - why do this
- try out code and modifications to design, different algorithms
- easily discard changes that are not needed - or leave them in a branch so they are not affecting / poluting the main codebase

* [Branching and Merging](chapter09-branch-and-merge.html)
* [merging changes](merging-changes.html)


## Collaborating with other developers using Git and Github
* [Chapter 10: Collaborating with Github](collaborating-with-github.html)
* Practices to avoid when using shared repos like Github
- rebasing, forgetting to push changes (especially for sub modules)


## Troubleshooting]
- what to do if you loose your head
- if you really have to change a commit
- unstage changes


## Resources
* Git submodules


# Git local workflow visualised

You can quickly get versioning your code with Git, all on your own computer.  You do not need to set up a server.

<img class="img-code" src="images/git-local-workflow.png">

# Git and Github workflow visualised

To give you a big picture view of how you use Git and Github, here is a visualisation of the workflow for both.  The details of this workflow are ocvered in the workshop from [Chapter 10: Collaborating with Github](chapter10-collaborating-with-github.html) onwards.

<img class="img-code" src="images/git-and-github-workflow.png">

# Reference

* [Git essential commands](/developer-guides/git-quickstart-guide.png) for the most common commands for using Git
* [Git Visual cheat sheet](http://ndpsoftware.com/git-cheatsheet.html)
* [Git Reference](http://gitref.org/)
* [Learning Version Control wth Git](http://www.git-tower.com/learn/ebook/command-line/introduction) - git-tower.com
* [StarLogs.net demo from my blog](http://starlogs.net/#jr0cket/jr0cket.github.io-hexo)
