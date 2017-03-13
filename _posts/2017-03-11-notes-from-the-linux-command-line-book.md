---
layout: default
title:  "The Linux Command Line: A complete Introduction"
date:   2017-03-11 16:43:59 +0000
categories: linux development
---

# The Linux Command Line: A complete Introduction

## General Definitions

1. **Shell** - is a program that takes keyboard commands and passes them to the operating system to carry out

2. **Bash** - a GNU Project called *bash* : Bourne Again Shell - Bourne is a call out to Steve Bourne

3. **Terminal Emulator** - GUI access to the shell

4. $ **date** - displays complete date and time

5. $ **cal** - displays current month calendar and highlights current day

6. $ **df** - displays the amount of free space on your disk drives

7. $ **exit** - exits the terminal emulator window

8. $ **ctrl-alt-F1 through F6** - displays the Consoles running behind the scenes

9. $ **pwd** - Print name of current working directory

10. $ **cd** - change directory

11. $ **ls** - List directory contents

12. $ **.** - is the current directory

13. $ **..** - is the parent directory

14. $ **cd** - entered alone takes you back to the home directory

15. $ **cd -** - Changes the working directory to the previous working directory

16. $ **cd ~** - Changes the working directory to the home directory of *username*

17. $ **ls -a** - shows all files including the hidden files that start with dot(.)

18. $ **file** - determines the file type of a file

19. $ **less** - View file contents

20. $ **ls -l** - List with output long format

21. $ **-rw-r--r-- 1 root root**:
	- \- type of file
	- next three characters are access rights for the owner
	- next three characters are for members of the file's group
	- final three characters are for everyone else.
	- 1 \- File's number of hard links.
	- root \- user name of the file's owner
	- root \- name of the group that owns the file

22. **ASCII text** - (pronounced "As-Key") is short for *American Standard Code for Information Interchange*

23. **Less commands** - 

	- page up or b - scroll back one page
	- page down or Spacebar - scroll forward one page
	- G - move to the end of the text file
	- lG or g - move to the beginning of the text file
	- /characters - search forward to the next occurrence of characters
	- n Search for the next occurrence of the previous search
	
24. **LFHS** - Linux Filesystem Hierarchy Standard

25. **symbolic link** ls -l --> yields an l at the beginning with two file names

26. **cp** - Copy files and directories

27. **mv** Move/rename files and directories

28. **mkdir** - Create directories

29. **rm** - Remove file and directories

30. **ln** - Create hard and symbolic links

31.  **wildcards**

	\* Any characters
	? Any single character
	[characters] - any character that is a member of the set *characters*
	[!characters] - any character that is not a member of the set *characters*
	[[:class:]] - Any character that is a member of the specified *class*
		- [:alnum:] - any alpha numeric character
		- [:alpha:] - Any alphabetic character
		- [:digit:] - Any numeral
		- [:lower:] - Any lowercase letter
		- [:upper:] - Any uppercase letter
	- * - all files
	- g* - any file beginning with g

32. *Here is a useful tip:* Whenever you use wildcards with rm (besides carefully checking your typing!), test the wildcard first with ls.  This will let you see the files that will be deleted.  Then press the up arrow key to recall the command and replace the ls with rm

33. **ln** *file* *link* - to make a hard link 

34. **ln** *file* *link* - to make a symbolic link

35. **type** - indicate how a command name is interpreted

36. **which** - Display which executable program will be executed

37. **man** - Display a command's manual page

38. **apropos** - Display a list of appropriate commands

39. **info** - Display a command's info entry

40. **whatis** - Display a command's info entry

41. **alias** - Create an alias for a comman

42.  **Command** can be four things:

	- An executable program
	- A command built into shell itself
	- A shell funciton
	- An alias

43. **type** *command* - will examine the command

44. **which** - display an executable's location

45. **help** - displays quick info about a command

46. **command > filename** - the > puts the command output to a filename

47. **command >> filename** - the >> appends the command output to the end of the filename

48. **2>** - performs the redirection of standard error to the file

49. **Notice** - that the order of the redirections is significant.  The redirection of standard error must always occur after redirecting standard output or it does not work.

