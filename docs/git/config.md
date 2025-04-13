# Git Config

[Git customisation documetation](http://git-scm.com/book/en/Customizing-Git-Git-Configuration){target=_blank .md-button}

## Configure git

- github email private with alias for public address, to prevent spam
- default branch
- github token
- using Magit forge


=== "FreeDesktop XDC"

`$XDG_CONFIG_HOME/git/config` Git client configuration

`$XDG_CONFIG_HOME/git/ignore` patterns to ignore when showing git status


=== "Default locations"

`.gitconfig` git client configuration

`.gitignore-global` patterns to ignore when showing git status


??? EXAMPLE "Practicalli Git Configuration"
    ```config title="Git Config"
    # Practicalli Git Configuration
    # Adjust paths if not saved in `~/.config/git/`

    ## ------ Identity ------ ##

    # Default identity configuration
    [include]
            path = ~/.config/git/identity-practicalli-john

    # Over-ride identify for specific directories
    [includeIf "gitdir:~/projects/company-name"]
            path = ~/.config/git/identity-company-name

    ## ------ Git Behaviour ------ ##

    [core]
        # Set which editor to use for editing commit messages (when not included with -m)
        # VISUAL or EDITOR environment variables also set the choice of editor
        # vi used if not set.  Typical examples are nvim or emacsclient
        editor = nvim

        # file and directory patterns to ignore across all projects
        excludesfile = ~/.config/git/ignore

        # Tool to page through long output (e.g. git log). `less` is default
        # pager = less

        # Ensure Linux & MacOSX line endings in checked out text files
        autocrlf = input

    [commit]
        # Default commit message - useful if team has a commit message policy
        template = ~/.config/git/commit-message-template

    [init]
        # scripts and hooks to add when creating a new local Git repository
        # templateDir = ~/.config/git/repo-template/

        # default branch name when creating a new local repository
        defaultBranch = main

    [merge]
        # Include common parent when merge conflicts arise
        conflictstyle = diff3

    [fetch]
        # Remove deleted remote branches from local repository
        prune = true

    [merge]
        # Include common parent when merge conflicts arise
        conflictstyle = diff3

    [push]
        # Set local brach to track new remote branch automatically
        # Requires Git 2.37.0
        autoSetupRemote = true

    ## ------ Git commands ------ ##

    # command line shot cuts
    [alias]
        branches = branch -av
        tags = tag -l
        lg = log --graph --decorate --relative-date --oneline
        sitrep = status -sb
        word = diff --word-diff
        unstage = reset HEAD
        empty = "git commit --allow-empty"

        # delete locate branches merged into the remote
        delete-local-merged = "!git fetch && git branch --merged | egrep -v 'master' | xargs git branch -d"

    # Clone short-cuts
    [url "git@github.com:practicalli/"]
        # git clone practicalli:repo-name
        insteadOf = practicalli:

    [help]
        # Automatically change incorrectly typed commands
        # Set timeout (in 0.1 second steps) before git automatically changes the command
        # autocorrect = 50
    ```

!!! EXAMPLE "Git Identity configuration"
    Practicalli uses separate identity files for open source and commercial work.
    ```config title="identity-practicalli-john"
    ## ------- Identity ------- ##
    # Add identity to all commits (required for GitHub / GitLab)
    [user]
        name = John Practicalli

        # Use GitHub no-reply email address to keep real address private
        email = "250870+practicalli-john@users.noreply.github.com"

        # For signed commits and signed annotated tags
        # https://www.git-scm.com/book/en/v2/Git-Tools-Signing-Your-Work#_signing
        # signingkey = <gpg-key-id>

    ## Identity for using GitHub API
    [github]
        user = practicalli-john

        # Use `authinfo.gpg` to store tokens for greater security
        # oauth-token = ghp_verylongtokenwithlotsofrandomlygeneratedcharacters
        # host = api.github.com

    # [credential]
    #     helper = osxkeychain
    ```

    ```config title="Identity for specific Company work"
    ## ------- Identity ------- ##
    # Add details for specific company identity

    # Add identity to all commits (required for GitHub / GitLab)
    [user]
        name = John Practicalli

        # Use GitHub no-reply email address to keep real address private
        email = "account-name@company-name.com"

        # For signed commits and signed annotated tags
        # https://www.git-scm.com/book/en/v2/Git-Tools-Signing-Your-Work#_signing
        # signingkey = <gpg-key-id>

    ## Identity for using GitHub API
    [github]
        user = practicalli-john

        # Use `authinfo.gpg` to store tokens for greater security
        # oauth-token = ghp_verylongtokenwithlotsofrandomlygeneratedcharacters
        # host = api.github.com

    # [credential]
    #     helper = osxkeychain
    ```

## Core configuration

Configure a Git identity by adding user name and email which is added to each commit created by that user

either edit the `~/.gitconfig` file or run the following commands

Configure user name


```shell title="Configure Git Identity"
git config --global user.email=obfuscated-name@github.com
```

Use the email address used for the Github / GitLab account, or use and obfuscated email address provided by the GitHub account

```shell title="Configure Git Identity"
git config --global user.email=obfuscated-name@github.com
```

To check what has already been added to Git (some gui clients add information to your gitconfig), you can list all the current configuration entries using the command:

```shell
git config --list
```



> Use the same email address you have used for your Github account to make things easier.

To check what has already been added to Git (some gui clients add information to your gitconfig), you can list all the current configuration entries using the command:


Later in this workshop we will see how to set up aliases for the commands and options you regularly use.  We will also show how to set up specify tools for merging changes and viewing *diffs* (differences between files and commits).



## Global Ignore file

Add patterns that should be ignnored across all projects, such as editor specific configurations and operating system backup files

Example global-git-ignore file



## ssh keys

generate an SSH key with

```shell title="Generate SSH key"
ssh-keygen -t rsa -C email-name@domain.com
```
TIP:  Use an actual phrase or a series of random words with spaces
TIP: store the passphrase in the keyring of the operating system, and have it unlock the key when you login


## Developer token

for use with other tools such as Emacs Magit
