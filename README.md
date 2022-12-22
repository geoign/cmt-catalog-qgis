# cmt-catalog-qgis
A hastely-made implementation of GlobalCMT catalog on QGIS for your convenience.
![Sample image](https://github.com/geoign/cmt-catalog-qgis/blob/main/samplescreenshot.jpg)

## Product detail
All data is based on ![GlobalCMT](https://www.globalcmt.org/).
![Obspy](https://docs.obspy.org/) is used for extracting GlobalCMT data.
~~In this implementation, earthquakes larger than M4 between the period of 1991-2020 (30 years) are included.~~
Now it covers all events in GlobalCMT catalog as of Dec. 2022.

## Installation
Note: The following steps show how-to in QGIS 3.28.1. 
1. Download ![GlobalCMT-All.gpkg](https://github.com/geoign/cmt-catalog-qgis/blob/main/GlobalCMT-All.gpkg). This file contains the table (id, latitude, longitude, magnitude, depth, image file name). 
2. Download ![a ZIP file containing SVG images (Google Drive)](https://drive.google.com/file/d/1eyFN9rPi6tNDi8nPYqlECI6mo2zioISg/view?usp=share_link). Note that these images consume **28 GB** of your disk space when they get extracted!!!.
3. Download ![QGIS Style file](https://github.com/geoign/cmt-catalog-qgis/blob/main/globalcmt-style-M7-30km.qml). This file allows to do the basic seup for the gpkg layer.
4. Extract the ZIP file. You will find 57k SVG images in CMTimages folder. Remember where you place them.
5. Open GlobalCMT-All.gpkg on QGIS. Proceed **layer properties -> Style -> Import style**. Choose **globalcmt-style-M7-30km.qml** which was downloaded earlier and apply it to the gpkg layer.
8. Next, choose **Symbology** and click the marker. The marker setting window will pop up. Scroll to the bottom. 
7. Find textbox to choose the path to SVG files. Click "ε" and choose edit to open a textbox.
   ![showing steps 2](https://github.com/geoign/cmt-catalog-qgis/blob/main/screengrab3.jpg)
8. In the textbox, you will find the text in place. 
   You need to change it accodringly to the path to the SVG files which you extracted from the ZIP file.
9. Click OK to close the all pop-ups. You will see several beachballs around the world.
   By default, only the events with Depth<30 km and Mag>7 are shown. 
   You may change it through modifying the filter in **Layer properties -> Symbology -> Value**. 

## Disclaimer
These datasets are provided for conveniently view regional-scale trend in CMT solutions.
Uncertainty, differences in magnitude types, etc. are not considered in this implementation.

## Developer information
Fumihiko Ikegami (Twitter:@geoign) of Ikegami Georesearch. 
