---
layout: article
title: Other Overlay Options
permalink: /historical-overlays/other-overlay-options/
aside:
  toc: true
sidebar:
  nav: webmap-workshop
---

There are other ways than using _external_ tile servers and to display historical map overlays on web pages.

## Local Tile Set

You can create your own tile set from a georeferenced map using the beloved [Geospatial Data Abstraction Library (GDAL)](https://gdal.org/en/stable/){:target="\_blank"}. GDAL is an open source and powerful toolkit for working with geographic raster data. It has many build it functions that allow us to do all kinds of things with our data, including a script called [gdal2tiles](https://gdal.org/en/stable/programs/gdal2tiles.html){:target="\_blank"}. Gdal2tiles is a Python script that splits up a raster image into a directory structure that can be read as an XYZ tile layer by your web map framework. GDAL doesn't have a GUI and can be intimidating to some, but it's a very efficient and feature rich tool.

![GDAL Logo](https://upload.wikimedia.org/wikipedia/commons/thumb/d/df/GDALLogoColor.svg/200px-GDALLogoColor.svg.png?20080323200139 "Geospatial Data Abstraction Library")

<div style="text-align: center;"><sub><sup>[Copyright © GDAL Team](https://commons.wikimedia.org/wiki/File:GDALLogoColor.svg). [Used under CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/deed.en)</sup></sub></div>

## Web Map Services (WMS)

A [Web Map Service (WMS)](https://www.ogc.org/publications/standard/wms/){:target="\_blank"} is a protocol for requesting and getting georeferenced map images over the web, and is a very common way of sharing data over the web. In order to get a WMS map image, you need to request the map from the server. There are many servers hosting WMS services, such as Stanford's Earthworks discovery platform for spatial data. There is an example in the Mapbox GL JS documentation showing [how to add a WMS layer to your Mapbox map](https://docs.mapbox.com/mapbox-gl-js/example/wms/){:target="\_blank"}.

## Cloud Optimized GeoTIFF (COG)
