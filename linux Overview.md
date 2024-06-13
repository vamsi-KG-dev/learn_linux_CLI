DEF: linux is an open source operating system.The OS is the software that directly manages a system's hardware and resources.It sits b/t hardware and application.

**NAVIGATION commands**

**1.The'ls' command** in linux is a basic command used to list contents in curent directory.It is also used for Managing and Navigating files 
>**ls -l**:This command gives contents in the current directory in long format.
>**ls -a**:This command gives all the contents in current directory including hidden files
>**ls -lh** :lists files with sizes in a human-readable format ( KB, MB).
**Q1.Need of this command**
>for these below things the 'ls' command is needed
i)File Management
ii)System Navigation
iii)Verification(to verify the creation,modification of files and directories)
iv)Troubleshooting

**Q2.History of This?Understand with examples?**
>This command derive from Unix,developed in the early 1970's.
>Evolution(-ls)
>It became a standard command in POSIX_complaint system(unix,mac os etc..)
>Integration: The 'ls' has been integrated into various scripting languages and automation tools.making it as primary in system administration.

**Q3.if we do NOT use it ,What will happen?**
>Difficulty in File Mangement
>Navigation Issues
>Increased Errors(while perfomiing file opertaions)
>Troubleshooting Issues

**Q4.Other ways of doing this?**
>File Managers(graphical file managers like Dolphin provide visual directory listings)
>Other commands: like 'find','tree',or 'du' also lidt the files
>Scripts:Custom scripts using programing languages(python)

**Q4.Why to use it?**
>simplicity,Efficiency,Flexibility(various options '-l','-a'),Integration(for easily integrated scripts into file management)

**Q5.When for NOT use it?**
>Large directories(bcaz it takes more time)
>Remote system with latency
>when Detailed Information Needed


**2.pwd command**
>This command is use to print the present Working directory.It tells u exatly where you are and gives you full path i.e,absolute path.

**3.cd command**
>change directory command is used to change the current working directory to another directory
>***Diffrent cd commands:***

cd: The command itself means "change directory."
cd ~: (~) represents the home directory.
cd /: (/) represents the root directory.
cd ..: (..) represents the parent directory.

>***Here are examples of using***
Change to Home Directory: cd ~
Change to Root Directory: cd /
Change to a Specific Directory: cd /home/user/documents
Change to Parent Directory: cd ..
>One more thing that related to 'cd' comand that is very useful.let's say that you are in downloads folder and you need need jump another directory that is somewhere else on the file system so in this case we are goin to use the following commands
**1.pushd /etc**
**2.popd( put working directory on a stack)**

**4.file command is use to determine the file type**
>linux  doesnt bothered about extentions like (.pdf,.pptx)it can identifiy it self the file type.
***file .filename***

**5.locate command is used to find loaction of the file in file system**

>***locate (filename)*** command is used
Linux system need to updated database to loacte files more efficiently for this this following command is used ***updatedb**

**6.which command is used to locate the command**
>It finds other command for us .so if you know what a command is but you dont know where it is loacted.
eg:***which cal** is used to check if it installed or not in system
then enter command ***cal** it shoes the calender an date of the day

**7.history**
This command shows all of the commands till we used in the current session

------------------------------------------------
**GETTING HELP**

There's plenty of help available to you and her few options for getting help
**1.whatis command**
This command will gives you little explanation so we looked at the Cal command which is calender command and it says displays calender  and the date that's all it does.
>In linux this command is used to display a brief description of a command ,it helps to understand the purpose of various command without reading full manner.
>***NEED***:Quick Refernces,Leanrning new commands,Verification(verify purpose of command before excute it),Documantation(while writting scripts user can checks the purpose of command)
>***if we do NOT use it,wt happens?***:
.Longer Time to understand the command
.Increased errors(users might misinterpret command functions and make errors in execution)
.Documantaion Inaccuracies

>***Other options of doing this***:
.Manual pages:use the 'man' command to read the full manual page(eg:'man ls')
.Help option:'--help' used to get summary of command options and usage(eg:'ls --help')
info Pagees:('info ls')is used to more detailed documantation
 >***How to Use it?***
