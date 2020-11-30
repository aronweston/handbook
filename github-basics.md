## GitHub Basics

Many new developers get mixed up with the Git and Github confusion as if they are the either the same thing or completely separate. 

The best way to think about Github is to roll back to your understanding of how Git, the version control system, works. 

You make a change, add a file or delete something in your working directory (your saved file). You add these files to your staging directory through `$ git add .` or `$ git add *file.html*`. Then you commit them to you local repository. 

Your local repository is represented by the collection of hidden files in the `.git` file in your project directory. 

Github is a remote repository used to store your commit history and files on your local repository using cloud storage. Github itself doubles up as the Facebook for Developers where we can share projects we're working on and collaborate on different things. 

## The GitHub Flow

### 1. Forking 
Adds a copy of someones repo to your Github remote account. This is done by selecting the fork button on any public repo on Github. 

### 2. Cloning

Clone the repo to your local repository. This link can be found in the green code button in your forked repo. 

`$ git clone https://url-to-clone`

### 3. Editing/Adding/Committing

Make changes, additions etc in your local repo remembering to stage and commit any changes along with meaningful messages 


### 5. Pushing 

After you have made your changes to the cloned repo, you want to push them to your remote repo, your GitHub account. This is achieved through the: `git push origin master` command.

* `origin` is shorthand for the URL of your default remote repo. This can be many different URLs depending on the project. The origin can be set and unset. 

* `master` refers to the central `branch` of your repository. Branches are exactly what they sound like. Separate arms of the same tree of code that *branch* out and try new ideas. This is often used for feature testing. When you're happy with the finished product, you then `merge` this branch back with the `master` branch. 
    
Bear in mind, as of writing this, Github has moved to rename the default branch from `master` to `main` to remove unnecessary references to slavery for a more inclusive approach.


### 6. Pull request

As your local and remote repos are up-to-date on all your changes. It's time to see if the OG repo owner wants your code. 