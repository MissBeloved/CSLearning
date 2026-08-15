**pwd** [print working directory]
- pwd
- display the current directory path from the root directory '/'

**ls** [list files and folders]
- ls
- ls -l [displays all the files and folders with long list in detail]
- ls -a [displays all the hidden files and folders]
- ls -la [displays all the hidden files and folders in long lost along with the normal files and folders]
- ls -lh [display the file size in human readable form]
- ls -lt [display all the file in updated time.. recently updated to last updated order]
- ls -R [display all the files or folders in each folder and subfolders recurssively]
- ls -r [displays all the files or folders in current directory in reverse alphabetical order]
- ls *.txt [display all the txt file names]
- ls file??.txt [display all the txt files with ]
- ls directory/*/ [display files and folders in subfolder]

**cd** [change directory from current directory]
- cd [navigates to home directory]
- cd directoryname [navigates into the given directory]
- cd .. [directs to one up directory]
- cd ~ [navigates to home directory]
- cd / [navigates to root directory]
- cd - [navigates to previously visited directory]
- cd path [navigates to the given path]

**mkdir** [creates a new empty directory]
- mkdir singleDirectory
- mkdir dir1 dir2 dir3 ...
- mkdir -p dir/subdir1/childDir [creates directories if they not exits that was given in the path]
	Create parent directories automatically: If any directory in the path doesn’t exist, `mkdir -p` will create it. Without `-p`, `mkdir` would throw an error if a parent directory is missing. -p stands for parent
- mkdir -p revision_day3/{linux,python,networking,notes}

**rmdir** [remove an empty directory]
- rmdir dir1 [can remove single or multiple empty directories]

**touch** [creates an empty file or changes the time stamp of the files or folders]
- touch filename.ext [creates an empty file]
- touch file1 file2 file3 ... [creates multiple files]
- touch existingFilename [updates timestamp for the file]
Ex:
touch file{1..5}.txt [creates file1 to file5, by using the wildcards]
touch "my file.txt" or touc "my\ file.txt" [cretes file witl space]

**cp** [creates the copy of the existing file or folder]
- cp existing.txt copy.txt
- cp path_of_the_file_to_copy path_of_the_file_to_paste
- cp -r folder1 folder2 [folder1 is existing and folder2 is new, -r is recurssive to copy files inside the folder1]
- cp -i
- cp -v

**mv** [rename or move file or directories]
- mv old.txt new.txt [rename file name]
- mv notes.txt Documents/ [move from current directory to another]
- mv directory directory/ [move folder to another]

**rm** [remove file or directory]
- rm filename.txt [remove file]
- rm file1.txt file2.txt file3.txt [remove multiple files]
- rm -r folder [delete folder with files inside it]
- rm -rf folder [force delete deletes even protected files]

**clear** [clear the terminal]
- clear or CTRL+L

**history** [display all the history from the starting command to very recent command]
- history
- !! [runs previously run command]
- !n [n is a number. the command in history run again]
- *Some commands that pipes connect history with other commands*
- history | head [print first 10 commands number 10 is default]
- history | tail [print last 10 commands]
- history | head -n 1 filename.ext [displays the first number, here -n represents the number of lines should display]
- history | tail -n 5 filename.ext [displays the last 5 commands]
- history -c clears the current shell's history.
- history -w writes the (now empty) history to ~/.bash_history, overwriting the previous contents.
Note: 
- history -w first and then history -c [so it clears complete history]
- history -c first and then history -w 

**whoami** [displays the hostname that we are currently logged in(username)]
- whoami
- echo "Current user is $(whoami)" [can also use in scripts]

**hostname** [displays the system's hostname]
- hostname
- hostname -I [display IP address]

**date** [displays the date and time]
- date [displays the date day month timestamp year]
- date +"%d-%m-%Y" [custom format]
| Code | Meaning |
| ---- | ------- |
| `%d` | Day     |
| `%m` | Month   |
| `%Y` | Year    |
| `%H` | Hour    |
| `%M` | Minute  |
| `%S` | Second  |

**cal** [displays current month calender]
- cal
- cal 2025 [display whole year cal]
- cal 8 2025 [specific month calender]

**echo** [write to the terminal or file]
- echo Hello [display in terminal]
- echo "text">filename.txt [overwrites into the file]
- echo "text">>filename.txt [appends into the file]

**cat** [displays the content in files]
- cat filename.ext [display content in the file]
- cat>filename.ext [creates the file and ask to write]
	after enter text press CTRL+D to exit from writing into the file
	>> in place of > if you wanna append
- cat file1 file2 [concat files]
- cat -n file.txt [display the numeber of lines]

**Linux Filesystem**
/ [root directory]
~ or /home/username [home directory]
important files
- /home [stores multiple user directories]
- /root [home directory of administration user]
- /etc [configuration files and users details and permissions]
- /var [logs/data that are repeatedly changes]
- /usr [applications or softwares]
- /opt [optinal third party softwares]
- /tmp [temporary files]
- /bin [user system commands]
- /sbin [administrator commands]
- /dev [device files representing hardware]
- /boot [files required to boot the operating system]
- /proc [virtual file system with process and kernel information]

**tree** [display the structure of the files and directories in the tree structure]
- tree is the software have to be installed before by using sudo
- 'tree' command helps to print the structure of the current directory which we are in present
- 'tree directoryname' helps to print the directory structure. if we use directoryname then we have to be on above the top level of the current directory

**head** 
- head filename.ext [display first 10 lines of data by default]
- head -n filename.ext [display n number of lines from the starting of the file. n can be any positive number]

**tail** 
- tail filename.ext [displays the last 10 lines of data by default]
- tail -n filename.ext [display n number of lines from last.]

**less** [opens a scrollable view]
- less filename.ext
- controls:
	- ↑ / ↓: move line by line
	- Space: next page
	- b: previous page
	- q: quit

**more** 
- more filename.ext
- q key is used to quit
- space is used to display the next page
- more it only one side view. where less allows two way navigation
- less is preferred over more because it allows both forward and backward navigation.

**nano** [creates a file]
- nano filename.txt
	- Save: Ctrl + O
	- Confirm: Enter
	- Exit: Ctrl + X

**Wildcards**
- * [matches zero or more characters]
	ls *.txt [displays all txt files]
	rm *.log [removes all log files]

- ? [matces exactly one character]
	ls file?.ext [display all the files with file_ last character differ]
	ls file??.ext [display all the files with last 2 char differ]

**Redirection & pipes**
- > [overrides]
	echo "linux">file.txt [replace the content]
- >> [appends]
	echo "Linux">>file.txt [add at last]
	NOTE: > and >> are output redirections
- | [sends the output left command to right command]
	Examples: history | less
	ls -l | less
	cat test.txt | less

***Check your user***
- Linux stores all the id numbers in etc/passwd/
- **whoami** [display current username]
- **id** [displays uid, gid and groups]
	- id [display current user id numbers of user id, group id and the groups he was in]
	- id username [display the userid, group id and groups existed of given username]
	- uid range (0, root), (1 - 999, System users and service accounts), (1000+, regular human accounts)
	Note:	System users (daemon,www-data, mysql, nginx, postgres, sshd)
			To know system user id number [id daemon, id system_user]
- **groups** [displays all the groups that the user belongs too]
- **who** [displays all the users that were currently logged in]		
- **cat /etc/passwd** [displays all the account information]
- **cat /etc/groups** [displays all the groups] 

***File Permissions***
- For directory drwxrw-r--  and for normal files -rwxrw-r-- and  l represent symbolic files
- permission order
	- (user)(group)(other)
- permission symbol
	- r - read [4 in number format]
	- w - write [2 in number format]
	- x - execute [1 in number format]
- Directory permissions
	- r - read [List the contents of the directory using `ls`]
	- w - write [create, delete or rename files inside the directory]
	- x - execute [enter the  directory using cd or access files inside it]

**chmod** [used to change permissions for a file or folder]
- chmod permissions filename  [change mode]
- Symbolic method (chmod [who operator permission] file)
	- + add permission
	- - remove permission
	- = set exact permission
	- Ex1: chmod u+x script.sh [add execute permission to only user]
	- Ex2: chmod +x script.sh [add execute permission to all]
- permission category
	- u - user/owner
	- g - group
	- o - other
	- a - all
- Numeric method (chmod xyz filename) [where x is user, y is group, z is other]
	- 0 = ---
	- 1 = --x
	- 2 = -w-
	- 3 = -wx
	- 4 = r--
	- 5 = r-x
	- 6 = rw-
	- 7 = rwx
	- Ex: chmod 700 file.txt [where user = rwx, group and others = ---]

***Creating user***
- sudo adduser username [creates user]
- id username [to know the user, group ids of the user and groups he was in]
- sudo userdel username [remove account but keeps their home directory and files]
- sudo userdel -r username [remove user account and files and directory]

***Creating groups***
- sudo groupadd groupname [creates new group]
- getent group groupname [verify the group exists]


**chown**
chown changes the ownership of the file
- -rw-r--r-- duo developers notes.txt [duo is owner and developer is group]
- sudo chown new_username_to_set file.txt [change user]
- sudo chown :new_group_to_set file.txt [change group]
- sudo chgrp new_group_to_set file.txt


**Package Management**
sudo apt update [run update command]
- sudo means "super user do" that gives administrator privileges. simply "run as administrator" in windows
- apt means ubuntu package manager
- update means refresh package list.
sudo apt upgrade -y [after sudo apt update command, used to update installed packages]
- means install updates
- -y means yes
sudo app install softwarename -y [install software]
sudo app remove softwarename -y [remove software]
- Ex: Tree is a software which is used to show the structure inside the folder visually