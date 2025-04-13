title: Creating a Git version controlled project
---

Create a new folder / project by either creating the project structure yourself or using a build tool to create it for you.  Here are some of the example build tools you could use:

    ## Node project
    npm init
    
    ## Node project via Grunt-init
    grunt-init my-template

    ## Project via Yoman generator 
    yo generator 

    ## Java project with Maven 
    mvn new my-project
    
    ## Clojure project with Leiningen 
    lein new my-project
    
    ## Scala project using Play framework
    play new my-project


Now you can see all the files you have created as untracked files in git using

    git status


Show example screenshots of git status output for the above projects

