**Git** is a version control system
******
- `git` gives u info about Git if it's installed
- `git --version` shows version of git which is installed if it's installed

## ==Main fundamentals of Git&Github==
- open path of project folder in terminal u use 
- type `git init` : to creat repo
- `git add style.css` to track changes on file 
- `git add .` tracks all files in the directory
- `git status` check status
- `git commit -m "added general style of pages"`  backups the repo and adding meannigful message
	- `-m` (msg)  
- to have an author account git config --global user,email"abdorabie@gmail.com" (it's important to add an author account because it won't back up until you have an account)
- `git config --global user.name"abdulazim"` 
- `git log` shows u the history of backups
- `git rm --cached main.docs` unstage file from staging area
- `git restore --staged index.html`
- `git clean -n` shows untracked files to remove it
- `git clean -f` removes untracked file
- `git branch`  shows branches
- `git remote -v` shows the ***link*** of repo
- `git remote` shows remote name
- `git push remoteName ranchName`  (remote name => origin , branch name => main , master )
	- `git push origin main`
- `git config -l` show list of configuration command
- `git pull origin` pulls changes and merge it 
- `git config --global --unset user.name` unset value of username
- `git config --global --unset user.email` unset value of email
- `git config --global --edit` to edit configurations
- `git config --global core.editor "code"` to set VScode as a default editor on cmder
- `git config --global alias.st status` setting "st" as an abbreviation for status command 
	- so if u wanna know status of repo > `git st` . that's it 
- `git config --global alias.cmm "commit -m"` we use double quotes when our commnd contains a space 
	- `git cmm "added a new folder"` 
- if u wanna unset ant values in configuration user `--unset` then put what u wanna unset 
	- `git config --global --unset core.editor` unset value of core editor to default 
## ==SSH==
[SSH keys for Github](https://jdblischak.github.io/2014-09-18-chicago/novice/git/05-sshkeys.html#:~:text=An%20SSH%20key%20is%20an,%2C%20you're%20granted%20access.)
## ==Branching & Merging==
- `git branch` : shows branchs
- `git branch new-feature` : creating a new branch
- `git checkout new-feature` : goes to the "new-feature" branch
- `gir checkout -b scroll-feature` : creates the "scroll-feature" branch then goes to it
- `git branch -m feature` : renames the opend branch to this name (feature)
- `git branch -d scroll` : deletes "scroll" branch , but you have to be in another branch to delte it . you can't delete branch is oppend 
- `git branch -D scroll` : forces to delete branch whether you merged it or not 
- `git merge scroll` : this will merge scroll barnch with main branch (opend branch)
## ==Stash==
stash = hiding 
- `git stash` hides files you've added ,,, it won't apper if you tried to use `ls` to know files in your directory
- `git stash list` shows list of stash 
- `git stash pop` return hidden files to staging area to be ready to commit these files
- `git stash save "message"` if you want to hide files (files which is on staging are) and write a message to make it easy to remember 
- when you type `git stash pop` that opens the last box and put his files on staging are to be commited 
- `git stash apply` adds files to staging area without deleting stash id (or box as we know) , So if you tried `git stash list` ,you'll see the last stash is existing
- if you want to drop a specific stash `git stash pop stash@{0/1/2}`
- `git stash drop` remove stash with files
	- `git stash drop stash@{1}`
- `git stash clear` clears all stashs 
- if you want to creat branch an put stash into it 
	- `git checkout -b newBranch`
	- `git stash pop`
## ==Reseting HEAD==
- `git reset --hard CommitHash` that makes the HEAD points to the commit hash you've typed 
	- i.e `git reset --hard 46de6be8ab07e330bdafd096e22abaf09049ff9a`
- `git push orgin main --force` then push the editions to the remote repository , we use `--force` to force to push changes and delete all commits after the specific commit
- `--force` = `-f`
## ==Ignoring files and directories==
to ingnore files and directories , creat a .gitignore file inside your local repository 
- `git touch .gitignore`
then open it in VS code
- `code .gitignore`
if you want to ignore a specific file , you can type file name and its extension like that `abdu.txt` . so now it you wanted to know the state of your rep `git status` you won't see abdu.text and you can't add it normally to staging are 
- ignoring all types of file => `*.pdf`
- except a file  `!me.pdf`
- ignoring directory `imgs\`
- to force file to be added to staging are otherwise it's ignored `git add -f abdu.txt`
- [Check it ](https://www.atlassian.com/git/tutorials/saving-changes/gitignore)
## ==Taging & Releasing==
- after committing your changes and typing message of committing you tag this 
- `git tag` shows tag you've done
- `git tag v1.2` that's lightweight tag (msg : form commit)
- `git push origin v1.2` you push this tag to the remote repository
- `git tag -a v2.0 -m "MSG"` that's annotated tag (msg : you type it)
- `git tag -l "v1.*"` / `git tag -l "v2.3"` => searching on versions or tags
- `git tag -d v1.0` : deletes v1.0 tag localy , so you've to push changes again
	- `git push origin -delete v1.0` : delete v1.0 tag remotely in remote repo
## ==Resources==
- [ ] [Problems](https://ohshitgit.com/)
- [ ] [Problems 2](https://dangitgit.com/en)
- [ ] [Nesi](https://support.nesi.org.nz/hc/en-gb/articles/360001508515-Git-Reference-Sheet)
- [ ] [Git Documentations](https://git-scm.com/docs)
- [ ] 