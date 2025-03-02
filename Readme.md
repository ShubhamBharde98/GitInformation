# Git & Github Information  
## Git:-
git is Version Control System (VCS).

git was created by Linus Torvalds in the year of 2005.

git is free & open source & scalable & super fast & efficient.

## Version Control System:-
It is a system that keeps track of our files, tracking any changes in our code, manage versions & their rollback (means anytime you can revert the previous version).

It allows us collaboration among multiple developers.

### Types of Version Control System:-
1. Centralized Version Control System :-
    - ex:- svn 
    - limited offline support requires a connection to commit, require server access for collaboration 
    - Stores full file copies 
    - Slower depends on server & Larger Repository Size

1. Distributed Version Control System:- 
    - ex:- git, mercurial
    - gives offline support, easily collaboration among multiple devlopers
    - Stores differences
    - Faster & Smaller Repository Size

## Why do we need of git?
1. tracking multiple files or any changes in our code.

1. managing different versions. 

1. rollback support (we can easily revert the previous version). 

1. Collaboration purpose also we can use. Multiple developers can work on the same project simultaneously without overwriting each other's work.

1. Branching & Merging:- Work on different features separately and merge them later.


## Github:-
github is a cloud-based platform for hosting and managing Git repositories. 

It provides a user-friendly interface to work with Git, enabling developers to collaborate, track changes, and manage projects efficiently.

## Git vs Github:-
1. Git:-
    <b> git is a distributed version control system which is tracking changes in our code </b>
    - Manages versions, branches, and commits locally.
    - Local storage (on your computer)
    - works offline (local repository)
    - Can be used alone or in a team via shared repositories.
    - No built-in access control.
    - Can be integrated manually


1. Github:-
    <b> GitHub is a cloud-based platform for hosting and managing Git repositories. </b>
    - Provides a remote Git repository with additional collaboration tools.
    - Cloud-based storage (accessible from anywhere)
    - Requires internet for syncing with remote repositories.
    - Designed for team collaboration, code reviews, and issue tracking.
    - Provides private repositories, access control, and role-based permissions.
    - Supports GitHub Actions for automation, CI/CD, and testing.

#### Note:- You can use git without github, but you can't use github without git. 

## git setup configuration:-
    git config --global user.email <"email id">
    git config --global user.name <"name">
    git config --global --edit

### Can I Set Config for Only One Project?
Yes! If you don’t want to set your username and email globally, you can configure them only for a specific repository:

``` bash 
    git config --local user.email "project-email@example.com"
    
    git config --local user.name "Project Name"
```
- This setting applies only inside that repository.

- Useful when working on multiple projects with different GitHub accounts
