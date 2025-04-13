# Git Client

Git binary is available in most good operating systems or from [Git SCM website](https://git-scm.com/){target=_blank}


## Quick Start

Configure Git identity

```shell
git config --global user.name "your name"
git config --global user.email "your.name@domain.com"
```

!!! HINT "Anonymise email for user"
    GitHub user account **Settings** > **Emails** has an option to use a `@users.noreply.github.com` address rather than the real email address.

    The noreply address should be set as the `user.email` configuration.


Initialise a local repository (inside your project directlory)

```shell
git init
```

Status of your files and all uncommited changes

```shell
git status
```

Tell Git which changes you want to make part of the next commit (staging)

```shell
git add filename       ; to add a specific file
git add .              ; to add everything
git add *.HTML         ; add all html files
```

Commit those files to create a new version

```shell
git commit -m "meaningful commit message"
```

Push your code to a remote repository (eg. Github)

```shell
git remote add repo-name git@github.com:github-account/repo-name.git
git push repo-name master
```


<!-- git-local-workflow.png -->
