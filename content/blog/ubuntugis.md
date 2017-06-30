+++
title = "Ubuntu下的GIS软件安装：UbuntuGIS"
date = "2017-06-30"
categories = ["技术"]
tags = ['GIS']
authors = ['forget']
slug = 'ubuntugis'
+++

# 1.Ubuntu系统
Ubuntu是开源Linux系统中应用最广的系统分支之一（桌面系统），主要Linux环境中开发的软件都能够在该系统中运行。为了GIS从业人员能够通过apt-get命令来安装和更新GIS软件，[UbuntuGIS](https://launchpad.net/~ubuntugis)团队开发[开源GIS软件仓库](http://trac.osgeo.org/ubuntugis/wiki/UbuntuGISRepository),以PPA的方式提供服务。UbuntuGIS软件仓库基本上包含了常用的Linux环境中的开源GIS软件，比如：QGIS、GRASS、GMT、Mbsystem等等。
# 2.UbuntuGIS仓库使用
UbuntuGIS软件仓库提供两种PPA，一种是每六个月更新一次的稳定版，一种是经常更新的非稳定版，在使用的时候，最好将两个PPA地址都加入到apt的源中。操作如下：
```bash
sudo apt-get install python-software-properties
sudo add-apt-repository ppa:ubuntugis/ubuntugis-unstable
sudo add-apt-repository ppa:ubuntugis/ppa
```
然后更新Ubuntu的APT源（Source）：
```bash
sudo apt-get update
```
接下来就可以在终端（Terminal）中，使用apt来安装、更新和维护你的软件系统了。

# 3.Mbsystem安装
Ubuntu下的[Mbsystem](http://www.mbari.org/products/research-software/mb-system/how-to-download-and-install-mb-system/)官方推荐使用UbuntuGIS的软件仓库来安装。Mbsystem在UbuntuGIS的非稳定版软件仓库中，在安装前需要按照上文对本地计算机的apt源进行更新。利用这种方式安装GMT和Mbsystem软件就非常简单了。步骤如下：
（1）安装GMT
使用[GMT官方](http://gmt.soest.hawaii.edu/projects/gmt/wiki/Installing)推荐的安装方式安装：
```bash
sudo apt-get install gmt gmt-dcw gmt-gshhg
```
(2)安装mbsystem
安装好GMT之后，再安装Mbsystem，在这个过程中，它会自动查找并安装软件所需要的依赖库。
```bash
sudo apt-get install mbsystem
```
（3）配置GMT_CUSTOM_LIBS
MBsystem软件中，有几个命令依赖于GMT函数，比如：mbcontour等。因此需要
在GMT安装目录（默认为:/usr/share/gmt/conf）下，编辑gmt.conf文件，找到GMT_CUSTOM_LIBS字段（默认情况下是空的）的等号“=”后面，添加mbsystem的gmt库，默认安装路径是：/usr/lib/libmbgmt.so.0。比如：
```conf
#
# GMT Miscellaneous Parameters
#
GMT_COMPATIBILITY		= 4
GMT_CUSTOM_LIBS			= /usr/lib/libmbgmt.so.0
GMT_EXTRAPOLATE_VAL		= NaN
GMT_FFT				= auto
GMT_HISTORY			= true
GMT_INTERPOLANT			= akima
GMT_TRIANGULATE			= Shewchuk
GMT_VERBOSE			= compat
```
