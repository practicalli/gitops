title: Identify yourself to Git
---

There are lots of useful things to add to your git configuration.  The most important thing is to set up your git user name and email, so people know who is creating commits.  To add your username and email to git, either edit the `~/.gitconfig` file or run the following two commands:

    git config --global user.name "your name"
    git config --global user.email "your.name@domain.com"

> You should use the same email address you have used for your Github account to make things easier.

To check what has already been added to Git (some gui clients add information to your gitconfig), you can list all the current configuration entries using the command:

    git config --list


Later in this workshop we will see how to set up aliases for the commands and options you regularly use.  We will also show how to set up specify tools for merging changes and viewing *diffs* (differences between files and commits).

Read the [official documentation on git customisation](http://git-scm.com/book/en/Customizing-Git-Git-Configuration) for more options.

