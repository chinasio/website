+++
title = "数据"
+++
# 常用海洋共享数据

## 1. 矢量数据
### （1）全球海岸线数据[GSHHG](https://www.ngdc.noaa.gov/mgg/shorelines/gshhs.html)
由 [GMT](gmt.soest.hawaii.edu)软件开发者Paul Wessel更新和维护，NGDC提供 [数据下载](https://www.ngdc.noaa.gov/mgg/shorelines/gshhs.html)。

### (2)Natural Earth Data
提供全球范围的地理矢量数据下载，免费开放下载([下载地址](http://www.naturalearthdata.com/downloads/))，持续更新。开发和维护者的话：
> Natural Earth is designed to meet the needs of production cartographers using a variety of software applications. Maximum flexibility is a goal.

## 2.栅格海底地形数据
### （1）全球大洋制图数据GEBCO
海底地形数据首推有大洋制图委员会制作的通用大洋制图数据集，最新版的为2015年发布的GEBCO_2014，海底地形网格间距为30弧秒，融合了全球范围内的最新共享单波束和多波束成果（~~没有中国的贡献~~）。在英国海洋数据中心[BODC](https://www.bodc.ac.uk/data/hosted_data_systems/gebco_gridded_bathymetry_data/)和通用大洋制图委员会[GEBCO](http://www.gebco.net/data_and_products/gridded_bathymetry_data/)都能下载。推荐下载netCDF格式配合GEBCO提供的查看和抽取软件[Grid display software](http://www.gebco.net/data_and_products/grid_display_software/)使用。

### （2）南北极海底地形数据
针对南极和北极海域，通用大洋制图委员会设立了各自的制图项目。南极海域的为南大洋制图项目[IBCSO](www.ibcso.org),由德国魏格纳海洋研究所的Jan Erik Arndt 负责，于2013年完成了第一版(IBCSO V1.0 Digital Bathymetric Model)南极周边海域500m网格间距的南大洋海底地形数据集（[下载地址](https://doi.pangaea.de/10.1594/PANGAEA.805734?format=html)）。北冰洋海底制图项目由1997年启动，目前最新的海底地形数据为2012年发布的IBCAO Version 3.0。该数据集融合了2012年之前完成的国际共享多波束（包括美国利用核潜艇调查的）和单波束数据，网格间距为500m（[下载地址](https://www.ngdc.noaa.gov/mgg/bathymetry/arctic/downloads.html)）。

### (3)美国外大陆架调查项目
美国虽然没有承认海洋法公约，但是也在积极开展自己的外大陆架调查工作(见[U.S. Extended Continental Shelf (ECS) Project](https://www.continentalshelf.gov/))，除了美国本土周边之外，在马尼亚纳群岛、阿拉斯加、楚科奇边缘地和夏威夷群岛周边都开展了大量多波束调查，并且编辑好的多波束实测地形、地貌（浅剖和散射数据）**免费**向全球**开放共享、下载**（[下载地址](http://ccom.unh.edu/theme/law-sea)）。

### （4）欧洲海洋观测和数据网
欧洲数据开放共享程度仅此于美国，2009年开始组建欧洲范围内的欧洲海洋观测和数据网(见[EMODnet](http://www.emodnet.eu/)),将欧洲各国的调查数据制作了海底地形网格，通过EMODnet提供免费开放下载（[下载地址](http://portal.emodnet-bathymetry.eu/)）。

### （5）美国在全球各大洋的实测多波束数据（**重点推荐**）
美国地球物理数据中心（[NGDC](https://maps.ngdc.noaa.gov/viewers/bathymetry/)）提供美国自然基金会资助的所有航次的多波束实测数据免费下载服务，数据格式为[MBsystem](https://www.ldeo.columbia.edu/res/pi/MB-System/)（开源多波束处理软件）格式。

推荐理由：数据质量和精度完全在你的控制之下，可以根据不同的需求制作不同的数据网格。

## 3.地球物理数据
### （1）重力数据
- 重力数据首推Sandwell利用卫星测高制作的全球1′×1′重力异常数据（[下载地址](ftp://topex.ucsd.edu/pub/global_grav_1min/)）。
- 南极重力和大地水准面项目也发布了一个**不完全**覆盖南极的重力数据模型：ANTGG2015（[地址](https://doi.pangaea.de/10.1594/PANGAEA.848168)）。
- 环北极制图项目（见[Circum-Arctic Mapping Project](https://www.ngu.no/en/publikasjon/circum-arctic-mapping-project-gravity-and-magnetic-maps-camp-gm)）编制了北极地区10km×10km的重力和地磁网格。

### （2）地磁数据
- 全球地磁场主要由[EMAG2](http://geomag.org/models/emag2.html)和[WDMAM](http://www.wdmam.org/)两种数据模型。
- 南极有ADMAP项目，但是数据较老。