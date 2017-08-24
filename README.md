# FunalabPorts
Local Portfile Repository for FunaLab.

## What is here
* devel/protobuf31-cpp   ... Portfile for [Google Protocol Buffers](https://developers.google.com/protocol-buffers/) v3.1.0
* devel/protobuf3-cpp-devel   ... Portfile for [Google Protocol Buffers](https://developers.google.com/protocol-buffers/) v3.3.0
* python/py-backports-weakref  ... Portfile for [backports.weakref](https://github.com/pjdelport/backports.weakref) v1.0rc1
* python/py-binstruct  ... Portfile for [binstruct](https://pypi.python.org/pypi/binstruct) v1.0.1
* python/py-chainer  ... Portfile for [Chainer](https://chainer.org) v1.24.0
* python/py-chainer2 ... Portfile for [Chainer](https://chainer.org) v2.0.0
* python/py-cpplint  ... Portfile for [CppLint](https://pypi.python.org/pypi/cpplint) v1.3.0
* python/py-cupy     ... Portfile for [CuPy](https://github.com/cupy/cupy) v1.0.0 (w/ patch [#91](https://github.com/cupy/cupy/pull/91))
* python/py-evic     ... Portfile for [Evic](https://github.com/Ban3/python-evic) 176cf0b
* python/py-filelock ... Portfile for [filelock](https://pypi.python.org/pypi/filelock) v2.0.10
* python/py-hidapi   ... Portfile for [cython-hidapi](https://github.com/gbishop/cython-hidapi) 3530c94
* python/py-mock2 ... Portfile for [mock](https://github.com/testing-cabal/mock) v2.0.0
* python/py-protobuf31 ... Portfile for python binding of [Google Protocol Buffers](https://developers.google.com/protocol-buffers/) v3.1.0
* python/py-protobuf3-devel ... Portfile for python binding of [Google Protocol Buffers](https://developers.google.com/protocol-buffers/) v3.3.0
* python/py-sigopt   ... Portfile for [SigOpt Python API](https://github.com/sigopt/sigopt-python) v2.10.0
* python/py-slackweb ... Portfile for [slack-python-webhook](https://github.com/satoshi03/slack-python-webhook) v1.0.5
* science/cufflinks  ... Portfile for [Cufflinks](http://cole-trapnell-lab.github.io/cufflinks/) v2.2.1
* science/libsbml-devel ... Portfile for [libSBML](http://sbml.org/Software/libSBML) v5.13.0 (supports building SBML Level 3 package extensions and language bindings)
* science/libsbmlsim ... Portfile for [libSBMLSim](https://fun.bio.keio.ac.jp/software/libsbmlsim/) v1.3.0 (supports building with language bindings)
* science/samtools0  ... Portfile for [samtools](http://samtools.sourceforge.net) v0.1.19 (because [cufflinks requires samtools-0.x](https://github.com/cole-trapnell-lab/cufflinks/issues/14))

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

py-chainer @1.24.0 (python)         # <== OK!
    A flexible framework of neural networks

py-chainer2 @2.0.0 (python)         # <== OK!
    A flexible framework of neural networks

py27-chainer @1.1.1 (python)
    A flexible framework of neural networks

py27-chainer @1.24.0 (python)       # <== OK!
    A flexible framework of neural networks

py27-chainer2 @2.0.0 (python)       # <== OK!
    A flexible framework of neural networks

py34-chainer @1.1.1 (python)
    A flexible framework of neural networks

py34-chainer @1.24.0 (python)       # <== OK!
    A flexible framework of neural networks

py35-chainer2 @2.0.0 (python)       # <== OK!
    A flexible framework of neural networks

py36-chainer2 @2.0.0 (python)       # <== OK!
    A flexible framework of neural networks

Found 10 ports.
```

### Install py-chainer (1.24.0) by MacPorts
```sh
% sudo port install py27-chainer
```
or
```sh
% sudo port upgrade py27-chainer
```

### Install py-chainer (2.0.0) by MacPorts
```sh
% sudo port install py27-chainer2
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
