title: Git in 2 minutes
date: 2014-08-24 18:22:00
---

If you have installed Git and know the basic theory of version control, here are the basic commands to get you going:

    ;; Tell Git who you are (only done once)
    git config --global user.name "your name"
    git config --global user.email "your.name@domain.com"

    ;; Initialise a local repository (inside your project directlory)
    git init
    
    ;; See the status of your files and all uncommited changes
    git status 
    
    ;; Tell Git which changes you want to make part of the next commit (staging)
    git add filename       ; to add a specific file
    git add .              ; to add everything
    git add *.HTML         ; add all html files 
    
    ;; Commit those files to create a new version 
    git commit -m "meaningful commit message"
    
    ;; Push your code to a remote repository (eg. Github)
    git remote add repo-name git@github.com:github-account/repo-name.git
    git push repo-name master


> The `;` character is a comment

To see the basics of Git useage visualised, here is a diagram of the local git workflow:

<img class="img-code" src="images/git-local-workflow.png">



