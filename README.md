# A03
IS 117-101 A03

Important Commands to Know
--------------------------------
+ $ git init -- initialize
+ $ git status -- see unstaged and staged files
+ $ git add -- add to repository
+ $ git add -A -- add everything to staging area
+ $ git reset -- remove files from staging area
+ $ git commit -m "commit message here" -- commit to branch
+ $ cd  -- change directory
+ $ cd .. -- previous directory
+ $ ls -- what's in directory
+ $ ls -la -- all info about directory
+ $ touch .gitignore -- ignore files (for files with sensitive info)
+ $ git log -- see commit just made

Set Up a New Repository Locally
---------------------------------
1. Create repository on GitHub
2. Configure your credentials: 
	* $ git config --global user.email "email@address.com"
	* $ git config --global user.name "Your Name"
4. Go to folder with desired projects: $ cd ./file_path/
5. Initialize git repository: $ git init
6. Link GitHub repository to local directory: 
	$ git remote add origin <repository URL>
7. Check if repository successfully linked:
	$ git remote -v
8. Add all files to staging area. Replace dot with filename to add specific files: 
	$ git add . 
9. Check staging area: $ git status
	To unstage a file: $ git rm --cached file_name 
10. Commit any changes to master branch: 
	$ git commit -m "COMMIT MESSAGE"
11. Push changes to master branch: $ git push origin master

Track an Existing Remote Repository
-------------------------------------
1. Clone an existing repository:
	* $ git clone <repository URL> <WHERE U WANT TO CLONE>
	* e.g. $ git clone ../remote_repo.git .
		* $ git clone https://github.com/stval98/A03
2. List all repository information: $ git remote -v 
3. List all branches in repository (local and remote): $ git branch -a 

Push Changes to a Remote Repository
-------------------------------------
1. Show changes made to files: $ git diff
2. Check staging area: $ git status
3. Add files to staging area: $ git add -A
4. Check changes made to staging area: $ git status
5. Commit changes to master branch: $ git commit -m "changes made"
4. Pull changes from master branch: $ git pull origin master
5. Push changes to master branch: $ git push origin master 

Create a New Branch
-----------------------
1. Create branch: $ git branch BRANCH_NAME
2. Switch to branch: $ git checkout BRANCH_NAME 
3. List local branches: $ git branch

Push Local Branch to Remote Repository
-----------------------------------------
1. Push branch to remote repository: $ git push -u origin BRANCH_NAME 
2. List all branches: $ git branch -a
3. Pull changes from branch: $ git pull
4. Push changes to branch: $ git push

Merge a Branch to Master Branch
--------------------------------
1. Check out master branch: $ git checkout master 
2. Pull changes from master branch: $ git pull origin master
3. List branches merged in so far: $ git branch --merged 
4. Merge to master branch: $ git merge BRANCH_NAME
5. Push to master branch in remote repository: $ git push origin master

Delete a Local Branch
----------------------
1. List branches merged in so far: $ git branch --merged
2. Delete branch locally: $ git branch -d BRANCH_NAME
3. List all branches: $ git branch -a
4. Delete remote branch: $ git push origin --delete BRANCH_NAME

Solve a Merge Conflict
----------------------
1. Pull changes from master branch: $ git pull origin master
2. Check staging area to see file affected: $ git status
3. Inspect file to find conflict. Search for <<<<<<< HEAD conflict marker.
4. Make necessary changes to resolve the conflict. 
5. Commit changes: $ git commit -m "changes made"
6. Push changes to branch: $ git push
	
	
Additional References:
----------------------
+ https://rogerdudler.github.io/git-guide/
