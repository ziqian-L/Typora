使用系统版本：WSL——Ubuntu 20.04.6 LTS

在官方的[github](https://github.com/milkv-duo/duo-buildroot-sdk)上按照教程安装时，由于我的Ubuntu版本比较低，所以最多只能安装Cmake 3.16.3，而编译需要使用的Cmake版本最低为Cmake3.16.5

在使用官方的方法后，死活安装不上

在参考了https://blog.csdn.net/qq_34629975/article/details/86569023这篇文章后，发现需要在 `sudo`后面加上一个·`sh`

官方的指令是这样的

```
wget https://github.com/Kitware/CMake/releases/download/v3.26.4/cmake-3.26.4-linux-x86_64.sh
chmod +x cmake-3.26.4-linux-x86_64.sh
sudo ./cmake-3.26.4-linux-x86_64.sh --skip-license --prefix=/usr/local/
```

改后的指令是这样的

```
wget https://github.com/Kitware/CMake/releases/download/v3.26.4/cmake-3.26.4-linux-x86_64.sh
chmod +x cmake-3.26.4-linux-x86_64.sh
sudo sh ./cmake-3.26.4-linux-x86_64.sh --skip-license --prefix=/usr/local/
```

成功

```\
CMake Installer Version: 3.26.4, Copyright (c) Kitware
This is a self-extracting archive.
The archive will be extracted to: /usr/local/

Using target directory: /usr/local/
Extracting, please wait...

Unpacking finished successfully
```

最后再使用

```
cmake --version
```

查看Cmake版本

```
cmake version 3.26.4

CMake suite maintained and supported by Kitware (kitware.com/cmake).
```

