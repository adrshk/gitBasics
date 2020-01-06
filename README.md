# gitBasics
Git commands(Pull, Commit, Push, Stash, Branch, Tags, Rename, Log, Merge)

# Basic Commands

- git init : turns a directory into an empty Git repository. This is the first step in creating a repository. After running git init, adding and committing files/directories is possible. 
- git config : configurations and settings
- git status : This command returns the current state of the repository.
- git add <file or directory name> : Adds files in the to the staging area for Git
- git commit -m "Commit message in quotes" : Record the changes made to the files to a local repository. For easy reference, each commit has a unique ID.
- git checkout <sha1> : to check out a particular commit.

=========================================================================================

# Remote Repositories

- git remote <command> <remote_name> <remote_URL> : Add remote repository
- git remote -v : List named remote repositories
- git clone <remote_URL> :create a local working copy of an existing remote repository
- git pull : get the latest version of a repository run git pull
- git push  : Sends local commits to the remote repository.  

=========================================================================================

# Branching 

- git branch <branch-name> : creates a new branch
- git checkout <branch-name> : checks-out the HEAD commit for the given branch
  	-b : creates a branch first if it doesn’t exist before checking it out.
- git branch : shows a list of all existing branches in the project and indicates the current branch with an asterisk (*).
- git push -d origin(remote_name) <branch_name> : deletes an existing branch in the remote repo, should be executed before deleting the branch locally
- git branch -d <branch_name> : checks if a branch is merged with master and if it is, deletes it locally, else gives a warning message.
- git branch -D <branch_name> : force deletes a branch locally
- git merge <branch_name> : Integrate branches together.
  
=========================================================================================

# Stash

- git stash -u : Store current work with untracked files
- git stash pop : Bring stashed work back to the working directory
- git stash drop : delete all the stash list
- git stash drop stash@{n} :  This will drop the specific  saved stash.
- git stash save “name” : Save a stash using name
- git stash list : This will list down all your stashes.
- git stash pop stash@{n} : To apply a stash and remove it from the stash stack
- git stash apply stash@{n} : To apply a stash and keep it in the stash stack

~ Where n in the index of the stashed change.

=========================================================================================

# Merging 

 (Merging <branch-name>  into master : run the following one by one)
- git checkout master: check out the master so that you can merge the branch into the master
- git merge <branch-name> : this will merge the branch in the master. You need to resolve the conflict manually.
 (Merging  master into <branch-name> : run the following one by one)
- git checkout <branch-name> :  checkout the branch in which you want master branch to be merged.
- git merge master :  This will merge master into the current working branch. You need to resole the conflict manually.   

~ Make a commit of conflict resolution

=========================================================================================

# Rename (run the following one by one)

1. git branch -m old_branch new_branch : Rename branch locally    
2. git push origin :old_branch : Delete the old branch    
3. git push --set-upstream origin new_branch : Push the new branch, set local branch to track the new remote

=========================================================================================

# log

- git log : Show entire git log
- git log --<after/before/since/until>=<date> : Show git log with date parameters
- git log --<author>="Author Name" : Show git log based on commit author



