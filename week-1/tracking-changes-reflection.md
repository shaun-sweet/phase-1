# How does tracking and adding changes make developers' lives easier?

Tracking and adding changes make developers' lives easier because it shows the process you took, and steps you did to the code. In addition, it allows you to work separtaely from the master version and compile all your changes before adding/sycning with the master version. This is good for reviewing your work before committing to changes, and allows us to see exactly what was done and when it was done. 


# What is a commit?

A commit is a save point in Git.


# What are the best practices for commit messages?

Since commits are save points, it is best practice to write good commmit messages. A good commit message would be a short, but specific and direct message saying what you did/changed in the files/code.


# What does the HEAD^ argument mean?

HEAD^ in Git refers to current commit you are on, which can be the current branch.


# What are the 3 stages of a git change and how do you move a file from one stage to the other?

Since it is not best practice to work directly from the master branch there are a few steps to take to make changes. For the first stage, on the master branch, do a git pull to get the changes. You would then create a new branch using `git checkout -b new_branch`. Then you would do your work on that branch you created. Once this is done, for the next stage, you would check your `git status` to see that changes have been made, and if you are satisfied with the changes you can do a `git add .` to add the files to commit. You would then `git commit -m "your message"`. Then, you would use the command "git push origin new_branch" to push your changes remotely. For the final stage, on GitHub, you would create a pull request to merge your branches. Once you follow the steps and merge on GitHub you can also delete this new_branch. Then back on the command line, you can swtich back to the master using `git checkout master` and use `git fetch origin master` to get the changes you made on GitHub remotely to your local machine, then finally `git merge origin/master` to merge, and you've made a change.


# Write a handy cheatsheet of the commands you need to commit your changes.

`git pull`

- Get most recent changes

`git checkout -b new_branch`

- Create and switch to a new branch

`git add`

- Set changes you've done to be committed

`git commit -v` *or* `git commit -m "message"`

- Open sublime to write a message for your commit or just write the message in the command line using the second option

`git push origin new_branch`

- Push changes to GitHub 

`git fetch origin master`

- Get changes you made on GitHub to your local machine

`git merge origin/master`

- Merge these changes with your master


# What is a pull request and how do you create and merge one?

A pull request is a way to merge branches. You would create a new separate branch to do your work on, add/commit and push those to GitHub. You would merge on GitHub remotely and then fetch/merge them to your local machine.


# Why are pull requests preferred when working with teams?

Pull requests are the preferred way when working with teams because then each developer can work on a separate piece of code without altering the master. When a developer is ready to send his code to the master, the code can first be reviewed, and we can see what exactly was done before we merge with the master. We can also finalize changes, and be sure we are ready to send to the master before actually committing these changes. As well, it allows us to track and version control changes, and see excatly when/where a change was made so if there is a bug we can go back to a previous iteration or commit.