# Build and Install Poplog from Source

You may prefer to build and install Poplog from source. This is only really suitable for people with some experience with using Linux at the command line - but it does give a few extra options.

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

This is the most flexible installation method and there are many options available that are not described here that allow you to customise Poplog. [The Makefile](https://github.com/GetPoplog/Seed/blob/main/Makefile) is well-commented so please read that file to learn more.