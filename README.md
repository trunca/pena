## Our buildserver is currently running on: ##

> Ubuntu 16.04.1 LTS (GNU/Linux 3.14.32-xxxx-grs-ipv6-64 x86_64)

## teamBlue 6.1 (based on openPLi) is build using oe-alliance build-environment "4.1" and several git repositories: ##

> [https://github.com/oe-alliance/oe-alliance-core/tree/4.1](https://github.com/oe-alliance/oe-alliance-core/tree/4.1 "OE-Alliance")
> 
> [https://gitlab.com/teamblue/enigma2/tree/master](https://gitlab.com/teamblue/enigma2/tree/master "teamBlue E2")
> 
> [https://gitlab.com/teamblue/skin/tree/master](https://gitlab.com/teamblue/skin/tree/master "teamBlue Skin")

> and a lot more...


----------

# Building Instructions #

1 - Install packages on your buildserver

    sudo apt-get install -y autoconf automake bison bzip2 chrpath coreutils cvs default-jre default-jre-headless diffstat flex g++ gawk gcc gettext git-core gzip help2man htop info java-common libc6-dev libglib2.0-dev libperl4-corelibs-perl libproc-processtable-perl libtool libxml2-utils make ncdu ncurses-bin ncurses-dev patch perl pkg-config po4a python-setuptools quilt sgmltools-lite sshpass subversion swig tar texi2html texinfo wget xsltproc zip zlib1g-dev

----------
2 - Set your shell to /bin/bash

    sudo dpkg-reconfigure dash
    When asked: Install dash as /bin/sh?
    select "NO"

----------
3 - Add user teambluebuilder

    sudo adduser teambluebuilder

----------
4 - Switch to user teambluebuilder

    su teambluebuilder

----------
5 - Switch to home of teambluebuilder

    cd ~

----------
6 - Create folder teamblue

    mkdir -p ~/teamblue

----------
7 - Switch to folder teamblue

    cd teamblue

----------
8 - Clone oe-alliance git

    git clone git://github.com/oe-alliance/build-enviroment.git -b 4.1

----------
9 - Switch to folder build-enviroment

    cd build-enviroment

----------
10 - Update build-enviroment

    make update

----------
11 - Finally you can start building a image

    MACHINE=gbquad4k DISTRO=teamblue make image

