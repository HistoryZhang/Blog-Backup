---
layout: post
title: "iOS合并真机和模拟器静态库"
date: 2014-08-03 10:48:38 +0800
comments: true
tags: iOS随笔

---
# 前言
有时候会在真机和模拟器间切换,总是来回替换库到是很不方便.这样可以在开发的时候将真机和模拟器库何必为一个文件,等到发布的时候再替换为真机库即可.

# 正文
使用下面的命令即可合并两个静态库.

```
lipo -create /libXXSimulator.a /libXXOs.a -output /libXX.a
```
使用的时候记得注意文件的路径.其中`-create`后的两个参数是真机和模拟器静态库的路径,`-output`后面的参数是合并后的静态库路径.