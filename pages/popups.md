---
layout: article
title: Adding Popups
permalink: /adding-data/popups/
aside:
  toc: true
sidebar:
  nav: webmap-workshop
---

Mapbox Example: [Show polygon information on click](https://docs.mapbox.com/mapbox-gl-js/example/polygon-popup-on-click/){:target="\_blank"}
{:.info}

The data that you added to the map has attribute values (geojson properties) for each of the features. Our example geojson data represents the locations of public water pumps in John Snow's London, with a property called `label`. The map we've built up until now doesn't use that property, but let's make our map show a popup when we click on one of the pump locations.

### Popup Click Event

The first thing we want to do is create a popup that appears when a user clicks on a feature in the `"snow_water_pumps" layer`. The code block below adds a Mapbox GL JS [`click` event](https://docs.mapbox.com/mapbox-gl-js/api/map/#map#on) listener that passes an event object (e) to the function. This event object contains information like the clicked location (e.lngLat) and the clicked feature(s), which we use to display a popup with content from the feature's properties.

Note that the popup below sets the HTML to include a `property` called `label`, so will need to be edited if you are showing a popup with another property name.
{:.warning}

`To Do`{:.info}

- Copy and paste the code below into your boilerplate below the comment `// Add your popup event listener here.`

```js
map.on("click", "snow_water_pumps", (e) => {
  new mapboxgl.Popup()
    .setLngLat(e.lngLat)
    .setHTML(e.features[0].properties.label)
    .addTo(map);
});
```

- Save the map and view the changes in your browser. You've created an un-styled Mapbox Popup.

### Mouseover Event

Notice that the map's cursor doesn't change like it would normally when hovering over a link. A changing cursor improves user experience and interactivity by giving a clear visual signal that something on the map is clickable or interactive. Let's add this functionality to our map.

The code below changes your cursor to a pointer when hovering over a point, then

`To Do`{:.info}

- Copy and paste the code below into your boilerplate below the comment `// Add a mouseover event listener to the layer.`

```js
// Change the cursor from a hand to a pointer when
// the mouse is over the pumps layer.
map.on("mouseenter", "snow_water_pumps", () => {
  map.getCanvas().style.cursor = "pointer";
});

// Change the cursor back to the default hand
// when it leaves the pumps layer.
map.on("mouseleave", "snow_water_pumps", () => {
  map.getCanvas().style.cursor = "";
});
```
