# Markdown guide
1.  heading 	# H1, ## H2 ... etc
2.  Bold :           	**bold text**
3.  Italic :		*italicized text*
4.  Blockquote :	> blockquote
5.  Ordered List :	
	1. first item
	2. Second item
6.  Unordered List : - (item; see below)	
	- First item
7.  Code :		`code`
8.  Link :		[Links](https://www.example.com)
9.  Image :		![alt text](image.jpg)
	1. first, you will need to upload the image to GitHub via the website
	2. second, pull the changes from your repo to your local
	3. third, either, mv (move) or cp (copy) the image to a folder you want to contain the images,
	4. then, use the absolute path to the image jpg, or the relative path **(only if in the same folder as your code)** in the parenthesis shown above as *(image.jpg)*
10. Source Link :	[Source for guide](https://www.markdownguide.org/cheat-sheet/)
11. Crossing out: 	~~crossed out~~

## command line git:
1. status
	- shows the status of local repository. This includes:
		- number of local commits that have not been synced with remote (GitHub)
		- list of files in local folder that are NOT being tracked by git
		- list of files in local folder that have changes that need to be committed
	- command: git status
2. clone
	- clones the repo from the remote (GitHub)
		- if you clone the repo from the remote while already having a clone of the repo
		- you will recursively overwrite the current clone. 
		- this will cause you to lose everything not already pushed to the remote repo
	- git clone "repo-name@github.com"
3. add
	- adds files that need to be added for tracking
		- this adds files to be tracked, but doesn't commit the files for pushing to the remote
		- multiple files can be added at once
		- just put a (space) between the files you wish to add
	- git add (replace-with-file name)
4. rm
	- removes files from your local system
		- this does not remove files from the remote. not until you add, commit, and push the changes
	- rm (filename-without-the-parenthyses)
5. commit
	- commits files that have been added for tracking
		- this still does not actually add the files to the remote
	- git commit 
		- this can be shortcutted by using *git commit -m "commit message"
6. .gitignore
	- a file that contains things that you want ignored via git status
	
	- command: vim .gitignore
		- list of anything you want to be ignored

6. push
	- pushes changes committed to github
	- git push

7. fetch
	- fetches the file from the remote (GitHub)
	- downloads the changes from the remote but doesn't merge it to your local
	- git fetch

8. merge
	- merges your fetched files into your local cloned repo
	- git merge

9. pull
	- pull is a combination of both fetch and merge
	- git pull

10. branch
	- creates a new location where changes can be made to a core program without affecting the main program.
		- each branch can have changes made, then returned to the Main branch.
		- this allows the Main to remain a working program.
	- git branch (name)
	
	- git checkout (branch name) to change branches
	
11. checkout
	- changes your working branch from your current branch to another branch.
	- git checkout (branch name) 	

12. init

13. remote

### git files & folders

1. .git folder
	- this folder contains all the information necessary for commits, remote repository addresses and other things relating to your GitHub account.
	- this log can help you roll back to a previous commit or change if necessary 


2. .gitignore file
	- a file that contains things that you want ignored via git status
	- list of anything you want to be ignored by the `git status` command.
	- vim .gitignore

3. .git/hooks
	- 

#### GitHub
1. pull requests
	- sets up requests for a group to look over the content stored on a branch and decide whether or not it is up to par
	- this request can be approved, permanently denied, or denied until further changes are made.

2. SSH authentication to repositories
	- go to settings on GitHub and prepare for pasting in a public key,
	- on ubuntu, use the command : ssh-keygen -t ed25519 ; to generate a new SSH key pair
	- cd into the .ssh folder, then vim the content of ed25519.pub file.
	- copy the file into the field on the GitHub settings tab for a new ssh key.
	- save and enjoy your ability to ssh into your repos from the computer with the private key
	- or save the key onto a thumbdrive and transfer it from computer to computer (not safe)
		- a better way would be to use the ssh-keygen command to set up new key-pairs on each new computer

3. git rm --cached
	- removes changes, specifically files and folders, from git tracking. 
	- the file still exists, it just won't be on github for everyone to see.
	- still have to git commit
