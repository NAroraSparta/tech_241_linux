Linux is a popular open-source operating system that is based on the Unix operating system. It was initially developed by Linus Torvalds in 1991 and has since grown to become one of the most widely used operating systems in the world. Linux is known for its stability, security, and flexibility. 

Here are some of its main advantages:
1. Fast growing
2. Open source
3. Stability and reliability
4. Security
5. Customization and flexibility
6. Wide range of software and applications
7. Cost effective
8. Compatibility and hardware support

Kernel is a core operating system and it's libraries.

Linus is case-sensitive.

Some important commands:
1  ls		                             To list all the files


2. cat > file1	                        To create a new file


3. cat file1 	                        To read the contents of the named file


4. cat >>file2                          To add anything to the file and use CTRL+D to exit 


5. cat file1 file2 >new                 To copy contents of file1 and file2 to newfile 


6. tac new	    To read the content upside down(last line first and then all others in descending order)


7. cat file2 > file1	To copy content of file2 to file1 (content of file1 gets overwritten)


8. touch <file3> file4 file5 	To create new file/s- file3, file4 and file5 , to change all timestamp or update only access time or modify time of a file)


9.stat <filename>	to check the time stamp of any file (access time, modify time of a file)

10.   stat -a  to check the access time of any file

11. vi <file_name>	To create a file with VI/VIM editor , press ESC and then :wq

12. :w 	                to save


13. :q              	to quit


14. :wq             	to save and quit


15. :q!	                to force quit, no save


16. nano <filename>     To create a file with nano editor


17. ls -l            To see the long list with directories n permissions


18. ls -a           shows all entries for files, including those that begin with a dot (.)-the hidden ones


19. history             To see all the commands used on linux terminal 


20. Hostname		        Hostname of the machine


21. Hostname –I		        IP address of host machine


22. Ifconfig			    IP address of host machine


23. Cat /etc/os-release	    Operating system release version


24. Whoami                  To see the name of currently logged in user


25. mkdir <name_of_directory>   To make a new directory


26. Ctrl +l	                To clear screen


27. uname                   To see the name of OS in use


28. uname -r                Kernel release version


29. uname -p                Name of the processor running


30. uname --help            Lists all commands to be used with 'uname'


31. uname -n                    Nodename or Hostname


32. mv <old_name> <new_name>    To rename a file


33. cp <old_name> <new_name>    To copy a file from one to another


34. rm <file_name>              To remove a file


35. rm -r                       To delete everything 


36. file <file_name>            To find out the type of the file


37. head -2 <file_name>         To display first 2 lines of the file


38. tail -2 <file_name>         To display last 2 lines of the file


39. nl <file_name>              To add numbers to the lines


40. curl                        Tool to transfer data to and from a server

41. cat <file_name> | grep <keyword>    To find any particular keyword/word in the named file

42. sudo apt install tree           To install tree package

43. sudo apt update -y              To update any packages already installed on the system

44. tree                            To view files and folders in a tree way

45. mv <File to be moved> <folder where you want the file to move to>

46. mv ../chicken-joke.txt.     Move file named chicken-joke.txt from parent folder to current folder

47. cp <file name to be copied> <new name>      To copy from one file to another

48. mv <file name> ~            To move any file to home folder

49. printenv                    To print all environment variables

50.  printenv USER              To print the USER 

51. MYNAME=neha                 To add a new environment variable

52. echo $MYNAME                To print your name on the screen

53. export MYNAME=neha          To add a new variable to environment variables

54. printenv MYNAME             To print your chosen variable to the screen

55. nano .bashrc                To add/edit any environment variable. Addition is at the end.  

56. source .bashrc              Reload that configuration in the session. Exit and re-Login to check the environment stays.

57. ps                          Brings up user processes

### Processes are of two types- System and User processes
### Every process has a Process ID (PID)

## Environment variable
### -edit .bashrc
### if in that current session, reload: source .bashrc

58. ps --help simple

59. ps -aux                 Detailed info about all the processes running

60. sleep 5                 System waits for the number of seconds specified

61. sleep 5000 &            Gets a pid and runs in the background for 5000 seconds

62. jobs                    Lists the jobs running in the background

63. jobs -l                 Lists all processes running in the background
    
64. kill -1 <PID>           Most gentle way of hanging up or shutting down a process
    
65. kill <PID>              Immediately forcefully kills a process(Parent as well as child processes). This is also called Kill-15
    
66. kill -9 <PID>           Brute force, kills Parent processes and child processes keep using the memory and are called zombie processes
    
67. ps -ef                  To list all parent processes n child processes
    
