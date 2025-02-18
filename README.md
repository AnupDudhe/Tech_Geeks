What is Git?
Git is a distributed version control system (VCS) that manages and tracks changes in their code over time. It allows multiple people to work on the same project simultaneously, 
with tools to merge their changes and resolve conflicts. Git keeps track of all changes made to a project, making it easy to revert to previous versions, collaborate with others,
and manage different branches of development.

Key features of Git include:
•	Version control: Keeps track of all changes made to files.
•	Branching: Developers can create different branches to work on new features without affecting the main codebase.
•	Merging: Combines changes from different branches back into the main codebase.
•	Distributed: Every user has a full copy of the repository, making it possible to work offline and still have access to the full history of changes.

Why is Git used?
Git is used for several important reasons, especially in software development and collaborative projects:
•	Version Control: Git tracks every change made to the codebase, allowing developers to see a complete history of modifications. This makes it easier to revert to previous versions if needed.
•	Collaboration: It enables multiple developers to work on the same project at the same time. Git manages changes from different people and merges them efficiently, preventing conflicts and
  ensuring that everyone is working on the most up-to-date version.
•	Branching and Merging: Developers can create branches to work on new features or bug fixes without affecting the main codebase (usually called master or main). Once their work is ready, 
  they can merge the changes back into the main branch.
•	Distributed System: Unlike centralized version control systems, Git is distributed, meaning each developer has a complete copy of the repository, including its history. This makes it faster,
  more reliable, and allows developers to work offline.
•	Backup and Recovery: Git helps prevent data loss by providing a local copy of the project’s history. In case of a problem, developers can recover the previous state of the project.
•	Code Review and Collaboration Tools: Platforms like GitHub, GitLab, and Bitbucket allow developers to host their Git repositories and provide features like pull requests, issue tracking, 
  and code reviews, which improve the development process.
•	Efficiency and Performance: Git is fast, especially when it comes to handling large projects. Operations like commits, branches, and merges are optimized to be quick, even with a large amount of history.

How Does Git Work?
Git is a distributed version control system that tracks changes in files and allows multiple developers to collaborate on the same project. It works by maintaining a local repository on each user's 
machine, which contains the entire project history, and a remote repository where code is shared. Git helps in managing different versions of the code, enabling users to create branches for new features
or fixes without affecting the main codebase. Changes are tracked through commits, and developers can merge their work back into the main branch once completed.
The workflow in Git typically involves modifying files in the working directory, staging those changes with git add, and then committing them to the repository with git commit.
Developers can push their changes to a remote repository using git push and pull updates from others using git pull. Git's branching and merging capabilities allow for efficient collaboration,
even when multiple developers are working on different features or fixes simultaneously. This ensures that the project remains organized, and changes are systematically integrated.

#git commands :
yum install git -y	-> by default you don't get git installed in RHEL AWS linux therefore you need to install it by using this command.

git init	-> initializes .git file in a specific folder or repository.

git status	-> displays the state of your working directory, showing which files have been modified, staged or untraced.

git add .	-> stages files in you working directory, preparing them for inclusion in next commit.

git commit -m "commit"	-> saves changes from the working directory into a local repository making it ready to push to a remote repository.

git log	-> displays the commit history of git repsitory.

#git rollback commands :
git revert	-> Creates a new commit that undoes the changes made in a previous commit. This is a safe way to undo changes, as it doesn't alter the commit history.
    git revert <commit-hash>

git rebase	-> Reapplies commits on top of another base commit. It's often used to integrate changes from one branch into another or to clean up the commit history.
	git rebase <base-branch>
	
git reset	-> Resets the current branch to a specified commit, potentially discarding commits made after that point. It has different modes that affect the working directory
			   and staging area. (Works at the Commit Level)
    git reset --soft <commit-hash> # Keeps changes in staging area
    git reset --mixed <commit-hash> # Keeps changes in working directory
    git reset --hard <commit-hash> # Discards changes
	
git restore	-> Restores files in the working tree from either the staging area or another commit, and does not update your branch. It can be used to unstage or discard 
			   uncommitted local changes. (Works at the File Level)
    git restore --staged <file> # Unstage file
    git restore <file> # Discard local changes

#git commands :
git pull	-> syncs or copies changes from a remote repository directly into your working directory.

git fetch	-> Just downloads updates, no changes to your local branch.

git remote	-> manages connections to remote repositories. It allows you to add, view, rename, or remove remotes.

git clone <repourl>	-> copies an existing repository from a remote server to your local computer.

git branch	-> states current branches in repository.

git branch dev1	-> creates a branch other than main.

git checkout dev1	-> moves from current branch to created/another.

git push -u origin dev1	-> pushes your local dev1 branch to the remote repository named origin.
		or
git push-u <sshurl> dev1

*******************************************************************************************************************
//	Why Is GitHub Rejecting Your Password?																		                                    *
//	GitHub removed password authentication for Git operations over HTTPS on August 13, 2021. You now need to use: *
//	1. A Personal Access Token (PAT) instead of your password 													                          *
//						or																						                                                      *
//	2. SSH Authentication for secure access.																	                                    *
*******************************************************************************************************************

git diff main dev1	-> gives diffrence between two branches.

git merge dev1	-> merges devl data into main or current branch to merge first be in the branch You want to merge data into.
