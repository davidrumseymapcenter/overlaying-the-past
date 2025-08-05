---
layout: article
title: Other Base Map Providers
show_title: false
permalink: /base-maps/other-styles/
aside:
  toc: true
sidebar:
  nav: webmap-workshop
---

You can add sources of base map data to your Mapbox maps as well, such as from [Stadia Maps](https://stadiamaps.com/products/maps/map-styles/){:target="\_blank"}, [OpenStreetMap](https://wiki.openstreetmap.org/wiki/Basemap){:target="\_blank"} ([JSON style](https://raw.githubusercontent.com/go2garret/maps/main/src/assets/json/openStreetMap.json){:target="\_blank"}), [Carto](https://carto.com/basemaps){:target="\_blank"}, and others. You will need to find the style JSON endpoints from these base map providers, but can insert them as a source on your map by creating a custom variable:

```js
const basemap =
  "https://raw.githubusercontent.com/go2garret/maps/main/src/assets/json/openStreetMap.json";

const map = new mapboxgl.Map({
  container: "map", // container ID
  style: basemap,
  center: [-122.169462, 37.429889], // starting position [lng, lat]. Note that lat must be set between -90 and 90
  zoom: 13, // starting zoom
});
```

<!-- Mapbox GL JS v3.x **requires** you to use a Mapbox-hosted style and include an access token. This workshop's boilerplate code uses v3.9.4.
{:. .warning} -->
