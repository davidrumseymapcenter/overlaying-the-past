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

- In VS Code, copy and paste one of the code blocks below in your boilerplate where there is a note `// Add a raster source to the map.`

#### Using your own Allmaps map:

```js
map.on("load", () => {
  // This is an event listener that waits for the map to load before adding the source and layer.
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

- Edit the `[annotation ID]` text with your map's ID, or paste a new full tile url.
- Change `yourID` with something more descriptive, like `sanFrancisco`. Don't use spaces. This is the source's ID, which is also the source of the layer.

#### Using John Snow's map:

```js
map.on("load", () => {
  // This is an event listener that waits for the map to load before adding the source and layer.
  map.addSource("yourID", {
    type: "raster",
    tiles: ["https://allmaps.xyz/images/45bbc7ea6e45e5c9/{z}/{x}/{y}.png"],
    tileSize: 256,
  });

  map.addLayer({
    id: "historical-overlay",
    source: "yourID",
    type: "raster",
  });
});
```

- Save your map and view the changes in the browser.

The recommended way to add an Allmaps tile source is by using an Allmaps plugin, which will reduce the burden on the Allmaps tile servers and load maps faster. Unfortunately, there are no such plugin for Mapbox. There are currently plugins integrating Allmaps with [OpenLayers](https://github.com/allmaps/allmaps/tree/main/packages/openlayers){:target="\_blank"}, [MapLibre](https://github.com/allmaps/allmaps/tree/main/packages/maplibre) and [Leaflet](https://github.com/allmaps/allmaps/tree/main/packages/leaflet). Implemeting these plugins and will be the theme of a future workshop.
{:.warning}

## Change Starting Zoom Level and Position

You will likely have to change where your map loads, so that you don't have to zoom/pan to your georeferenced overlay. We can do this really easily by changing our starting zoom level and position (long/lat). This can also be done programmically with more advanced scripts, but for this workshop we are going to do it the manual way.

`To Do`{:.info}

- Find the approximate centerpoint of your map using [www.findlatlong.com](https://www.findlatlong.com/){:target="\_blank"}.
  HINT: If you're using Snow's map, the Broad Street Pump is at `-0.13667, 51.51333`

- In VS Code, insert the lat/long values in the appropriate order. The order in our map's code is long/lat, or x/y like a computer would expect it.

```js
const map = new mapboxgl.Map({
  container: "map", // container ID
  style: "mapbox://styles/mapbox/light-v11", // style URL
  center: [-122.169462, 37.429889], // starting position [lng, lat]. Note that lat must be set between -90 and 90, and long between -180 and 180
  zoom: 13, // starting zoom
});
```

- Change the starting zoom to fit the map. Save and adjust if needed.

 <iframe height="600px" width="100%" src="/overlaying-the-past/maps/map02.html" title="Dislaying the map boilerplate with a historical map overlay"></iframe>
