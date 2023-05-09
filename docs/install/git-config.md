# Git Config

Configure Git page




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

Later in this workshop we will see how to set up aliases for the commands and options you regularly use.  We will also show how to set up specify tools for merging changes and viewing *diffs* (differences between files and commits).

Read the [official documentation on git customisation](http://git-scm.com/book/en/Customizing-Git-Git-Configuration) for more options.


 username and email

 using obfuscated email address

## Global Ignore file

Add patterns that should be ignnored across all projects, such as editor specific configurations and operating system backup files

Example global-git-ignore file



## ssh keys

generate an SSH key with

```shell title="Generate SSH key"
ssh-keygen -t rsa -C email-name@domain.com
```


## provide long passphrase

TIP:  Use an actual phrase or a series of random words with spaces
TIP: store the passphrase in the keyring of the operating system, and have it unlock the key when you login



## Developer token

for use with other tools such as Emacs Magit



## Configure GitHub page

### Core configuration

#### username and email

#### using obfuscated email address

#### Global Ignore file


### ssh keys

Add
provide a longish passphrase

TIP:  Use an actual phrase or a series of random words with spaces
TIP: store the passphrase in the keyring of the operating system, and have it unlock the key when you login



### Generate developer token
- for use with other tools