50. **/dev/null** location to redirect to in able to throw away the output of the command (this file is called a *bit bucket*

51. **cat** - Concatenate Files

52. **|** - or *pipelines* reads data from standard input and send to standard output 

53. **ls -l dir | less** let's you page through the output of *ls -l dir*

54. **uniq** - removes duplicates from a list

55. **uniq -d** - shows the duplicates from a list

56. **wc** - displays the number of lines, words, and bytes contained in a file

57. **grep** - used to find text patterns within files ( *-i* will ignore case) - *global regular expression print*

58. **head** - shows the first 10 lines of a file, can be adjusted with *-n*

59. **tail** - shows the last 10 lines of a file, can be adjusted with *-n*

60. **echo** - Display a line of text

61. **$((*expression*))** - arithmetic expansion

62. ** \*\*** - Exponentiation

63. **echo Front-{A,B,C}** - will return Front-A Front-B Front-C

64. **mkdir {2009..2011}-1** - will return 2009-1 2010-1 2011-1

65. **printenv | less** - will return a list of variables on the system

66. **ls -l $(which cp) - will return the contents of cp without having to know the location of cp

67. **quoting** - to selectively suppress unwanted expansions

68. **""** - if you place text inside double quotes, all the special characters used by the shell lose their special meaning and are treated as ordinary.  The exceptions are:
	- $
	- \
	- `

69. **' '** - to suppress *all* expansions use *single quotes*

70. **\\** - to suppress a character use \\

71. **Readline** - bash uses a library(a shared collection of routines that different programs can use)

72. **Cursor Movement Commands**:
	- ctrl-A - Move cursor to the beginning of the line
	- ctrl-E - Move cursor to the end of the line
	- ctrl-F - Move cursor forward one character
	- ctrl-B - Move cursor back one character
	- ctrl-L - clear the screen
	
73. **Cutting and Pasting (Killing and Yanking Text**
	- ctrl-D - Delete the character at the cursor location
	- ctrl-T - Transpose (exchange) the character at the cursor location with the one preceding it
	- ctrl-K - Kill text from the cursor location to the end of the line
	- ctrl-U - Kill text from the cursor location to the beginning of the line

74. **set | less** - shows the programmable completions

75. **history | less** - browses history from the beginning

75. **!###** - where ### is the history line item - will repeat the history command

76. **!!** - repeat the last command

77. **id** - Display user identity

78. **chmod** - Change a file's mode

79. **umask** - Set the default file permissions

80. **su** - Run a shell as another user

81. **sudo** - Execute a command as another user

82. **chown** - Change a File's owner

83. **chgrp** - Change a file's group ownership

84. **passwd** - Change a user's password

85. **id** - displays a number called a *user ID*, or *uid*.  The user is assigned a *primary group ID*, or *gid*

86. **ps** - Report a snapshot of current processes

87. **top** - Display tasks

88. **jobs** - List active jobs

89. **bg** - Place a job in the background

90. **fg** - Place a job in the foreground

91. **kill** - Send a signal to a process

92. **killall** - Kill processes by name

93. **shutdown** - Shut down or reboot the system

94. **Processes**

	- Upon startup, the kernel initiates a few processes and launches a program called *init*
	- *init* runs shell scripts located in /etc called "init scripts"
	- these "init scripts" start all the system services
	- many of these services are *daemon programs*
	- programs can launch other programs, expressed in the process scheme as a parents launch childs
	- each process is assigned a *process ID* (PID)
	- PIDs are assigned in ascending order, with *init* always getting PID 1

95. **daemon programs* - programs that sit in the background and do their thing without having any user interface

96. **&** - placed after launching something, this puts the process in the background

97. **printenv** - Print part of all of the environment

98. **set** - Set shell options

99. **export** - Export environment to subsequently executed programs

100. **Two types of shells**
	- *login shells* - is one in which we are prompted for our username and password
	- *non-login* - when we launch a terminal session in the GUI
	
101. **vi** - The first version of *vi* was written in 1976 by Bill Joy, a University of California, Berkeley student who later went on to co-found Sun Microsystems.  vi derives its name from theword visual, because it was intended to allow editing on a video terminal with a moving cursor.

102. **Package Management Systems**:
	- low-level tools -- handle tasks such as installing and removing package files
	- high-level tools -- perform metadata searching and dependency resolution
	
103. **rpm -qa** - lists all packages installed

104. **rpm -q** - determines if a package is installed

105. **dnf info package_name** - get's info about installed and available packages

106. **rpm -qf** - determines which package installed a file

107. **ping** - Send an ICMP ECHO_REQUEST to network hosts

108. **traceroute** - Print the route packets trace to a network host

109. **netstat** - Print network connections, routing tables, interface statistics, masquerade connections, and multicast memberships

110. **ftp** - Internet file transfer program

111. **lftp** - An improve Internet file transfer program

112. **wget** - Non-interactive network downloader

113. **ssh** - OpenSSH SSH client (remote login program)

114. **scp** - Secure copy(remote file copy program)

115. **sftp** - Secure file transfer program

116. **locate** - Find files by name

117. **find** - Search for files in a directory hierarchy

118. **xargs** - Build and execute command lines from standard input

119. **touch** - Change file times

120. **stat** - Display file or filesystem status

121. **rsync** - remote file and directory synchronization

122. **Regular Expressions** - symbolic notations used to identify patterns in text













	
 
