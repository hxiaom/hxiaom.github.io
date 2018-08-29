---
layout: post
title: "City Nighttime Lights"
categories: GIS
---
# 城市夜间灯光
创建一个中国县/市级别的城市夜间灯光照片生成网站

输入：中国 县/市
输出：该县/市的夜间灯光照片

数据需求：
1. 城市区划
2. 夜间灯光数据

# 参考资料：
1. 夜间灯光数据为 geotiffs 格式
    资料：http://trac.osgeo.org/geotiff/   https://www.gdal.org/gdal_tutorial.html
    通过 python gdal 读取 geotiff 文件
2. 截取出城市区划