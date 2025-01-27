Instructions for docker toolbox installation
----------------------------------------------
System requirements:
 - windows os >= 7/8/10 home
 - macOS >= 10.8 Mountain Lion

### Download docker app
We are going to use [docker](https://docs.docker.com/toolbox/overview/) app for this lab

Please download the latest release of the docker toolbox [here](https://github.com/docker/toolbox/releases) 

*Please install it to the default path the installer suggests (*e.g.,* C drive for Windows) to avoid volume mounting issues*
  - `pkg` file for MAC
  - `exe` file for windows  

You should see `Docker Quick Start Terminal` and `Kitematic` apps installed.

- Click on the `Docker Quick Start Terminal` icon to start the docker 
  - if you experience unsuccessful startups:
    - windows users: *e.g.,* "error while checking if machine default exists", try restart your computer
    - mac users: *e.g.,* "error on known virtual box bug", 
       - your os probably is more compatible with the docker desktop app, 
         but you can fix this by following the instructions [here](http://biercoff.com/how-to-fix-docker-machine-installation-on-mac-os-x/)

If successful, you will see a whale and a short message with your default machine IP.

To modify the docker-compose.yaml, you will need to do the following step.

1. Enter `echo $UID echo $GID` separately in your terminal. After entering `echo $GID`, you will probably get nothing. If so, you can set GID the same as your UID or just leave it unchanged.

2. Cd to the directory containing this file

3. Run the following command: 

   If you are using x86 CPU (Intel, AMD)

   `DOCKER_ARCH=amd64 docker-compose up`

    If you are using arm CPU (Apple M1/M2/M3)

   `DOCKER_ARCH=arm64 docker-compose up` 

   If you want to avoid typing "DOCKER_ARCH=" every time,

   `export DOCKER_ARCH=<your architecture>" >> ~/.bashrc && source ~/.bashrc`    

4.  Look at output and use the 127.0.0.1 URL (unless you changed the port in the file). Or your default machine IP :8888/lab

**FAQ**

1. If you encounter the error message "The virtual machine 'XXX' has terminated unexpectedly during startup with exit code 1 (0x1)," start by checking if `VirtualBoxVM.exe` can run. Typically, `VirtualBoxVM.exe` is located in the installation directory, such as `C:\Program Files\Oracle\VirtualBox\VirtualBoxVM.exe`. If it cannot run, uninstall the current version of VirtualBox and install the latest version.

   
