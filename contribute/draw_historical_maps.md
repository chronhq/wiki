# Interactive History Map Project

## Helping out with the map making

Some of you might have experience making maps before. If you've used Inkscape our program is kind of similar in that it uses vectors. But it is a full blown GIS(Geographic Information System) so it supports embedding geographical information in the vectors, like coordinates and projection. We will be using Quantum GIS, a free and open source program but if somehow you are familiar with another program that can produce .shp files you can of course use that.

First thing you do should be downloading QGIS from this [link](https://www.qgis.org/en/site/forusers/download.html). Make sure you download version 2.18. (If you are using Linux your package manager probably has an older version which won't have some features we need.)

QGIS works in layers, similar to programs like gimp, photoshop and inkscape. We will work with three kinds of layers, vector layers where we will draw our maps, raster layers where we will add our reference raster(image) maps and tileserver layer which gives us the world map as seen on websites like google maps.

#### 1. Adding a tileserver

First you should add a tile server so it's easier to navigate the map and see if your reference rasters match up. This gif shows how to do it.

![Adding tileservers](https://www.qgis.org/en/_images/f69a3601e9201e38f9a561d40807512035da2298.gif)

Here is the tileserver adress from the gif for copy-pasting: http://a.tile.openstreetmap.org/{z}/{x}/{y}.png

#### 2. Georeferencing Historic Raster maps

Then you need to georeference the raster maps you want to digitize. Georeferencing warps the raster map so it matches up with our projection. [Here](http://www.qgistutorials.com/en/docs/georeferencing_basics.html) is a tutorial on how to do it.

#### 3. Creating vector maps

Lastly we will create the actual maps. [Here](https://docs.qgis.org/2.8/en/docs/training_manual/create_vector_data/create_new_vector.html) is a good tutorial teaching all the aspects of working with vector layers.

Some things to keep in mind when creating your maps for this project is:

1. Shapes that are not connected must be different features otherwise you will have trouble uploading them.
2. Ask on slack which regions are still available currently before starting to work.
3. You can use vector maps you've found online and edit them so you don't have to trace over all of the coastlines etc. Just make sure that you don't use any vector maps as a base that are not under permissive copyright (like creative commons and opendatabase license).

#### 4. Uploading your creations

TODO
