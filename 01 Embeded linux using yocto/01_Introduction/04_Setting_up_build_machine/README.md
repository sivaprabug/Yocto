# Setting up Build Machine

## Prerequisites

1. 50 Gbytes of free disk space

2. Runs a supported Linux distribution (i.e. recent releases of Fedora, openSUSE, CentOS, Debian, or Ubuntu). 

3. 

- Git 1.8.3.1 or greater
- tar 1.27 or greater
- Python 3.4.0 or greater.

Packages and package installation vary depending on your development system.

(*) Install the required packages for Yocto to Work from
        https://www.yoctoproject.org/docs/latest/ref-manual/ref-manual.html#ubuntu-packages

$ sudo apt-get install gawk wget git-core diffstat unzip texinfo gcc-multilib \
    build-essential chrpath socat cpio python python3 python3-pip python3-pexpect \
    xz-utils debianutils iputils-ping python3-git python3-jinja2 libegl1-mesa libsdl1.2-dev \
    pylint3 xterm