68. .                        current directory
    
69. ..                       parent directory
    
 ##   #!/bin/bash

# update the sources 
sudo apt update -y

# upgrade (sometimes you dont want to upgrade because it installs new packages that might be incompatible with the existing softwares versions.)
sudo apt upgrade -y

# install nginx
sudo apt install nginx -y

# To view status of your Nginx server
sudo systemctl status nginx

# restart nginx
sudo systemctl restart nginx

# enable nginx    #- nginx will auto start on restart/reboot
sudo systemctl enable nginx

# What is Bash?
## Bourne Again SHell Unix was a text based operating system. Bash is an upgraded version of what was used in Unix.

/bin/bash

# What is a Shell?
## It is a software that basically provides interface to run commands.

###  There are multiple shells

cat /etc/shells -       listing all different shells installed in your os

ps -p $$ -              shows the processes that we are running (-p $$ specyfing current process)

!22 -                   ran the command from history under the number 22

history -c - cleaning the history

Linux treats everything as a file. Even the folder

c root directory - separate from the other users directories. It is for super user

## blue color is for directories, white for files

curl <url> --output <name of the file we want to save the data> - saving the data to the actual file we specified


rm -r <directory name> - removing directory -r means recursive. It will remove wverything inside the folder as well

apt install tree - to install packages e.g tree package

add sudo for super user permission

tree commands       
tree -                       tree structure for files and folders for where you currently are

sudo apt update -y -        update sources list just in case package is not on the list. -y to agree for the questions

# Scripting
## Making a script file

touch provision.sh - 
.sh - script files 
nano provision.sh -                  open editor to write commands

## if you are owner of the file you dont need to use sudo

#!/bin/bash -                       always start to mention which shell we want to use

./provision.sh                       To run a script

# Nginx (engine-x) is a popular open-source web server and reverse proxy server. Commonly used in web hosting environments to serve websites and web applications.

## systemctl is a command-line tool used to control and manage systemd services in Linux. Systemd is a system and service manager that provides a range of funcionalities including, starting, stopping and monitoring services.

## In the given script systemctl is used to interact with Nginx service.

# Environment variables
value stored in memory, it can be accessible by other tools in Linux

printenv -                              printing all environment variables and values e.g USER, PATH,

printenv USER -                         printing specific variable USER

unset <name of your variable> -         removes variable

### Editing .bashrc file to make environmental variables persistent (so they won't dissapear after logging out)

nano .bashrc -                      opening editor with the file

and add at the bottom of the file environmental variable e.g:

export CATSNAME=Bobby

source .bashrc - reload edited configuration file

After all these steps env variable will be persistent after next time we log in

# IP addressess:
Public IP address (associated VM)

### static - (default Azure) stays the same even when VM is restarted
### dynamic - (default AWS) - changes IP every restart of your VM

## Processes
2 types:

### system processes: ps aux
### user processes: ps
Process is like a program that loaded to RAM. If your CPU has 1 core basically CPU can run 1 process at the time. Multicores can do more. OS needs to prioritize processes. Which one most important.

PID - process ID (every process has a process ID)

How to start and kill the process
sleep <number of seconds> - puts terminal to sleep (puts foreground) for certain amount of time

sleep 5000 & - puts terminal to sleep for 5000 sec but in the background

jobs - lists processes running in the background

jobs -l - list of processes with the process ID

kill -1 <process ID> - kills the proecss in the most gentle way (signal 1) - hanging up

kill <process ID> - kill the process, terminating (signal 15) - it will kill parent process and also child processes

kill -9 <process ID> - the harshest way of killing the process. Brute force stubborn process. (signal 9) - it will kill the parent process but child processes will turn up zombie processes that might still running and taking up the memories

ps -ef - shows parent process ID

sudo systemctl - way to control system processes

## Sparta test app
Node js app
port 3000
2 features
a front page (no database if we just want to display front page)
posts page that shows some information from database
Requirements to run Sparta app

### Linux VM - Ubuntu 18.04 LTS
web server - nginx
right version node js - version 12.x works fine (dependency)
app folder
in app folder, run 2 commands:
npm install
node app.js or npm start
getting folder to VM azure
git clone

create a gitrepo - tech241-sparta-app
create a folder "tech241-sparta-app" on your local machine
copy app folder to your local reo
sync with your remote repo on GitHub
SSH into VM & git clone
scp command

will need the private key
path to folder
adminuser@IP address
scp -i ~/.ssh/tech241-neha-az-key -r ./app adminuser@40.120.57.73:/home/adminuser/tech241-sparta-app

rsync











   






