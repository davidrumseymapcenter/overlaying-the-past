---
layout: article
title: Adding Historical Map Overlays
permalink: /historical-overlays/
aside:
  toc: true
sidebar:
  nav: webmap-workshop
---

[Mapbox documentation for adding sources](https://docs.mapbox.com/mapbox-gl-js/api/sources/){:target="\_blank"} is the complete resource for adding data layers to your map.
{:.info}

Let's add our georeferenced map from Allmaps. To do this, we are going to add the georeferenced map as a source to our Mapbox map as an XYZ tile layer. We will need a few things first including the annotation ID (a 16-digit alpha numeric string) of the map in Allmaps. Once you have that ready, open your map boilerplate in VS Code.

`To Do`{:.info}

1. In VS Code, copy and paste the code block below in your boilerplate where there is a note `// Add a raster source to the map.`

```js
map.on("load", () => {
  map.addSource("yourID", {
    type: "raster",
    tiles: ["https://allmaps.xyz/maps/[annotation ID]/{z}/{x}/{y}.png"],
    tileSize: 256,
  });

  map.addLayer({
    id: "historical-overlay",
    source: "yourID",
    type: "raster",
  });
});
```

2. Edit the `[annotation ID]` text with your map's ID.
3. Change `yourID` with something more descriptive, like `sanFrancisco`. Don't use spaces.
4. Save your map and view the changes in the browser.

The recommended way to add an Allmaps tile source is by using a plugin, which will reduce the burden on the Allmaps tile servers and load maps faster. Unfortunately, there are no such plugin for Mapbox. There is currently a plugin integrating [OpenLayers and Allmaps](https://github.com/allmaps/allmaps/tree/main/packages/openlayers){:target="\_blank"}, and will soon be for MapLibre and Leaflet.
{:.warning}

## Change Starting Zoom Level and Position

You will likely have to change where your map loads, so that you don't have to zoom/pan to your georeferenced overlay. We can do this really easily by changing our starting zoom level and position (long/lat). This can also be done programmically with more advanced scripts, but for this workshop we are going to do it the manual way.

`To Do`{:.info}

1. Find the approximate centerpoint of your map using [www.findlatlong.com](https://www.findlatlong.com/){:target="\_blank"}. Just relax and eyeball it.
2. In VS Code, insert the lat/long values in the appropriate order. The order in our map's code is long/lat, or x/y like a computer would expect it.

```js
const map = new mapboxgl.Map({
  container: "map", // container ID
  style: "mapbox://styles/mapbox/light-v11", // style URL
  center: [-122.169462, 37.429889], // starting position [lng, lat]. Note that lat must be set between -90 and 90
  zoom: 13, // starting zoom
});
```

3. Change the starting zoom to fit the map. Save and adjust if needed.

 <iframe height="600px" width="100%" src="/overlaying-the-past/maps/map02.html" title="Dislaying the map boilerplate with a historical map overlay"></iframe>
