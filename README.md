Getting Started with Linux
Linux Directory Tree
Working with File Editors - Done 
Copying, Moving and deleting Files - Done 
Piping and I/O Redirection
Analyzing and Manipulating Files
Managing Users and Groups
Managing Files and Directories Permissions
Managing Sudo Permissions
Basic Linux Networking
Configuring Linux Firewall
Managing Processes
Managing Softwares and Repositories
Managing Disks and Partitions
Archiving and Compressing Files
Task Automation with Cron
-----------------------------------------------------------
Linux for Devops commands 

 hostname             :display the hostname of the machine 
 hostname -i          : Display the ip address iof the machine
 curl ifconfig.me     : Display the public ip/ external ip of the machine 
 man                  : Access manual pages for all linux command  - q out from that command 
 date
 ls                    : list everything 
 mkdir                 : creating file or folder 
 ls -l                 : Show Details and peremissions 
 pwd                   : Working present Direcorty 
 cd ~/Ubuntu           : to gon indise the file 
 touch newfile.txt     : Create a file inside directory 
 clear                 : to clear display 
 cd                    : cd devops/ 
 cd ..                 : to bavk to previous directory cd
 / slash               : is the root directory 
 bin                   : stores binary files 
 cd /root/home/devops/ :  direclty go into that dir 
 rm devops_file.txt    :     to remove the file only can remove files 
 rm -r                 : Recursivley remove the directory and files 
 rmdir                 : to remove directory directly 
 cat demofile.txt      : to show file contents inside file 
 echo " Welcome to Devops " : to print 
 echo redirect to file : echo"Welcome to Devops" >  demofile.txt
 echo " THis is my file" > Myfile.txt : to create without touch command 
 zcat : to zip file for compress it to show content to
 Head Myfile.txt       : to show top upper lines 
 Tail Myfile.txt       : print lower file lines 
 tail -f Myfile.txt    : wait for if any new lines add then print it 
 less myfile.txt       : to show start and end 
 cp demofile.txt Aws/  : to copy file to folder source to destination 
 cp devops/devops_file.txt Aws/ : to copy from devops folder to Aws 
 cp -r Aws/ devops     : to copy whole folder into other folder 
 mv Azure/ linux_for_Iam : To rename to folder or directory 
 wc devops_file.txt    : to cloud charachter , line , words , bytes
 hardlink              : Links are shortcut is the main file deleted but still hardlink will be available 
 Soft Link             : if main file are deleted then softlink also deleted 
 ln                    : stand for link  
 ln -s                 : /root/devops/Aws/devops_file.txt softlink-file 
 ls -ltr               : to listing all details
 ln                    : to crtae hardlink files
 ln devops/Aws/devops_file.txt hardlink-file
 cut                   : to cut the bytes from the filr content 
 cat aws.txt       : cut -b 1-5 aws.txt 
 tee echo "hello" | tee: to create file and echo msg into the file with the help of tee and pipe | 
 : echo "hello" | tee hello.txt
 sort                  : to sort alphabetical 
 clear                 : to clear disply 
 diff demofile.txt hardlink-file  :to check differnce btwn tow files only btwn tow files work  
 VI/vim Editor it is like notepad : vi demofile.txt 
                              : i - for insert mode
							  press Esc :wq to save the files 
 Wget                  : Direct download files from the internet 
 cat/etc/os-release    : get verion of machine 
 ifconfig              : get ip address 
 tar operation         : The linux "tar" stands for the tape archive , which is used by large 
                         number of linux system administrators to deal with tape drives backups ( Compressing + Binding)
						 example : mkdir Devops_file/{aws.txt,azure.txt.gcp.txt}
						 tar -cvf allfiles.tarDevops_file  - zip/tar all files  ( Create verbose file)
						 tae -xvf allfiles.tar             - untar operation   ( Extract verbose file) 
						 
						 

------------------------------------------------------------------------------------------------------------------		
cd ~/Desktop/EC2pemfile/ path for where the key is stored 
Login related 
 - ssh 
1.Public key - already have server side 

2.ptivate key - we need when we trying to connect local to server in Ppk format

----------------------------------------------------------------------------------
Disk Usage 
 - df : define storage occupied or free in your system 
  
 - df -h : show en high level storage 
 - du    : disk utility ( du -v . dot means current directory)
 - ls - la : to show hidden folders 
