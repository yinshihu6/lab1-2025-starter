# Due date: Feb 17, 2025 at 11:59 P.M.

# Lab 1: Neural Network Profiling and Inference

In this problem set, we will cover the basics of running neural network inference
in [PyTorch](https://pytorch.org/). PyTorch is a very popular
neural network framework maintained by Facebook, and it is used by a multitude of
researchers worldwide. Our goal will be to prototype networks for two classic
tasks: the MNIST digit recognition task and the ImageNet object classification
task. We will go through basic network inspection, inference and training in
these questions. Since the eventual goal of this course is to design hardware
for neural network inference, an important focus of this problem set will be to
develop a quantitative understanding of the computation involved in these tasks.

For this lab and forward, we will be using Docker to run the code, and Git to distribute the labs. Please read the instructions below and setup your Docker and Git properly, as this setup will be required for the future labs as well. Note that most of the labs do not require GPU support, and the Docker image we provide does not support GPU operations. Please reach out to the instructors in case you cannot setup your enviornments for the labs. 

After you successfully launch a Jupyter notebook following the instructions below, please find details of this lab in [workspace/lab1/README.md](./workspace/lab1/README.md).

## Installing Docker

First, we need to setup the [docker](https://docs.docker.com/get-started/) to run the code. We provide you two sets of instructions for installing docker. You can decide which app to install according to your operating system.

- MAC:

  - If you have macOS 10.13.0 High Sierra or higher, please follow instructions in `docker-desktop-readme.md`
  - otherwise, follow instructions in `docker-toolbox-readme.md`

- Windows:

  - If you have windows 10 pro with enterprise/education (most of you should not have this OS, and have windows 10 home instead. Please check carefully), please follow instructions in `docker-desktop-readme.md`
  - otherwise, follow instructions in `docker-toolbox-readme.md`

- Windows Subsystem for Linux 2 (WSL2):

  - If you have windows 10 with version 1903 or higher, you can install [WSL2](https://docs.microsoft.com/en-us/windows/wsl/install-win10)
  - You can install Docker Desktop with WSL2, and use Linux workspaces. Follow instructions [here](https://docs.docker.com/docker-for-windows/wsl/)

- Linux:

  - If you have Linux distributions, such as Ubuntu, please check if Docker supports your distribution and architecture from [here](https://docs.docker.com/engine/install/). Examples of supported distributions are: 
    - [Ubuntu](https://docs.docker.com/engine/install/ubuntu/)
    - [CentOS](https://docs.docker.com/engine/install/centos/)
    - [Debian](https://docs.docker.com/engine/install/debian/)
    - [Fedora](https://docs.docker.com/engine/install/fedora/)


## Git Basics

Since we will be using Git to distribute the labs, you should also install `git` - however, if you are using Linux distributions or WSL2, `git` should either be already installed or available in your relevant package manager. On Mac OSX, the simplest way to install git is to try running git on your terminal which will prompt you to install Xcode Command Line Tools if they are not already installed. On Windows (without WSL2), you can download [Github Desktop](https://desktop.github.com/). Below are basic git command examples:

[//]: # "TODO: change this url"
Clone this repository (replace `username` with your GitHub username)
```
git clone git@github.com:deep-learning-hardware-MIT/lab1-2023-username.git
```
*In case you are using WSL2, note that it is recommended to clone this repository to Linux filesystems.*

*In case you are using Windows, note that you should clone this repository to somewhere in C drive because docker doesn't play well with other drives.*

Commit and push back to this repository after you finish the assignment. You can commit and push multiple times, and we will only check your latest push. Please check if commit and push work correctly before starting the lab. You can check it by changing your name in each Jupyter notebook, then running commit/push. Check if this repository page has been updated properly according to your changes. 
```
git status
git config --global user.email "you@example.com"
git config --global user.name "Your Name"
git commit -a -m '<Short descriptive commit message>'
git push
```

## Starting Docker

Now, we will start Docker, and launch a Jupyter notebook. Follow the instruction
in `docker-compmose.yaml` file to change the `USER_UID` and set environment variable `DOCKER_ARCH`.
You can run `docker-compose up` from the directory containing `docker-compmose.yaml` file, and you will see a Jupyter server running. Launch the Internet browser of your choice, and access the Jupyter server (default will be `localhost:8888`, but may differ based on your docker configuration). For example, from your docker terminal:
```
cd <your-repository-directory>
export DOCKER_ARCH=amd64

# If you are using arm CPU (Apple M1/M2), 
# export DOCKER_ARCH=arm64 

docker-compose up
```

If your docker configuration changes the default IP address, then use that address when accessing the Jupyter server. If you want to avoid setting `DOCKER_ARCH` everytime, you can permanently add `DOCKER_ARCH=<your architecture>` into your `.bashrc` or `.zshrc`.

## Submission
After finishing all of the provided notebooks, please run `make commmit` to
submit your code. Check your submission on the GitHub website and ensure that
all notebooks have all cells run and all outputs visible. Additionally, ensure
that the `answers.yaml` file in the website matches the answers you have in your
notebooks. If either the notebooks or the `answers.yaml` file are not up to
date, you may lose points or receive a zero for the assignment.

FAILURE TO FOLLOW THESE INSTRUCTIONS WILL RESULT IN YOU RECEIVING A ZERO FOR THE
ASSIGNMENT. 
