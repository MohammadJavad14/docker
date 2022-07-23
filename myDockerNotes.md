# Running Linux
	- Go to docker hub
	- Search for ubuntu
	- copy the command: docker pull ubuntu
	- The best is to run: docker run ubuntu

	- docker ps: shows the list of running processes or container
	- docker ps -a: also shows the stopped container
	- docker run -it ubuntu: for running an image interactively

    - Linux commands:
        - echo
        - whoami
        - echo $0
        - history
        
# Managing Packages
    - apt: advanced package tool
    - apt-get
    - nano: basic text editor for linux
    - apt install nano
    - apt update
    - again: apt install nano
    - apt remove nano

# Navigating the File System
    - pwd: print working directory
    - ls: list
    - ls -a: list all the files also hidden files
    - ls -1: list one file per line
    - ls -l: list with long listing
    - cd: change directory
    - cd /foo: absolute path
    - cd foo: relative path
    - cd ..: go back one step
    - ls /foo or ls foo: show the list of file of directory inside the path
    - cd ~: navigate to home directory

# Manipulating Files and Directories
    - mkdir test: making a new directory called test
    - mv test docker: rename the test directory to docker
    - touch hello.txt: create a new file
    - touch file1.txt file2.txt: creating multiple files in one command
    - mv hello.txt hello-docker.txt: rename the hello.txt to hello-docker.txt
    - mv hello.txt /etc: move the hello.txt file to /etc directory
    - rm file1.txt file2.txt: remove one or more file
    - rm file*: remove all file which starts with file
    - rm docker/: getting an error "docker/" is a directory
    - rm -r docker/: remove a directory and all files inside it

# Editing and Viewing Files
    - apt install nano
    - nano file.txt: open the file and do some thing
    - ^X: for exiting
    - cat file.txt: to see the content of this file usually used for displaying short file
    - more file.txt: to see the long files
        - press space for go to next page
        - press enter go one line down
        - there is no way to go up
        - for that you can use less
        - to exit press q
    - apt install less
        - use up and down arrow 
        - press space for go to next page
        - press enter go one line down
        - to exit press q
    - head -n 5 file.txt: shows the first 5 line of the file
    - tail -n 5 file.txt: shows the last 5 line of the file
# Redirection
    - cat file1.txt > file2.txt: redirect the output from the screen to file2.txt
    - <: less than operator used for redirect the input  
# Searching for Text
    - grep hello file.txt: global regular expression print, search for word hello in file.txt
    - grep -i: removes case sensitivity from the search
    - grep -i hello file1.txt file2.txt: search in multiple files
    - grep -i hello file*: search all files with this pattern
    - grep -i -r hello /foo: search for directory and all its subdirectory
    - grep -ir hello /foo: combines the two -i and -r options
# Finding Files and Directories
    - find: show all the files and directories recessively
    - find /foo: show all the files in the path
    - find /foo -type d: only show the directories in the path
    - find /foo -type f: only show the files in the path
    - find /foo -type f -name "bar*": filtering results by name
    - find /foo -type f -iname "bar*": filtering results by name without case sensitivity
# Chaining Commands
    - mkdir test; cd test; echo done
    - cd ..
    - repeat last command: result an error and the two command after the first will execute
    - mkdir test && cd test && echo done: to stop execute after an error
    - mkdir test || echo "directory exists": if the first command executed the second one will not
    - ls /bin | less: piping, run the fist command and send the result for second command
    - mkdir hello;\
      cd hello;\
      echo done;
      : splitting a command in multiple line
# Environment Variables
    - printenv: print all environment variables
    - printenv PATH: print the value of PATH variable
    - echo $PATH: print the value of PATH 
    - export DB_USER=mohammad: set an environment variable. it is only available in this terminal session
    - echo DB_USER=mohammad >> .bashrc: appending this line to .bashrc file, it is just available in next terminal session
    - source .bashrc: for reloading .bashrc if we are in home dir
    - source ~./bashrc: if we are not in home dir
# Managing Processes
    - ps: show the running processes 
    - kill process id: killing the process
# Managing Users
    - useradd -m username: create the user's home directory
    - cat /etc/passwd: to see the user info
    - usermod -s /bin/bash john: modify the john's shell
    - cat /etc/shadow: shows the passwords
    - docker exec -it -u john ps_id bash: login as john
    - userdel john: delete the use john
    - adduser bob: more interactive than the useradd 