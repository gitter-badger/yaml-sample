# yaml-sample

This repository was created to reproduce the issue [jbeder/yaml-cpp#362](https://github.com/jbeder/yaml-cpp/issues/362) with [jbeder/yaml-cpp](https://github.com/jbeder/yaml-cpp) in  [Arch Linux](https://www.archlinux.org/packages/community/x86_64/yaml-cpp).

## Steps to reproduce the bug

```bash
$ sudo pacman -Sy yaml-cpp
$ git clone https://github.com/branoholy/yaml-sample.git
$ cd yaml-sample && mkdir build && cd build
$ cmake ..
$ make
```
