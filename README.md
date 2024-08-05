# Programmering
¤================¤                                                                                  ¤====================¤======¤
| Git user guide |                                                                                  | By Anya Roza Kragh | v0.1 |
¤================¤==================================================================================¤====================¤======¤

	Cheat sheet of some(but not all!) useful commands.

	git init											(creates a rew repository (.git folder))
	git add <file1> <file2>								(adds the the file/files to the commit)
	git add .											(adds all files to the commit)u
	git commit											(commits your changes to the current repository)
	git commit -m '<comment>'							(same as above but allows you to write a comment without a text editor)
	git branch											(displays all local branches)
	git branch -r										(displays all remote branches(-a for both remote and local))
	git branch -vv										(displays local branches currently in use(-vva for remote and local))
	git branch <name>									(creates a new branch)
	git branch -m <old_name> <new_name>					(renames an existing branch)
	git branch --delete <branch_name>					(deletes a branch)
	git checkout <branch_name>							(switches to the specified branch)
	git status											(shows the changes that will be committed and what won't be committed)
	git log												(shows a log of all previous commits with their comments)
	git push origin <branch>							(pushes the changes from your local repository to your remote repository)
	git pull origin <branch>							(pulls all changes from your remote repository to your local repository)
	git clone git@github.com:<user>/<repo>.git			(clones a remote repository to your local machine)
	git remote add origin <ssh/https address>			(adds a remote repository as an origin for the local repository)
	git remote -v										(shows all remote addresses saved)
	git config --global init.defaultBranch <name>		(changes the default branch name for newly created repositories)
	git config --global user.email <your@email.here>	(add your email signature)
	git config --global user.name <your_name_here>		(add your name signature)

¤=============================¤
| Best practice prerequisites |
¤=============================¤=================================================================================================¤

	(This guide assumes that you have either Git or Git CLI installed already)

	Before we start there are some prerequisites to git that are considered best practice/industry standards.
	These are things that we will configure globally so you will only have to do it this once.

Step 1:

	Git's default branch is called master because back when git was made it was still common to name things master/slave.
	Nowadays this is considered antiquated and bad practice but is kept in for legacy compatibility reasons.

	So the first thing we will do is rename the default branch to main.
	To do this systemwide we will be using the '--global' flag as well.

	Type 'git config --global init.defaultBranch main' into either Git CLI or your terminal depending on
	if you are using either Windows or Linux/Unix/MacOS.

Step 2:

	Next we will add your name and email signature to your git so your commits can be signed as yours.
	This is mainly for when you are working on projects with other poeple so you can check the log to see who did what and when.

	Type 'git config --global user.email <your@email.here>' and 'git config --global user.name <your_name_here>'
	into either Git CLI or your terminal depending on your system.

¤============================================¤
| Creating a new git repository from the CLI |
¤============================================¤==================================================================================¤

Step 1:

	To create a new git repository you will first have to go into your project directory/folder and use the command 'git init'. 
	This will inizialize a new empty git repository inside the directory.

Step 2:

	To add files into this new git repository you can either use 'git add <file1> <file2>' to add individual files
	or use 'git add .' to add all files in the current directory. Using either command will add the files to the next commit.

	You can check if all the files you want added are staged for commit by using the command 'git status'.
	Files staged for a commit will be highligted in green while files not staged will be highligted in red.

Step 3:

	To add these files into the git repository you can use the command 'git commit'.
	This will open up your default text editor first where you can write a short comment for logging purposes.

	Alternatively you can use 'git commit -m '<comment>' ' this will not open your default text editor
	as the flag -m allows you to write your comment enclosed with '' at the end of the command.

Step 4:

	Now that you have added/committed your files to the git repository you can check the git repository's log
	by using the the command 'git log'.

	This will display all the commits to the repository along with the date of the commit and associated comment.
	If working with others on the same repository 'git log' can also be useful to see who committed what and when.

Example:

	A typical example of what commands you would use to create a new git repository through the CLI.

	git init
	git add .
	git status
	git commit -m 'first commit'

¤===============================================================================================================================¤
