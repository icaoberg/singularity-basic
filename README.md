# singularity-basic
[![https://www.singularity-hub.org/static/img/hosted-singularity--hub-%23e32929.svg](https://www.singularity-hub.org/static/img/hosted-singularity--hub-%23e32929.svg)](https://singularity-hub.org/collections/2237)
![Release](https://img.shields.io/badge/release-prealpha-red.svg)
[![Build Status](https://travis-ci.org/icaoberg/singularity-basic.svg?branch=master)](https://travis-ci.org/icaoberg/singularity-basic)
[![GitHub issues](https://img.shields.io/github/issues/icaoberg/singularity-basic.svg)](https://github.com/icaoberg/singularity-basic/issues)
[![GitHub forks](https://img.shields.io/github/forks/icaoberg/singularity-basic.svg)](https://github.com/icaoberg/singularity-basic/network)
[![GitHub stars](https://img.shields.io/github/stars/icaoberg/singularity-basic.svg)](https://github.com/icaoberg/singularity-basic/stargazers)
[![GitHub license](https://img.shields.io/badge/license-GPLv3-blue.svg)](https://www.gnu.org/licenses/quick-guide-gplv3.en.html)

This is the Singularity definition of my personal container that I use while supporting the [Computational Biology Department](http://www.cbd.cmu.edu)'s [HPC](https://en.wikipedia.org/wiki/Supercomputer) [cluster](https://en.wikipedia.org/wiki/Computer_cluster).

The image has been tested on

```
➜  singularity --version
2.6.0-dist
```

## Installed packages
These are the packages

* [cowsay](https://en.wikipedia.org/wiki/Cowsay)
* [Figlet](http://www.figlet.org/)
* [fswatch](https://github.com/emcrisostomo/fswatch)
* [git](https://git-scm.com/)
* [graphviz](https://www.graphviz.org/)
* [htop](http://hisham.hm/htop/)
* [libtiff5](https://packages.debian.org/jessie/libtiff5)
* [pandoc](https://pandoc.org/)
* [TaskWarrior](https://taskwarrior.org/)
* [TimeWarrior](https://timewarrior.net/)
* [toilet](http://caca.zoy.org/wiki/toilet)
* [todo.txt](http://todotxt.org/)
* [tmux](https://github.com/tmux/tmux)
* [vim](https://www.vim.org/)
* [zsh](https://www.zsh.org/)

## Pull image from Singularity Hub

```
singularity pull shub://icaoberg/singularity-basic
singularity pull --name customname.img shub://icaoberg/singularity-basic
singularity pull --commit shub://icaoberg/singularity-basic
singularity pull --hash shub://icaoberg/singularity-basic
```

## Disclaimer

[![Wold you buy me some coffee?](https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png)](https://www.buymeacoffee.com/icaoberg)

I am nothing but a humble programmer creating and sharing this container.

---
[![CBD](http://www.cbd.cmu.edu/wp-content/uploads/2017/07/wordpress-default.png)](http://www.cbd.cmu.edu)

Copyleft © 2019 [icaoberg](http://www.andrew.cmu.edu/~icaoberg) at the [Computational Biology Department](http://www.cbd.cmu.edu) in [Carnegie Mellon University](http://www.cmu.edu)
