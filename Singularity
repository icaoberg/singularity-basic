Bootstrap: docker
From: debian:latest

IncludeCmd: yes

%labels
  Maintainer icaoberg AT alumni DOT cmu DOT edu
  Version v1.0

%runscript
      exec /usr/bin/python "$@"

%post
    /usr/bin/apt-get update && /usr/bin/apt-get -y upgrade
    /usr/bin/apt-get -y install module-init-tools
    /usr/bin/apt-get update --fix-missing
    /usr/bin/apt-get install -y --no-install-recommends apt-utils
    /usr/bin/apt-get install -y build-essential && \
      git && \
      vim && \
      wget curl && \
      ncdu && \
      toilet figlet cowsay &&
      zsh && \
      pandoc && \
      libtiff5 && \
      graphviz

    # Install fswatch
    wget https://github.com/emcrisostomo/fswatch/releases/download/1.9.3/fswatch-1.9.3.tar.gz && \
      tar -zxvf fswatch-1.9.3.tar.gz && \
      cd fswatch-1.9.3/ && \
      ./configure && make && make install && ldconfig && cd .. && \
      rm -fv fswatch-1.9.3.tar.gz && \
      rm -rfv fswatch-1.9.3

    # Install TaskWarrior
    wget -nc https://taskwarrior.org/download/task-2.5.1.tar.gz && \
      tar -xzvf task-2.5.1.tar.gz && \
      cd task-2.5.1 && \
      cmake -DCMAKE_BUILD_TYPE=release . && \
      make && make install && cd .. && \
      rm -fv task-2.5.1.tar.gz && rm -rfv task-2.5.1

    # Install TimeWarrior
    wget -nc  https://taskwarrior.org/download/timew-1.1.1.tar.gz && \
      tar xzf timew-1.1.1.tar.gz && \
      rm -fv timew-1.1.1.tar.gz && \
      cd timew-1.1.1 && \
      cmake -DCMAKE_BUILD_TYPE=release . && \
      make && \
      make install && \
      cd .. && \
      rm -rfv timew-1.1.1 

    # Install todo.txt
    wget https://github.com/todotxt/todo.txt-cli/archive/master.zip && \
      unzip master.zip && \
      cd master && \
      make && make install && \
      cd .. && rm -rfv master

    # Make folders for CBD HPC cluster
    if [ ! -d /images ]; then mkdir /images; fi
    if [ ! -d /projects ]; then mkdir /projects; fi
    if [ ! -d /containers ]; then mkdir /containers; fi
    if [ ! -d /share ]; then mkdir /share; fi
    if [ ! -d /scratch ]; then mkdir /scratch; fi

################### TOILET ###################
%appenv toilet
    BEST_APP=toilet
    export BEST_APP

%apphelp toilet
    Fore more information about pdftex please visit
 
    * http://caca.zoy.org/wiki/toilet

%apprun toilet
    toilet "$@"
    
################### VIM ###################
%appenv vim
    BEST_APP=vim
    export BEST_APP

%apphelp vim
    Fore more information about pdftex please visit
 
    * https://www.vim.org/

%apprun vim
    vim "$@"
