Bootstrap: docker
From: ubuntu:16.04

IncludeCmd: yes

%runscript
    exec /bin/bash "$@"

%post
    /usr/bin/apt-get update && /usr/bin/apt-get -y upgrade
    /usr/bin/apt-get -y install module-init-tools
    /usr/bin/apt-get update --fix-missing
    /usr/bin/apt-get install -y --no-install-recommends apt-utils
    /usr/bin/apt-get install -y build-essential git vim wget curl ncdu toilet figlet cowsay zsh
    wget https://github.com/emcrisostomo/fswatch/releases/download/1.9.3/fswatch-1.9.3.tar.gz && \
      tar -zxvf fswatch-1.9.3.tar.gz && \
      cd fswatch-1.9.3/ && \
      ./configure && make && make install && ldconfig

    # Make folders for CBD HPC cluster
    if [ ! -d /images ]; then mkdir /images; fi
    if [ ! -d /projects ]; then mkdir /containers; fi
    if [ ! -d /containers ]; then mkdir /containers; fi
    if [ ! -d /share ]; then mkdir /share; fi
    if [ ! -d /scratch ]; then mkdir /scratch; fi
