# 01: Intro and what are the shell, terminal, and CMD?

## Info

- ### ==Shell==
    
    : command line interpreter (المترجم اللى بيترجم الأوامر)
    
- ### ==Terminal==
    
    : text input/output environment (بيئة العمل الل بنكتب فيها الاوامر)
    
- ### ==CMD==
    
    : the original shell of Microsoft dos operating system (ده خاص ب مايكروسوفت)
    
- ### ==PowerShell==
    
    : after CMD ( more powerful than the shell )
    
    * * *
    

## Commands

- `cd` change directory
- `chdir` change directory but we use the above command since it's fast
- `wmic` Windows management interface commands
- `cd ..`  go back 
- `cd\` go back to the root 
- `mkdir` make a directory (a folder)
- `ls` list of dirs (mac and linux)
- `dir` list of dirs (windows)
- `C:` move to C partetion directly 
- `D:` the same
- `move` (only windows) move file or folder
	 `move sample.txt imgs` but if there is not a file called "imgs" => sample file will rename to imgs (so inteligent terminal )
- `mv` (mac and linux) works like `move` command :
    `mv sample.txt ..` this will move "sample.txt " file to the previous folder in the path 
- `rename` rename a file and his extension  at the same time :
	- `rename file.css script.js`
- `ren` also rename a file with his extension at the same time
  	- `ren sample.txt index.html` 
- `touch` make a file (not a folder)
  - `touch data.php` / `touch index.html style.css` / `touch project\script.js`
- `cp` stands for "copy" , so this copys file or folder to another file or folder :
  -  `cp index.html projectOne`
- `del` stands for deleting a file or folder :
	`del index.html`
- `rmdir`  (Microsoft)  stands for removing a directory or a file :
	`rmdir todoProject`
- `rm` (mac and linux) stands for removing a file or folder :
	`rm style.css script.js`
	- `rm -rf` stands for "force to delete a folder and what contains" so `rm` won't work if you want to remove a folder which has files and folders inside of it . we use `rm -rf name_of_file` to force computer removing it 
	`rm -rf css js`
	- `rm -d` if the directory is empty ,it will be removed and if not you'll get a message that this file is not empty so computer can't remove it (that's so important an many cases ... think about it): `rm -d ProjectOfUniversity`
- `echo` : print someting one console or inside a file :
	`echo "Hello world"` / `echo "Hello World" > file.txt`
	if i wrote `echo "again Hellow world > file.txt"` this will override the existed content , So if i want ot append texts  ... use `echo "agian salting >> file.txt"`
-`cat` : stands for concatenate strings in programming language here it append texts inside files and in addition to showing the content of file in console :
	`cat file.txt`  / `cat "hello" > file.txt` / `cat "world" >> file.txt` / 
	another trick , you absoluty can copy file content to another file `cat one.txt > two.txt` it there is a file called "one.txt" the terminal will copy the content of one.txt file to two.txt file ... if not .. guess you! yes that's it ,terminal'll print "one.txt" as  a word inside two.txt file ... it's as simple as that.
`cat *` => content of files in the directory will be shown in console (awsonme trick!)
- `date`  shwos the current date , you alse can print date in text file `date >> file.txt`
- `time` shows current time
- `grep` stands for "general regular expresion print" ... searchs on specific word or letter or sentence ... examples => 
	- `grep "abdu" file.txt` search on abdu in file.txt
	- `grep "abdu" -r` search on abdu in the directory
	- `grep "abdu" -r -l` gives you list of files have this word (doesn't show the line contains the word as default)
	- `grep "abdu" *`      `*` => search on all files , but differs from `-r` 
		-  `*` will search on files and gives the direct files , but if there is a file inside a directory , it wont show it in terminal . it will just indicate it .
		-  `-r` recrusive : will show you all files either direct file or not
	- `grep "abdu" -r -n` shows number of lines
	- `grep "abdu" -o` displays on word (won't show full line contains the wrod)
	- `grep "abdu" -i` doesn't care about case sensetive
	- `grep "abdu" -c` count the word in a file
	- `grep "abdu" -w` whole word 
- `file *` gives you all kinds files in ther directory (note: that doesn't care about extension)
- `move /?` shows the manual of this command (explain what this command does)
- ***ctrl + c*** => stops the process
- `tree` shows directories only 
- `tree /a` same use of the above command
- `tree /f` shows you both folders and files
-  `osk` open screen keyboard
-  `tasklist` show tasks is running on device right now
-  `taskkill` kills process `taskkill /im notepad.exe /f` / `taskkill /pid 1243 /f`
-  `start` open app `start notepad` / `start calc`
-  `alias` shortcuts of commands , for example : insted of writing `explorer` command , you can write `e. notepad` . don't forget you can creat shortcut for you `alias ab=abdulazim`
-  `&&` write two commands `echo hello >> one.txt && cat two.txt`
-  `whoami` shows device's name
-  `systeminfo` 
- `systeminfo >  system_file.txt` get system info and push these info inside txt file
- `ipconfig`
- ` (something) | clip` this saves (something) to clipboard of ms (means: just copys it)
	- `ipconfig | clip` : this copy ipconfig info 