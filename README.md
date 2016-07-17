# yaml-sample

[![Join the chat at https://gitter.im/branoholy/yaml-sample](https://badges.gitter.im/branoholy/yaml-sample.svg)](https://gitter.im/branoholy/yaml-sample?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

This repository was created to reproduce the issue [jbeder/yaml-cpp#362](https://github.com/jbeder/yaml-cpp/issues/362) with [jbeder/yaml-cpp](https://github.com/jbeder/yaml-cpp) in  [Arch Linux](https://www.archlinux.org/packages/community/x86_64/yaml-cpp).

### Steps to reproduce the bug

```bash
$ sudo pacman -Sy yaml-cpp
$ git clone https://github.com/branoholy/yaml-sample.git
$ cd yaml-sample && mkdir build && cd build
$ cmake ..
$ make
```

### Output of `make`

```
Scanning dependencies of target yaml-sample
[ 50%] Building CXX object CMakeFiles/yaml-sample.dir/src/main.cpp.o
make[2]: *** No rule to make target '/build/yaml-cpp/src/yaml-cpp-release-0.5.3/libyaml-cpp.so.0.5.3', needed by 'yaml-sample'.  Stop.
CMakeFiles/Makefile2:67: recipe for target 'CMakeFiles/yaml-sample.dir/all' failed
make[1]: *** [CMakeFiles/yaml-sample.dir/all] Error 2
Makefile:83: recipe for target 'all' failed
make: *** [all] Error 2
```
