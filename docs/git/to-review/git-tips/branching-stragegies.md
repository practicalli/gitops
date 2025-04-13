title: Branching Stragegies
---

Previously we discussed what a branch is in Git, how they are created and how to switch between branches.  Now we will discuss different approaches to using branches, from the very simple to the complex.

## Local Branches only Strategy

Branches created locally.  Any changes to be shared are merged into the master branch first then that master branch is pushed to a common repository.

### Advantages
* Very simple to use.
* Only 1 branch to keep in sync with everyone else.

### Limitations


## Github Pull Model

Branches created locally.  Any changes to be shared are merged into the master branch first then that master branch is pushed to a common repository.

### Advantages
* Quite simple to use.
* Can work with multiple shared branches
* Provides easy way to review, discuss and document changes

### Limitations
* Requires a services such as Github that supports pull requests


## Git Flow

...

### Advantages
* It makes you learn git really well 
* It can help with larger teams

### Limitations
* It may be overkill
* Learning curve for adoption, not to be rushed into
* Need to ensure everyone understands the flow, human error easily introduced
* Relying on tools to manage the flow can mean problems harder to fix if something goes wrong, as people may not understand the flow enough.



See the [Git Flow section](git-flow.html) for more details.
