---
layout: article
title: Adding GeoJSON Data
permalink: /adding-data/
aside:
  toc: true
sidebar:
  nav: webmap-workshop
---

Let's add our geoJSON data we made from our georeferenced map. By now you have already heard what geoJSON is and how it is structured, but if you want to know even more, [Tom Macwright's More than you ever wanted to know about GeoJSON](https://macwright.com/2015/03/23/geojson-second-bite){:target="\_blank"} is a great read.

Mapbox Example: [Load data from an external GeoJSON file](https://docs.mapbox.com/mapbox-gl-js/example/external-geojson/){:target="\_blank"}.
{:.info}

## Add a GeoJSON Source

`To Do`{:.info}

- Verify you have your geoJSON data stored in the same directory as your map boilerplate. Your directory should look something like:

```
├── map-boilerplate
    |
    ├── map.html
    |
    └── export.geojson

```

- In VS Code, add the text below where you find the comment about adding a geojson source.

```js
map.on("load", () => {
  map.addSource("datalayer", {
    type: "geojson",
    data: "export.geojson", // be sure filename and path matches yours.
  });
  // add your layer and styles here
});
```

- Save your map in VS Code.

## Add and Style the GeoJSON Layer

The next step is to add the source as a layer on your map, while also giving it some styling. Since styles in Mapbox GL JS are applied differently to points, lines, and polygons, you will need to choose the appropriate directions below. The full documentation on adding and styling layers is essential in understanding how to make your data layers look and feel the way that you want them.

Mapbox Documentation: [Style Spec Reference for Mapbox Layers](https://docs.mapbox.com/style-spec/reference/layers/){:target="\_blank"}.
{:.info}

### Adding Points

`To Do`{:.info}

- If you are adding point data, add the text below to your map in VS Code. This will make the points appear as small blue circles with white strokes.

```js
map.addLayer({
  id: "example",
  type: "circle",
  source: "datalayer",
  layout: {},
  paint: {
    "circle-radius": 4,
    "circle-stroke-width": 2,
    "circle-color": "#88c0d0",
    "circle-stroke-color": "white",
  },
});
```

### Adding Polygons

`To Do`{:.info}

- If you are adding **polygon** data, add the text below to your map in VS Code. This will make the polygons appear as blue shapes.

```js
map.addLayer({
  id: "example",
  type: "fill",
  source: "datalayer",
  layout: {},
  paint: {
    "fill-color": "#88c0d0",
    "fill-opacity": 0.5,
  },
});
```

### Adding Lines

`To Do`{:.info}

- If you are adding **line** data, add the text below to your map in VS Code. This will make the lines appear blue with rounded edges.

```js
map.addLayer({
  id: "example",
  type: "line",
  source: "datalayer",
  layout: {
    "line-join": "round",
    "line-cap": "round",
  },
  paint: {
    "line-color": "#888",
    "line-width": 8,
  },
});
```

If done correctly, you should see a similarly functioning map:

<iframe height="600px" width="100%" src="/overlaying-the-past/maps/map04.html" title="Dislaying the map boilerplate with a historical map overlay and transparency slider"></iframe>
