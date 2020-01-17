# Overview
- Introduction to Git
- Git as Version Control
- Question Time 1
- Git to Collaborate
- Question Time 2
- Resources
- References

# Introduction to Git
## What is Git?
Git is a version control system often used to keep track of changes in source code and to collaborate with other programmers.
Though source code is not the only use for Git as it can be extended to other text-based file formats like this.
An example would be using Git for amendments to The U.S. Constitution: github.com/JesseKPhillips/USA-Constitution.

![Priorities of Software Development](https://i.imgur.com/IiAdxbB.png)

## What is Git Used For?
Git has many different use cases, some of the most common uses are:
- Revision history
- Collaborating with other developers
- Backup code and important files
- Distributed development
- Organization of code
- Tracking incomplete code
- Tracking different versions of code

#  Git as Version Control
## Snapshots
A _snapshot_ can be compared to a backup or "picture" of your code at any given point in time.
Git creates and maintains a history of your code using these snapshots.
For example, given a software repository, if a user creates a file, Git will take a snapshot for the repository history of when the file is created.
Then when the file is modified, Git will take a snapshot afterwards, storing the repository state after the file is modified.
Importantly, Git still has the snapshot from after the file was created and before it was modified, available to fall back on if the modifications (or deletion!) is undesirable.

## Staging Area
Git allows users to selectively add files to snapshot by using something called the \textit{staging area}.

For example, if we create two files, _a.txt_ and _b.txt_, but _a.txt_ is used for temporary configuration and we don't want Git to take a snapshot of it, we can add _b.txt_ to the staging area and then when we take the snapshot _b.txt_ will be in the snapshot but not _a.txt_.

## Workflow Overview
- _git add_: Move specified file(s) to the staging area
- _git commit_: Create a snapshot of the staging area
- _git push_: Push local history (i.e. snapshots) to remote history
- _git pull_: Pull remote history into local history
- _git checkout_: Switch to another branch
- _git merge_: Merge another branch's snapshots into the current branch

![A Common Git Workflow](https://www.edureka.co/blog/wp-content/uploads/2016/11/Git-Architechture-Git-Tutorial-Edureka-2.png)

## Walkthrough
We will demonstrate some of these ideas by first creating a repository on GitHub.
We will then use GitHub Desktop to _git add_ a file to put it into the staging area, marking it as something we would like to track with Git.
Note: if the file were erased or changed at this moment, there would be no snapshots or history to undo those changes.

This is where we _git commit_ and tell Git to take a snapshot of our file at the stage when we ran _git add_.
This means if we modified the file after doing _git add_, those changes aren't in the staging area so we would need to run _git add_ again.

Committing files requires a message summarizing the changes.
There are many standards people use for commit messages but I personally try to use language that describes the action that I did when modifying files.
For example, here I would use `Add hello.py'.
Once we commit, we can see that the file is being tracked by Git.

## Branches
Branches in Git represent different paths of development.
The default branch used is **master**.
Branches are useful in real world scenarios where the code needs to be deployable/runnable at any point in time but we want to make changes like adding a feature, rewriting part of the code base, and experimenting with different ideas.

For example, if we had code to convert a data set from _csv_ to _json_, we may need to run this program at any point if new data comes in.
However, if we want to add functionality to convert to another data format, we may need to rewrite and `break' the existing code.

![An Example Branch Diagram](https://git-scm.com/book/en/v2/images/basic-branching-4.png)

# Question Time 1
Any questions about using Git as version control?

# Git to Collaborate
## Pushing and Pulling
We have covered making commits, but up until now, we have only made commits and changes in our local repository.
If we wanted to send these changes to GitHub, where others could see it (including ourselves from a different machine for example), we need to _git push_.

Luckily, GitHub Desktop makes that easy for us and will notify us of any unpushed commits.
Now we can go to GitHub and see the commits (snapshots) and could potentially clone this repository to another folder, computer, etc..

We will do exactly this to help demonstrate _git clone_ again but also to demonstrate _git pull_, where we pull changes another person made (or us from another location) from the remote repository into our own local repository.

## Pull Requests
One of the features that GitHub provides for collaborating is something called _Pull Requests_.
A pull request has many uses, but some of the most important uses are to provide a place to communicate regarding a branch of development and document discussions about the branch and, most of the time, the eventual merge of the code from the branch into the branch where it split from.
We can demonstrate this in GitHub with a simple branch.

# Question Time 2
Any questions about using Git to collaborate?

# Resources
- https://guides.github.com/activities/hello-world/
- https://guides.github.com/introduction/git-handbook/
- https://github.github.com/training-kit/

# References
- In Case of Fire image: https://i.imgur.com/IiAdxbB.png
- Git Workflow image: https://www.edureka.co/blog/wp-content/uploads/2016/11/Git-Architechture-Git-Tutorial-Edureka-2.png
- Git Branches image: https://git-scm.com/book/en/v2/images/basic-branching-4.png
