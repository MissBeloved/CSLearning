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