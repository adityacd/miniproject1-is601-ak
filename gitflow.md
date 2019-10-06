## Understanding the Gitflow


1. Repository
* A repository is like a folder for your project.
* Your project's repository contains all of your project's files and stores each file's revision history.
* You can also discuss and manage your project's work within the repository.

This is how a Github Repository looks like.
![repo](https://user-images.githubusercontent.com/37020817/66275082-227c1e80-e853-11e9-8448-33d31e8d03fe.png)

Further in this guide you can see how to completely use and manage a Github repository.

2. Clone
* Clone is primarily used to point to an existing repo and make a clone or copy of that repo at in a new directory, at another location.
* The original repository can be located on the local filesystem or on remote machine accessible supported protocols.

When you enter the following coommand, the **clone** of the local repo is created.
```
$ git clone <repo-URL>
```
Here the **local repository** is on left side and **remote repository** is on right side. 
![Clone](https://user-images.githubusercontent.com/37020817/66275192-40964e80-e854-11e9-8d4f-2e3d07cf09d6.png)

* You can use both **SSH and HTTP** link to clone a repo.

3. Fork  
* It is used to access the contents of the owner repository.



4. Branch
* A branch is a reference to a commit. 
* The branch represents the top of a series of commits.
![github branch](/Downloads/Branch-1)

we can create a branch by 
```
git branch <branch-name>
```

5. Commit

* It captures the snapshot of the currently made changes in git. 

6. Merge
* It is used to merge the work from different branches to the master branch. 
* Merging updates the commits (or changes) that are made from one branch to another. 
```
$ git merge
```
* Here you can see the **Feature Branch**(green) is merged with **Master Branch**(sky blue).
* This merging is also commited.

![Merge](https://user-images.githubusercontent.com/37020817/66276367-5873cf80-e860-11e9-8992-3513d9401a88.png)

The command will be
```
$ git merge Feature
```
7. Checkout
* Th


8. Push
* The git push command is used to upload local repository content to a remote repository.
* Pushing is how you transfer commits from local to remote repo.
```
$ git push
```
![pushpull](https://user-images.githubusercontent.com/37020817/66275636-9f5dc700-e858-11e9-8c0a-fa71f4e7a52b.jpg)
```
$ git push origin
```
* git push origin works the same as that of git push (without parameter).
* Here, we are assuming that you have named your remote repository as origin.
```
$ git push origin branch-name
```
* Push your branch-name branch only to remote repository named as origin.
* Here, we explicitly define name of a single branch to push.

9. Pull
* The git pull command is used to fetch and download content from a remote repository.
* It immediately updates the local repository to match that content.

```
$ git pull
```

The below command is used to pull changes from the origin remote, master branch and merge them to the local checked-out branch.
```
$ git pull origin master
```

10. Remote Add/Remove/Show
* The git remote command lets you create, view, and delete connections to other repositories.
* Remote connections are more like bookmarks rather than direct links into other repositories.
The following are some commands of remote.

List the remote connections you have to the  other repositories.
```
$ git remote
origin
```
Here just include the URL of the connection.
```
$ git remote -v
```
After adding a remote, you’ll be able to use <name> as a convenient shortcut for <url> in other Git commands.
```
$ git remote add <name> <url>
```
To remove remove the connection to the remote repository just do the following.
```
$ git remote rm <name>
```
To rename a file use the following command <old-name> changes to <new-name>.
```
$ git remote rename <old-name> <new-name>
```
11. Status
* The git status command displays the state of the working directory and the staging area.
* It lets you see which changes have been staged, which haven’t, and which files aren’t being tracked by Git.

Here you can see the status command tells which files should be added and which should be modified.
```
$ git status
On branch aditya
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   gitflow.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        images/

On branch aditya
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   gitflow.md

```

12. Master Branch
* A branch in Git is simply a lightweight movable pointer to one of the commits.
* The default branch name in Git is **master**.
* As you start making commits, you're given a master branch that points to the last commit you made.
* Every time you commit, the master branch pointer moves forward automatically.

![Branch](https://user-images.githubusercontent.com/37020817/66276352-22365000-e860-11e9-97ea-dea43e14497e.png)
