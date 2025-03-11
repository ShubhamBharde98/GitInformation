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
``` bash
    git config --global user.email <"email id">
    git config --global user.name <"name">
    git config --global --edit
```

### Can I Set Config for Only One Project?
Yes! If you don’t want to set your username and email globally, you can configure them only for a specific repository:

``` bash 
    git config --local user.email "project-email@example.com"
    
    git config --local user.name "Project Name"
```
- This setting applies only inside that repository.

- Useful when working on multiple projects with different GitHub accounts


## Git Commands:-
1. git init
1. git add < file name > OR git add .
1. git commit -m <"message">
1. git push -u origin < branch name > OR git push


1. git clone < httpsLink >
1. git remote add origin < httpsLink >

1. git status
1. git log
1. git remote -v
1. git branch


1. git branch -M < branch name >
1. git checkout < branch name >

1. git commit --amend -m <"new message">

1. git rm --cached < file name >
1. git rm -rf .git/

## Git Authentication methods:-
Git supports multiple authentication methods:

1. HTTPS with Username & Password (Deprecated)
1. HTTPS with Personal Access Token (PAT) ✅ (easy)
1. SSH Authentication ✅ (Recommended & hard)
1. Credential Helper (for HTTPS) ✅ (very easy)
1. GPG Signing for Secure Authentication

## Detail steps for Git Authentication Methods:-
### 1] OAuth authentication via Git Credential Manager(GCM) OR Credential Helper (for HTTPS) ✅:-

#### What Happens in This Step?
- Git detects that authentication is needed for pushing to GitHub.
- Instead of asking for a username & password, it opens a browser window.
- You log in to GitHub, and GitHub grants OAuth access to your local Git client.
- Git Credential Manager (GCM) securely stores the authentication token.
- Your push operation automatically succeeds without needing manual authentication again.

#### Why Is This Easier?
- No need to remember/store Personal Access Tokens (PATs).
- No need to set up SSH keys.
- Works seamlessly across Windows, macOS, and Linux.

#### What is Handling This?
- Git Credential Manager (GCM) is handling the authentication.
- GCM supports OAuth authentication and securely stores credentials (Windows Credential Manager, macOS Keychain, or Linux Secret Service).

### 2] PAT (Personal Access Token):-
- GitHub and GitLab no longer support username/password authentication over HTTPS. Instead, they require a Personal Access Token (PAT).

- Generate a Personal Access Token (PAT)
    - For GitHub: Go to GitHub Tokens → Generate a new token.

- Git will prompt for a username. Enter your GitHub/GitLab username and use the PAT as the password.

- Save Credentials (Optional)
``` bash 
git config --global credential.helper store
```

### 3] SSH Authentication (Recommended) ✅:-
``` bash 
ssh-keygen –t ed25519 –C <”email id”>
OR
ssh-keygen –t rsa –b 4096 –C <”email id”> 
```

- enter file name in that we getting key 
    - e.g.:- < projectNameKey >
-  done!!! You will get <“projectNameKey.pub”> file

- ls –la
- cat <”projectNameKey.pub”> // read that file and print content of key

- copy that key & go to github accout page 
- in github accout page go to setting ==> click on SSH keys
- then hit the New SSH Key button
- enter Title field as “< projectNameKey >”
- & enter Key field as “< paste key which is you already copied >” & hit on Add SSH key button.
- Done!!!


## Errors which is i gotted & How i tackled.
### Error 1:-
#### remote: Permission to ShubhamBharde98/GitInformation.git denied to ShubhamBharde.
#### fatal: unable to access 'https://github.com/ShubhamBharde98/GitInformation.git/': The requested URL returned error: 403 

### Error 1 Solution:-
1. open control panel ==> search & open credential manager
1. click on Windows Credentials
1. remove the previous git credential
1. done!!! 


## Basic Git Workflow:-
### Step 1:- Create or Modify files 
- Modify or create a file in the working directory.

### Step 2:- Stage Changes
- Use ```git add <file_name>``` or ```git add . ``` to move files to the staging area.

- This marks changes as ready for commit.

### Step 3:- Commit Changes 
- Execute ```git commit -m "<descriptive_message>" ```to save changes to the local repository.

- Commits serve as snapshots of the project.

### Step 4:- Push Changes to Remote Repository 
- Use ```git push -u origin <branch_name> ``` to upload changes.

- Ensures version control across distributed environments.


## Git Components:-
### Local Repository:-
- A version-controlled directory on a local machine.

- Stores committed changes and allows local development.

### Remote Repository:-
- A centralized repository hosted on a remote server (e.g., GitHub, GitLab).

- Facilitates collaboration by enabling multiple contributors.

### Working Directory:-
- The current state of files in a project.

- Reflects untracked, modified, or staged changes.

### Staging Area (Index):-
- A temporary storage area where changes are prepared before committing.

- Ensures only selected modifications are committed.

### Push:-
- Sends committed changes from the local repository to the remote repository.

- May require authentication and branch specification.

### Pull:-
- Retrieves updates from a remote repository and integrates them into the local branch.

- Equivalent to ```git fetch ``` followed by ```git merge ```.


## Blob (Binary Large Object):-
Blob stands for Binary Large Object.

- Represents the content of a file as a unique SHA-1 hash.

- Stores file data but excludes metadata (e.g., filename, permissions).

- Git relies on content-based addressing rather than file names.

## Tree Object:-
- Represents a directory structure in Git.

- Stores references to blobs (files) and other trees (subdirectories).

- Facilitates efficient version tracking and branching mechanisms.


