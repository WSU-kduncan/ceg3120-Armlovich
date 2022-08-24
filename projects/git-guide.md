# Markdown guide
1. heading 	# H1
		## H2 ... etc
2. Bold            **bold text**
3. Italic		*italicized text*
4. Blockquote	> blockquote
5. Ordered List	1. first item
		2. Second item
6. Unordered List	- First item
7. Code		`code`
8. Link		[Links](https://www.example.com)
9. Image		![alt text](image.jpg)
10. Source Link	[Source for guide](https://www.markdownguide.org/cheat-sheet/)

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
		- vim .gitignore
			- list of anything you want to be ignored
7. push
	- pushes changes committed to github
	- git push
8. fetch
	- fetches the file from the remote (GitHub)
	- downloads the changes from the remote but doesn't merge it to your local
	- git fetch
9. merge
	- merges your fetched files into your local cloned repo
	- git merge
10. pull
	- pull is a combination of both fetch and merge
	- git pull
11. branch
	-
12. checkout

13. init

14. remote

### git files & folders
1. .gitfolder

2. .gitignore file
	- this is listed above and will be moved down here

3. .git/hooks

#### GitHub
1. pull requests

2. SSH authentication to repositories