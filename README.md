# FunalabPorts
Local Portfile Repository for FunaLab.

## What is here
* python/py-chainer  ... Portfile for chainer-1.19.0
* python/py-filelock ... Portfile for filelock-2.0.7
* python/py-cpplint  ... Portfile for CppLint
* science/cufflinks  ... Portfile for Cufflinks-2.2.1
* science/libsbml-devel ... Portfile for libSBML-5.13.0 (supports building SBML Level 3 package extensions and language bindings)
* science/libsbmlsim ... Portfile for libSBMLSim-1.3.0 (supports building with language bindings)
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

py-chainer @1.19.0 (python)         # <== OK!
    A flexible framework of neural networks

py27-chainer @1.1.1 (python)
    A flexible framework of neural networks

py27-chainer @1.19.0 (python)       # <== OK!
    A flexible framework of neural networks

py34-chainer @1.1.1 (python)
    A flexible framework of neural networks

py34-chainer @1.19.0 (python)       # <== OK!
    A flexible framework of neural networks

Found 6 ports.
```

### Install py-chainer (1.19.0) by MacPorts
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

### Install libSBML (5.13.0) with python binding and SBML Level 3 package extensions by MacPorts
```sh
% sudo port install libsbml-devel +spatial +python27
```

### Install libSBMLSim (1.3.0) with Java, python, ruby and C# bindings by MacPorts
```sh
% sudo port install libsbmlsim +java +python27 +ruby +csharp
```

Have fun!
