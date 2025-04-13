title: Checking for Changes
---

Git provides several commands to help you see changes in your project files, helping you manage your project easily and helping you capture small and coheirent changes.

## Git Status 

Even experienced Git users will run the `git status` command very frequently.  This command gives you an overview of all the files that contain changes, changes that have been staged and any files Git is not currenly tracking 

> untracked files are those that have not been added to the Git repository

If you are using a GUI client for Git, it may be running `git status` regularly in the background so the information it is displaying is up to date.

Git status only shows the changes happening locally, it will not show changes on any remote repository (ie. on Github).  See the section on `git log` for tracking changes in remote repositories.

{% note info Exercise 1 %}
This is a note, I wonder if it works.  Yes it does, but it looks just like a blockquote using the > notation
{% endnote %}

## Git Diff 

Compare changes between the working copy and the staging area.  You can compare all files in the project or just the changes in a specific file or filename pattern 

    git diff 
    git diff filename 
    git diff *.md


Compare changes between the staging area and the latest commit 

    git diff --cached 
    git diff filename --cached
    git diff *.md --cached 


Compare changes against a specific commit (version)

    git diff v1.09       ; compare working directory against specific version
    git diff dev master   ; difference between two branches


Using the `--stat` option to see just the statistics about the changes - eg, you want to see the number of changes rather than all the change details.

    git diff v1.09 --stat 