----------------------------------------------------------------------
*Processes 
 - top : to show all processes are running ( q- for quite) 
 - ps  : to show on which prcess id 
 - fuser : use for perticular file file statem process NAS - Network atached storage 
 - kill  : kill - 9 162( process id) 
 - free  : its show diskspaces 
 - free -h : show in deatilas 
 - nohup : use in application to staore logs in file 
   nohup free -h 
   cat nohup.out 
   nohup df -h : 
   head -n 5 nohup.out
   tail -n 5 nohup.out
   vmstat : vertual memory 
          : vmstat -a : to show active or inactive 
-----------------------------------------------------------------------------------
*Users & File Management* 
 system-level commnds
 1. uname : to check  on which paltform we are running 
 2. uptime : time used 
 3. date : check date 
 4. who  : it show many user logged in this system and when
 5. whoami : curent user 
 6. which : to show application toolsap loacation python, bash, java and version 
           which bash , which java 
 7. id   : to show user id , group id 
 8. sudo  :  super user do 
 9. cd /etc/ : to show list of users 
 10. cat /etc/passwd : show list of users 
 11. shutdown : to stop instance 
 12. reboot : restart 
 13. apt   : apt is a commandline package manager , apt is a application package manager  
             Most used commands:
             list - list packages based on package names
             search - search in package descriptions
             show - show package details
             install - install packages
             reinstall - reinstall packages
             remove - remove packages
             autoremove - automatically remove all unused packages
             update - update list of available packages
             upgrade - upgrade the system by installing/upgrading packages
             full-upgrade - upgrade the system by removing/installing/upgrading packages
             edit-sources - edit the source information file
             satisfy - satisfy dependency strings
			 
	sudo apt install docker.io - apt only search into own syatem package 
	sudo apt-get install docker.io - tp get docker file from internet  
	sudo apt-get update : Upgrade your system 
	Cltr r - 
	
	sudo apt remove docker.io : to remove the package 
14. Yum : is aslo application package manger for (centos) 
15.	dnf  : is also application package manager for (fedora)
16. pacman : is also application package manager for (arch)
17. porage : is also application package manager for (ChromeOS)
18. rpm    : is aslo application package manager for (redhat )
---------------------------------------------------------------------------------- 
	LINUX / UNIX File Structure 

/root - Super user , sudo -i , sudo su 
/etc  - system Configuration file 
/bin  - Executable (i,e, ready to run) program binary files 
/user - user directory 
/temp - temporary file directory 
/dev  - devices files created while installation 
    C:\progam files 
/home - user home directory
/lib  - shared library modlue 
/media - such as cd as rom
/mnt   - temporarary mounted filesystem
/opt   - on application software packages
/proc  -atomatically generated file saystem
/root  - home directory for root user 
/run  - run time program data
/sbin   - system binaries
/srv   - site specific data served by this system 
/sys  - virtual directory provinding info about the system 
/usr  - read only user files
/var  - file that expected to continueosly change 
-------------------------------------------------------------------------------
User realated Command 
 - adduser Devops : add user to the system
 - passwd Devops : change user password 
 - userdel       : delete user account and related files
 - addgroup dev  : add grp to the system 
 - getent group  : show all entry of grps/ users and informatin
 - usermod -a -G group username - add user to the group 
 - delgroup    : remove a group from the system 
 - chage       : change user password expiry informatin
 - sudo relevant files : /etc/passwd(User information) 
                         /etc/shadow(encrypted passwords)
						 /etc/group(group info)
						 /etc/sudoers(configuration for sudo)
------------------------------------------------------------------------------------------
* NETWORKING Commands in Linux *
 ifconfig  :disply and manupulate route network interfaces
 Ping     : check connectivity btwn tow nodes
 Ping     : check connectivity btwn tow nodes 
 netstat  : Display connection information
 ss       : it is a replacement of netstat
 dig google.com  : Query DNS realted information
 nslookup  : fine dns related query 
 route    :  shows and manipulate ip routing table 
 hostname  : to identify a network names
 curl or wget : to doanload files form internet 
 mtr       : combine ping and tracepath into single command 
 whois     : will tell you about the websdites whois 
 ifplugstatus  : tell whether a cable is plugged in or out
 --------------------------------------------------------------------------------------------------
						 
						 



 
