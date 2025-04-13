title: Git Common Pitfalls
---

Here are some common pitfalls that people experience when using git and of course ways to dig yourself out of them.

## Loosing your head

Confusing Git leads to your confusion


## Staging and Commiting to the wrong branch

[Undo a commit to a local branch ]

If using the command line for git, enhance your prompt to display the current branch you are on.

Use Git status ....

Learn how to use your git tool well, so that it visualises the current branch you are on or asks / checks you are pushing to the correct branch.



## Pushing to the wrong repository

Warn everyone immediately, the longer you wait the more pain people will feel. 

Best approach is to create a new commit that resolved the problem you just created.


## Staging the wrong files 

Learn to use git diff well to see the changes before you add them.

Use git status to see which files have been modified and which ones you have addded.

[Undo staging a file, when tracked and untracked]


## Staging unwanted changes in a file

- eg whitespace, formatting changes 

Use `git add -p filename` to select only the lines (hunks) you want to stage.

Use `git checkout filename` to reset the file to be the same as that committed in Git, wiping out any unwanted changes (perhaps made by mistake or by your code writing tools).