.Basic Usage: ***whatis ls***
.Multiple Commands: ***whatis ls cp mv*** 'ls' is the argument for which you want the description.
.Wildcard Usage: ***whatis *net* ***(shows descriptions of all commands containing 'net')
.With Sections: **whatis -s 1 ls** (shows description from section 1 of the manual)

**2.apropos**
>This command is used to search the manual page names and descriptions. It is useful for finding commands related to a particular topic or keyword.
>Using 'man -k network' achieves the same result as apropos network

**3.man command**
>The man (manual) command in Linux provides detailed documentation about commands, system calls, library functions, and other aspects of the operating system
>***How to use it***
.Basic Usage: ***man ls** (displays the manual page for the ls command).
.Search by Section: ***man 5 passwd*** (displays the manual page for passwd in section 5, which covers file formats).
.Search for Keyword: ***man -k network***(searches for all manual pages related to "network").Network is the keyword
.View Specific Section: ***man -s 2 open***(displays the manual page for the open system call in section 2).open is syetem call to look up
------------------------------------------------

**WORKING WITH FILES**
> These commands are used to work with files an and dirctories directly .
**1.mkdir command**
>In linux 'mkdir' is used to create new direcctory in file system
>***NEED***
>It is used to Organize files ,Project Intialization,Backup and Storage.
>Another way to crteate directory in File system API's in programming language like python(0s.makedir) to create directory
>It is used for Simplicity,Automation,Consistency.
>This command is no need to use in such cases liken Single file Storage,temporary file etc..
>Eg:***'mkdir new_dir'*** here mkdir is command and new_dir is name of the directory.
>***mkdir -p parent/child***: -p is an option to create parent directories, and parent/child is the directory path.
>***mkdir -m 755 new_directory***: -m 755 sets the permissions to 755, and new_directory is the name of the directory.
>***mkdir -v new_directory***: -v provides verbose output, and new_directory is the name of the directory.

**touch command**
>touch command is used create an empty file that not exist in the directory and also to know the last date and time that has been accesed.It usefull in Backup Strageties ,to know lastly backup time ...

**cp command**
>This command is used to copy files and directories from home directory in file system.
>**NEED**: Backup files to prevent data loss,Duplicate configurations,File Organization etc..
>If we do not use this leading to several issues and challanges such aa Data loss risk,Disorganised files..
>Basic Usage:*** cp file1.txt file2.txt*** (copies file1.txt to file2.txt).
For directory :*** cp -r dir1/ dir2/ ***(copies the contents of dir1 to dir2 recursively).

>Other options of doing this are listed below
.rsync: A more advanced tool that can copy files and directories, often used for backups and synchronization ***(rsync -a source/ destination/)***
.scp: Used for copying files over a network securely ***(scp file user@host:/path)***
. ***Drag and Drop***: In graphical environments, users can drag and drop files to copy them to different locations.

