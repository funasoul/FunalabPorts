# FunalabPorts
Local Portfile Repository for FunaLab.

## What is here
* python/py-chainer  ... Portfile for chainer-1.18.0
* python/py-filelock ... Portfile for filelock-2.0.7
* science/cufflinks  ... Portfile for Cufflinks-2.2.1
* science/samtools0  ... Portfile for samtools-0.1.19 (because [cufflinks requires samtools-0.x](https://github.com/cole-trapnell-lab/cufflinks/issues/14))

## How to use
### Use this project as your Local Portfile Repository
At first, clone this project.
```sh
% mkdir -p ~/git
% cd ~/git
% git clone https://github.com/funasoul/FunalabPorts
% cd FunalabPorts/
% portindex
```
Then, add this local repo. to your MacPorts.
```sh
% sudo chmod 644 /opt/local/etc/macports/sources.conf
% sudo vim /opt/local/etc/macports/sources.conf
# Add this following line (please change "yourname" as your username)
file:///Users/yourname/git/FunalabPorts
% sudo chmod a-w /opt/local/etc/macports/sources.conf
```

### Test whether your Macports can find your local repo.
```sh
% port search chainer
py-chainer @1.1.1 (python)
    A flexible framework of neural networks

py-chainer @1.18.0 (python)         # <== OK!
    A flexible framework of neural networks

py27-chainer @1.1.1 (python)
    A flexible framework of neural networks

py27-chainer @1.18.0 (python)       # <== OK!
    A flexible framework of neural networks

py34-chainer @1.1.1 (python)
    A flexible framework of neural networks

py34-chainer @1.18.0 (python)       # <== OK!
    A flexible framework of neural networks

Found 6 ports.
```

### Install py-chainer (1.18.0) by MacPorts
```sh
% sudo port install py27-chainer
```
or
```sh
% sudo port upgrade py27-chainer
```

### Install cufflinks (2.2.1) by MacPorts
```sh
% sudo port install cufflinks
```
or
```sh
% sudo port upgrade cufflinks
```
Have fun!
