# Download and Install Poplog for Linux

## Recommended: Install via Standard Package (*.deb or *.rpm)

For most Linux users the best way to install Poplog is using a standard package. 
 - We host these on our page on [OpenBuildService](https://software.opensuse.org/download.html?project=home:getpoplog&package=poplog).
 - We recommend using the "Add repository and install manually" links for your distribution.
 - Only use the 'Grab binary packages directly' link if you know what you are doing.

### Worked Example for Centos 8 User

1. In a web browser navigate to [link](https://software.opensuse.org/download.html?project=home:getpoplog&package=poplog)
2. Click on Centos logo
3. Click on "Add repository and install manually"
4. Find the best match for 'Centos 8' and enter the instructions at a terminal
```sh
cd /etc/yum.repos.d/
wget https://download.opensuse.org/repositories/home:getpoplog/CentOS_8/home:getpoplog.repo
yum install poplog
```

### Worked Example for Ubuntu 20.04 User

1. In a web browser navigate to [link](https://software.opensuse.org/download.html?project=home:getpoplog&package=poplog)
2. Click on Ubuntu logo
3. Click on "Add repository and install manually"
4. Find the best match for 'Ubuntu 20.04' and enter the instructions at a terminal
```sh
echo 'deb http://download.opensuse.org/repositories/home:/getpoplog/xUbuntu_20.04/ /' | sudo tee /etc/apt/sources.list.d/home:getpoplog.list
curl -fsSL https://download.opensuse.org/repositories/home:getpoplog/xUbuntu_20.04/Release.key | gpg --dearmor | sudo tee /etc/apt/trusted.gpg.d/home_getpoplog.gpg > /dev/null
sudo apt update
sudo apt install poplog
```

## Alternative for all Linux users - AppImage

[AppImages](https://appimage.org/) are entire applications packaged into a single, self-contained executable file. There's no installation required, although you may prefer to put the executable somewhere on your `$PATH`. On each release we package up Poplog as an AppImage and this is particularly suitable for people who want to just kick the tyres and check things out before they install Poplog or just for for keeping old versions of Poplog to hand.

### Worked Example of Using the Poplog AppImage

1. [Download the AppImage](https://github.com/GetPoplog/Seed/releases/download/v0.2.0-beta/Poplog-x86_64.AppImage) from the release pages of the GetPoplog Seed repository.
2. At a terminal type:

```sh
$ cd ~/Downloads                        # Navigate to your local downloads folder   
$ chmod a+x Poplog-x86_64.AppImage      # Ensure it is executable
$ ./Poplog-x86_64.AppImage --help       # Try running it!
Usage: poplog [action-word] [options] [file(s)]
...
```

## Build and Install from Source

If you have a need for a specialised installation and have some experience on the command line then [this page](BuildAndInstallFromSource.html) may be of interest.

## Checking Poplog is correctly installed

Once you have installed Poplog, try starting it up and checking that it works. At the terminal, type `poplog`:
```
$ poplog

Sussex Poplog (Version 16.0001 Mon May 17 13:04:57 EDT 2021)
Copyright (c) 1982-1999 University of Sussex. All rights reserved.

Setpop
: 'Hello, World!' =>                                  
** Hello, World! 
: 
```

To exit, type Ctrl-D (the 'd' key with control held down) or type the command `sysexit();` which will cause Poplog to immediately exit.
