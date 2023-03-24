# Git Config

Configure Git page

## Core configuration

Configure your Git identity

```shell title="Configure Git Identity"
git config --global user.email=obfuscated-name@github.com
git config -- global user.name="Practicalli John"
```

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
