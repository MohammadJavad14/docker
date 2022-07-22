- # Running Linux
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
        
- # Managing Packages
    - apt: advanced package tool
    - apt-get
    - nano: basic text editor for linux
    - apt install nano
    - apt update
    - again: apt install nano
    - apt remove nano

- # Navigating the File System
    - pwd: print working directory
    - ls: list
    - ls -1: list one file per line
    - ls -l: list with long listing
    - cd: change directory
    - cd /foo: absolute path
    - cd foo: relative path
    - cd ..: go back one step
    - ls /foo or ls foo: show the list of file of directory inside the path
    - cd ~: navigate to home directory