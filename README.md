# cmt-catalog-qgis
The hastely-made implementation of GlobalCMT catalog on QGIS for your convenience.

## Product detail
All data is based on [GlobalCMT>https://www.globalcmt.org/].
[Obspy>https://docs.obspy.org/] is used for extracting GlobalCMT data.
In this implementation, earthquakes larger than M4 between the period of 1991-2020 (30 years) are included.

## Installation
Note: The following steps show how-to in QGIS 3.28.1. 
1. Download GlobalCMT-M4-1991-2020.gpkg. This file contains the table (id, latitude, longitude, magnitude, depth, image file name). 
2. Download [[a ZIP file containing SVG images>https://drive.google.com/file/d/1YIS7r06jmMpaXapfmDQdW7KwuBJKHyio/view?usp=share_link]]. Note that these images consumes 23.2 GB of your disk space when they get extracted!!!.
3. Extract the ZIP file. You will find 46k SVG images in CMTimages folder.
4. Open GlobalCMT-M4-1991-2020.gpkg on QGIS.
5. Proceed layer properties -> Symbology. If you are a Pro of QGIS, you may choose "graduated" symbology and then type case when "mag" > 7 then case when "dep" < 30 then "mag" end end or something to the "Value". If you are new to QGIS, choose "single". 
6. Marker setting. You need to click the second row (1) and choose "SVG marker" (2). Then scroll down to the bottom.
7. Find textbox to choose the path to SVG files. Click "ε" and choose edit to open a textbox.
8. In the textbox, you need to specify the path to the extracted SVG file. For example, type 'E:\\GIS\\Seismicity\\GlobalCMT\\' || "imgfile" if the SVG files have the path E:\GIS\Seismicity\GlobalCMT\CMTimages\*.svg. 
9. Click OK to close the windows. Done!

## Disclaimer
These datasets are provided for conveniently view regional-scale trend in CMT solutions.
Uncertainty, differences in magnitude types, etc. are not considered in this implementation.

