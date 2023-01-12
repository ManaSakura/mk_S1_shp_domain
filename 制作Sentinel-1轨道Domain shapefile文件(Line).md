1将sentinel-1中的kml文件导入Global Mapper

![1](制作Sentinel-1轨道Domain shapefile文件(Line).assets/1.jpg)

2在Global Mapper中，'File' -> 'Export' ->'Export raster/image format'



![2](制作Sentinel-1轨道Domain shapefile文件(Line).assets/2.jpg)

3 导出，选择'GeoTIFF'格式，导入文件为142_116.tif

![3](制作Sentinel-1轨道Domain shapefile文件(Line).assets/3.jpg)

4 将142_126.tif 导入arcgis中，发现有白色背景色，看到背景色对应的白色像素值为255

![image-20221211173428342](制作Sentinel-1轨道Domain shapefile文件(Line).assets/image-20221211173428342.png)

5 将白色像素值更改为 ‘NoData', 右键142_126.tif，'数据‘ -> '导出数据'，将NoData设置为255，设置导出格式为TIFF，设置导出位置，文件命名为142_121.tif

![image-20221211174332052](制作Sentinel-1轨道Domain shapefile文件(Line).assets/image-20221211174332052.png)

6 导出后的142_1261.tif可以看到没有白色背景

![image-20221211174520794](制作Sentinel-1轨道Domain shapefile文件(Line).assets/image-20221211174520794.png)

7 导出影像范围，3D Analyst工具 -> 转换 ->由栅格转出 ->栅格范围，保存文件为142_1261RasterDomain.shp

![image-20221211174732049](制作Sentinel-1轨道Domain shapefile文件(Line).assets/image-20221211174732049.png)

8 此时导入142_1261RasterDomain.shp就为影像覆盖范围

![image-20221211174846539](制作Sentinel-1轨道Domain shapefile文件(Line).assets/image-20221211174846539.png)