---
layout: article
title: Adding GeoJSON Data
permalink: /adding-data/
aside:
  toc: true
sidebar:
  nav: webmap-workshop
---

Let's add our geoJSON data we made from our georeferenced map. By now you have already heard what geoJSON is and how it is structured, but if you want to know even more, [Tom Macwright's More than you ever wanted to know about GeoJSON](https://macwright.com/2015/03/23/geojson-second-bite) is a great read.

There are two primary ways to add geoJSON data to your map:

1. [From an external sournce using a URL endpoint](https://docs.mapbox.com/mapbox-gl-js/example/external-geojson/).
2. As a local data layer.

Since our data has (probably) not been uploaded to the web, we're going to create a local data layer and add it to our map.
