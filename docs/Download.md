# Download and Install Poplog for Linux

Work in progress ... please call back soon

## Recommended: Install via Standard Package (*.deb or *.rpm)

 - For most Linux users the best way to install Poplog is using a standard package. 
 - We host these on our page on [OpenBuildService](https://docs.appimage.org/packaging-guide/hosted-services/opensuse-build-service.html).
 - From there you can either:
   1. Add the OBS repo to your list of sources and then use apt or dnf to install Poplog. You'll find instructions for this are given when you click on the page.
   2. Alternatively you can download the package for your OS (`*.deb` or `*.rpm`). After that you will need to install using `apt` or `dnf`.

### Worked Example for Centos User

1. In a web browser navigate to [link](https://docs.appimage.org/packaging-guide/hosted-services/opensuse-build-service.html)
2. Click on Centos logo
3. Click on Grab binary packages directly & identify the closest match to your OS
4. Download [poplog-0.2.0-2.1.src.rpm](https://download.opensuse.org/repositories/home:/getpoplog/CentOS_8/src/poplog-0.2.0-2.1.src.rpm)
5. At a terminal type
```sh
$ cd ~/Downloads     # Navigate to the downloads folder
$ dnf install poplog-0.2.0-2.1.src.rpm
```

### Worked Example for Ubuntu User

1. In a web browser navigate to [link](https://docs.appimage.org/packaging-guide/hosted-services/opensuse-build-service.html)
2. Click on Ubuntu logo
3. Click on Grab binary packages directly & identify the closest match to your OS
4. Download [poplog_0.2.0-1_amd64.deb](https://download.opensuse.org/repositories/home:/getpoplog/xUbuntu_20.04/amd64/poplog_0.2.0-1_amd64.deb) 
5. At a terminal type
```sh
$ cd ~/Downloads     # Navigate to the downloads folder
$ apt install ./poplog_0.2.0-1_amd64.deb  # The leading './' tells apt to use a local file
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

This poplog "commander" runs various Poplog commands (pop11, prolog, etc) with
the special environment variables and $PATH they require. The 'action-word'
determines what command is actually invoked.
...
```

## Build and Install from Source

You may prefer to build and install Poplog from source. This is quite 
straightforward.


```sh
$ git clone https://github.com/GetPoplog/Seed.git
$ cd Seed
```

Now you need to install the appropriate build tools for your distribution. We
have created a handy shortcut for this.
```sh
$ make help-jumpstart
$ make help-jumpstart
# Jumpstarts are targets that install the dependencies for a particular
# Linux distribution. Installing dependencies are not part of a normal
# build process and they are provided as a convenience to admins.
# These will need to be run with sudo e.g.
#	sudo make jumpstart-debian
#
# Valid targets are:
#   jumpstart-debian - installs the packages a Debian system needs
#   jumpstart-ubuntu - installs the packages an Ubuntu system needs
#   jumpstart-fedora - installs the packages a Fedora system needs.
#   jumpstart-rocky - installs the packages a Rocky Linux system needs.
#   jumpstart-centos - installs the packages a Rocky Linux system needs.
#   jumpstart-opensuse-leap - installs the packages a openSUSE Leap system needs.
```

Let's suppose we are on Ubuntu Linux, then we would continue like this:
```sh
$ make jumpstart-ubuntu    # Install all the build tools needed for Ubuntu
$ make build               # Build Poplog
$ sudo make install        # Install Poplog in /usr/local/poplog
```

This is the most flexible installation method but is really only suitable for Linux users with a bit of experience in managing their own systems. The advantage is that there are many options available that are not described here that allow you to customise Poplog. [The Makefile](https://github.com/GetPoplog/Seed/blob/main/Makefile) is well- commented so please read that file to learn more.

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
