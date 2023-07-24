# Reference: Git Clone

clone a repository from another location, typically a shared Git service (GitHub, GitLab, etc.)

```shell
git clone --origin practicalli repository-url local-directory
```

`--branch` option will checkout a specific branch name once cloned.

[Clone - Git reference](https://www.git-scm.com/docs/git-clone){target=_blank .md-button}


## Managing Clone size

Continuous Integration workflows can be more effective when cloning a small part of the repository.


### Partial Clone

`--filter option` is used to clone a partial repository.

`git rev-list --filter=<filter> --all` shows objects in your repository that match the filter. 

```shell title="Blobless clone"
git clone --filter=blob:none <url>
```

Blobless clone downloads all reachable commits and trees, fetching blobs on-demand. 

**Use case**: developers and build environments that span multiple builds.


```shell title="Treeless clone"
git clone --filter=tree:0 <url>
```
treeless clone download all reachable commits, fetching trees and blobs on-demand. 

**Use case**: build environments where the repository will be deleted after a single build, where access to commit history is required


### Shallow Clone

A shallow clone truncate the commit history, only fetching after the specified time.

```shell
git clone --shallow-since=<date>
```

**Use case**: build environments where the repository will be deleted after a single build.

Shallow clones are discouraged for development as they limit git commands and may put undue stress on later fetches 

!!! WARNING "Partial Clones are typically recommended over shallow clones"



[Get up to speed with partial clone and shallow clone](https://github.blog/2020-12-21-get-up-to-speed-with-partial-clone-and-shallow-clone/){target=_blank .md-button}
