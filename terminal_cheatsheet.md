# Terminal Cheatsheet
## Basic Commands
- {CMD !}
	- increase window and font size
	
- {CMD -}
	- decrease font size

- {CONTROL  L}
	- Clears what's on the screen and moves command line to the top to be easier to read.
	- Does not delete previous stuff, just moves it out of sight

- Line up/down
	- {OPTION CMD UP/DOWN ARROW}
	
- pwd
	- put in command line, press return
	- tells you where you are, what directory and folder
	
- ls
	- lists files and folders. If you installed oh-my-zsh, folders will be in blue, files in white

- ls -l
	- lists files and folders along with permissions, owner, and date last modified
	
- ls -al
	- Shows hidden files as well as other files and folders

- cd Documents
	- cd = Change Directory.
	- Use cd and folder name to move into anywhere in the file system
	- cd by itself takes you back to the home directory

- cd D {TAB KEY}
	- Shows options under the letter D, to see spelling
	- Keep hitting tab key to highlight one the folders, then hit enter to select the folder, and enter
	-  again to go into the folder

- {TAB KEY}
	- Works as auto-complete shortcut. Very useful
		- e.g. cd Doc{TAB KEY to autofill to Documents}/ {TAB KEY to show file options}{TAB KEY to move between files}

- cd ..
	- Moves one level up in the directory, e.g. moving from Documents to User Folder to Home to Root.

- mkdir
	- Creates a folder
	- E.g. {In Documents} mkdir my_directory
		- No whitespace in file name or it makes multiple folders
			- e.g. mkdir day_01 day_02 day_03
				- makes 3 folders

- open .
	- Opens current directory in finder to see files available if lost

- mv
	- Changes name of file
		- e.g. {In my_directory} mv {current name of file.txt} {new name of file.txt}
		- Can also just do in finder
	- Also can move files
		- e.g. {IN my_directory} mv {file name.txt} ~/{TAB KEY to show options of folders, then TAB through options}

- touch {file name.md}
    - Create new file, .md, .txt, et.c

- rm -rf 
	- <mark>BE VERY CAREFUL WITH THIS COMMAND
	- Forcefully deletes folders, even protected ones without asking

- git status
    - See if code is in staging area to be committed

- git add .
    - add all changes to staging area to be committed

- git commit -m "add commit message"

- git push
    - pushes committed code to repository

- git log
    - show commit history

- git pull
    - pull any new code from repository to local machine

- git branch
    - show list of branches that exist locally

- git init
    - Creates a .git folder
&nbsp;

&nbsp;
## New Repository Set-up
1. Head to Github, create a new repository, add readMe file
2. Copy SSH link in the green CODE section
3. In the terminal:
    ```
    cd repos/
	git clone {past SSH link here}
    ```
4. To test connection:
    ```
    cd {repository file name}/
	git remote -v
    ```
&nbsp;

&nbsp;
## Add collaborator to GitHub Repo
1. Navigate to the Settings page and select Collaborators on the left-hand side
    - By default, if your repository is public (which you can see up the top left), anybody can clone it and make commits locally. But for someone to push to your repo, they need to be added as a collaborator here.

2. To add somebody, click Add people, and input either the username or email of the person you'd like to add. Once added, they will receive an email and will have to accept the invitation.
&nbsp;

&nbsp;
## Join Repo as a Collaborator
1. Click the green code icon, 
2. copy the HTTP URL link, 
3. ``` 
    git clone <insert URL you copied> 
4. Insert your username (LadyCaro)
5. Insert password 
    - need to create a token by going to settings, dev eloper settings, tokens, new token, click repo, then copy into terminal
6. Open in VSCode, then commit, sync and push any changes for others to see

&nbsp;

&nbsp;

## Adding code from collaborator to local machine
1. Open the code in VSCode
2. ```
    git pull
    ```
&nbsp;

&nbsp;
## Creating Branches
- [ ] <mark>To Be Updated
&nbsp;

&nbsp;
## Git Workflow

1. Modify files
2. git status
	- Check which files are not commited
3. Add files to staging area
	- git add [file]
	- OR git add . (means all)
4. git status
	- Check what is in the staging area
5. Commit the files in staging area and add commit message
	- git commit -m "Add desciptive message about file changes"
6. git status
	- Should say "nothing to commit"
7. Git log
	- Shows commit history

&nbsp;

&nbsp;
### When ready, push commits to GitHub
1. git push 
- OR 
1. git push origin main (if working with other branches)
	- Push work to GitHub repository
2. Git status
	- Should say “Your branch is up to date with ‘origin/main’. nothing to commit, working tree clean”
3. Reload repository on GitHub to show the changes. 

