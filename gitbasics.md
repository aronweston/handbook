## Git Basics

### Check git version
`$ git version` 

### Intialise git in your project directory

```
$ cd desktop
$ mkdir project
$ cd project
$ git init
```

### Check the status of the git local repository. 

This will show any and all file changes, deletions and updates made since last commit. These files are present in your working directory with status telling you if they have been deleted, modified or created.

`$ git status`

### Add files to your staging directory.  

By adding your files from your working directory into your staging directory, your updates and deletions to be saved ready to be committed to your local repository, and pushed to your remote repo in your next commit. 

`$ git add *insertfilename*`

To add all of the changes, use the `$ git add .` command. However, be careful not commit files and changes that contain sensitive information like API keys. These files should be added to a `.gitignore` file. Enter in the file names such as `config.js` or directories like `/assets` to hide them from all future commits. 

Often when creating a new project, there are multiple hidden files such as `.DS_Store` that are committed to projects, when they do not need to be. As a general rule, unless you are constantly changing and need a *version* of it (since it is version control), do not commit it.

An example of this is the common beginner mistake of committing `node_modules` or `asset` directories that contain common modules or multiple megabits of data that should only exist on your local repository machine. 


### Commit files from the staging directory to your local directory

Commit your additions, changes and deletions from the staging area to the local repository. Be sure to make your messages meaningful and describe what and why you have done things that way. You may have to roll back changes to these checkpoints, so be as descriptive as possible. [This is a good resource](https://www.freecodecamp.org/news/writing-good-commit-messages-a-practical-guide/)

`$ git commit -m "#2: Working app; added index.html file; ui click events are still buggy; form submits successfully"`

* Use the `-a` flag to commit all new and tracked files to the local repo.

`$ git commit -a -m "#3: Small bug fixes on index.js"`

* Check the commit history. This will give you a list of the past commits, the time, username, ID, branch and your meaningful and well thoughtout messages.

`$ git log`


### Pushing to a remote repo

The last piece in the jigsaw. After you've made all your changes on your local repo, you're going to what to let your dev friends know about your sick Weather App. So you can then push your code to GitHub with a few commands.


## 1. Add and commit 
`git add .`
`git commit -m "meaningful commit messages"`

## 2. Rename your master branch to main.

This is inline with Githubs recent changes to community guidelines as the `master` branch is now refered to [as the `main` branch](https://github.com/github/renaming)

`git branch -M main`

## 3. Add a remote origin

This is where you tell your repo where its going. This is generally done through HTTPS in which case you'll have to ensure that you have set your username and email through `git config`.

git remote add origin https://github.com/username/yourepo.git

## 3. Add a remote origin

This command pushes your code on your local repo to your remote repo set at the `origin` you have created, and set to your default branch, `main`. The `-u` flag gives the specific commit a reference for that commit. [Link](https://git-scm.com/docs/git-push#Documentation/git-push.txt--u)

`git push -u origin main` 

All commits after this initial set up just require `git push` after your commit, unless you change your `origin`. 






