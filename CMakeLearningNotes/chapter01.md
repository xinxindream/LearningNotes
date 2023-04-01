# CMake概述
## 一、CMake简介
### 1. 什么是CMake？
CMake（cross platform make），跨平台编译构建工具，相当于一个编译构建脚本

### 2. 为什么使用CMake？
当项目涉及多个单元模块，涉及多个源文件以及资源，逐个编译以及链接库将十分复杂，CMake可以解决

## 二、CMake下载与安装
由于再linux上使用CMake居多，故只有Linux上下载安装教程

### 1. Linux下载CMake源码（3.26.2）
1. CMake官网获取CMake源码安装包（Binary distributions）
> 官网地址：https://cmake.org/download/
- Binary distributions: 二进制文件发行版，解压直接使用
- Source distributions: 需要自己去编译安装

2. 下载至自己知道的路径下
> 本人安装包存放地址：/root/Downloads/softwares

3. 下载源码命令行（我的是aarch64）：
> wget -P /root/Downloads/softwares https://github.com/Kitware/CMake/releases/download/v3.26.2/cmake-3.26.2-linux-aarch64.tar.gz


### 2. Linux安装CMake（以下步骤需要sudo权限）
1. 解压至CMake安装目录
> tar -zxvf cmake-3.26.2-linux-aarch64.tar.gz -C /usr/local/devtools/

2. 重命名
> mv cmake-3.26.2-linux-aarch64 cmake-3.26.2

### 3. Linux配置CMake
1. vim打开/etc/profile
2. 末尾添加
> export CMAKE_HOME=/usr/local/devtools/cmake-3.26.2/bin
export PATH=$CMAKE_HOME:$PATH
3. 更新profile
> source /etc/profile
4. 软链接，全局cmake生效
> ln -sf /usr/local/devtools/cmake-3.26.2/bin/* /usr/bin/

### 4. Linux卸载CMake
> rm -rf 安装目录 