**mv command**
>move command is used to move files and directories from one location to another or to rename them. 
>Basic Move: *** mv file1.txt dir/ ***(moves file1.txt to dir).
Rename File:***mv oldname.txt newname.txt***(renames oldname.txt to newname.txt).
Move Directory: ***mv dir1/ dir2/***(moves dir1 to dir2)

**rm command**
>The rm (remove) command in Linux is used to delete files and directories.
>*** rm file1.txt ***(deletes file1.txt).
>*** rm -r dir/ ***(recursively deletes dir and its contents)
>It is used to Removing Tempoerary files ,Cleanig up projects,Freeing Up Space and Secure deletion.

**rmdir command**
>This command in linux is used to remove empty directories and files.
>If it was not used causes Disk Space Shortage,Secruity Risks etc.
>*** rm file1.txt ***(deletes file1.txt).
>*** rm -r dir/ ***(recursively deletes dir and its contents)
>It used in Cloud storage managemnt and Database Cleanup etc..
------------------------------------------------

**TEXT FILES**
 
***1.cat command*** (concatenate)
>In linux commandline The cat command is use to list bunch of files or content in the files.
>It is used to View file contents,Conacaterating files,Copying Files and creating Files.
>There are alternative ways to achieve the same functionality as cat.
1.***less or more***: For viewing file contents with paging.
2.head and tail: For viewing the beginning or end of files.
3.cp: For copying files.
4.Text Editors: Using editors like *** nano or vim *** for viewing and editing file contents.
>***cat file1.txt*** (displays the content of file1.txt)
>*** cat file1.txt file2.txt *** (displays the content of both files).
>*** cat file1.txt > file2.txt *** (copies the content of file1.txt to file2.txt)
>***cat file1.txt >> file2.txt***(appends the content of file1.txt to file2.txt).
------------------------------------------------

**USERS**

**1.sudo command**:It is used to alloe the user to excute a command as the another user.
>***Need of this command***:For the following thinga this command is needed i.e,System Administration,Secruity,Logging and Granular Permisions.
>For better Enhanced Secruity ,Auditing,convinience and control purposes we use this command.
>It is use when we do System updates,User Management,Service managemnent and File syetm Changes.
>***'sudo command'*** (Runs a command with elevated privileges).
>***'sudo nano /etc/hosts'*** (Opens the /etc/hosts file with nano editor as root).
>***sudo ./install_script.sh'***(Runs an installation script with elevated privileges).
>***'sudo apt update && sudo apt upgrade'*** (Updates package lists and upgrades installed packages on Debian-based systems).
>***su Command***: Switch to the root user for performing tasks.

**2.su command**:It used to switch the current user to another user account. If no user is specified, it switches to the root user by default.
>It is need to be use for the Dircet Access,Debugging and User Management..
>Switch to Root: ***'su'*** (Switches to the root user)
>Switch to Another User: ***'su username'*** (Switches to the specified user account).
>chroot: Change the root directory for a command or shell session, effectively isolating the environment.

**users command**
>The users command in Linux displays a list of all users currently logged into the system.
>The need of this command is to system monitoring,Resource management and auditing.
>Other options for doing same thing are:
.who: Displays a list of logged-in users and their login times.
.w: Provides a detailed view of logged-in users and their activities.
.finger: Offers comprehensive information about logged-in users.
.last: Shows a list of the last logins to the system
>It gives Quick overiew
>Basic use of this command:
.Basic Command: Simply type 'users' in the terminal to see logged-in users.
.With Redirection: Use 'users > logged_users.txt' to save the output to a file.
.In Scripts: Integrate into a script: 'echo "Current users: $(users)"'.
.Filtering Output: Combine with grep to filter specific users: 'users | grep 'username''.

**id command**
>It is used to print user and group information for the specified user, or the current user if no user is specified. This information includes user ID (UID), group ID (GID).
>It is used in various scenarios like Secruity audit and user verification etc..
>Other commands and methods to obtain similar information include:
whoami: Prints the current user name.
groups: Lists the groups a user belongs to.
getent passwd [username]: Retrieves the user's details from the passwd database.
stat [file]: Shows detailed information about a file, including owner UID and GID.
>It is used before file opertaions and after login and also in Scripts
>Examples of using the id command:
Basic Usage: 'id' to display information about the current user.
Specific User: 'id username; to display information about a specific user.
User ID Only: 'id -u' to display the user ID only.
Group Information: 'id -G' to display all group IDs of the current user.
-----------------------------------------------------------------------------------------------------------

**CHANGING FILE PERMISSIONS**
>changing file permissions is crucial for controlling access to files and directories. The primary command used for this purpose is 'chmod;
>change mode
>If we do Not use this command dat loss may be occurs and execution failure also occurs.
>'chown' Command: Changes file ownership, indirectly affecting permission management.
>Use the chmod command in scenarios such as:
.After file creation,Before runnning scripts and File sharing.
>Examples of using the chmod command:
Basic Usage: 'chmod 755 filename' to set read, write, and execute permissions for the owner, and read and execute for group and others.
Symbolic Mode: 'chmod u+x filename' to add execute permission for the owner.
Recursive Change: 'chmod -R 644 directory' to change permissions of a directory and its contents.
Removing Permissions: 'chmod o-rw filename' to remove read and write permissions for others.
-----------------------------------------------------------------------------------------------------------

**KILLING PROGRAMS AND LOGGING OUT**
Ctrl+C - kill a running command
killall - kill processes by name
exit - log out of bash

**USEFUL SHORTCUTS**
Ctrl+D - signal bash that there is no more input
Ctrl+L - redraw the screen
Ctrl++ - make text bigger in terminal emulator
Ctrl+- - make text smaller in terminal emulator

