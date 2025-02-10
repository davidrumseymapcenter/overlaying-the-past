---
layout: article
title: Map Boilerplate
permalink: /setting-up/map-boilerplate/
aside:
  toc: true
sidebar:
  nav: webmap-workshop
---

A [boilerplate](https://www.freecodecamp.org/news/whats-boilerplate-and-why-do-we-use-it-let-s-check-out-the-coding-style-guide-ac2b6c814ee7/){:target="\_blank"} is a chunk of code that can be used as-is in multiple contexts and often provides the basis for more advanced operations. The boilerplate code for this workshop renders a basemap which we will tinker with and add to in order to build our own map.

Mapbox Example: [Display a map on a webpage](https://docs.mapbox.com/mapbox-gl-js/example/simple-map/){:target="\_blank"}
{:. .info}

Now that we've seen what the boilerplate basemap for this workshop looks like, let’s explore the code behind it. Return to VS Code (your code editer). Your boilerplate should look like this:

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8" />
    <title>Add a title here!</title>
    <meta
      name="viewport"
      content="initial-scale=1,maximum-scale=1,user-scalable=no"
    />
    <link
      href="https://api.mapbox.com/mapbox-gl-js/v3.9.4/mapbox-gl.css"
      rel="stylesheet"
    />
    <script src="https://api.mapbox.com/mapbox-gl-js/v3.9.4/mapbox-gl.js"></script>
    <script src="./data.js" charset="utf-8"></script>
    <style>
      body {
        margin: 0;
        padding: 0;
      }
      #map {
        position: absolute;
        top: 0;
        bottom: 0;
        width: 100%;
      }
    </style>
  </head>
  <body>
    <div id="map"></div>
    <script>
      mapboxgl.accessToken = "[your new Mapbox access token]"; // don't use your public access token!
      const map = new mapboxgl.Map({
        container: "map", // container ID which you can see in the <div> above
        center: [-122.167486, 37.429214], // starting position [lng, lat]. Note that lat must be set between -90 and 90
        zoom: 6, // starting zoom
      });
    </script>
  </body>
</html>
```

## The Map HTML Document

The HTML document is split into two main sections: the `head` and the `body`. Each of these sections are contained within opening `<` tags `>` and closing `</` tags `>`. Notice that because the document is in HTML format, everything is contained within the `html` tag.

```html
<html>
  <head>
    The stuff inside the head is the metadata for your browser as well as links
    to the source code for Mapbox's JavaScript and CSS rules. If you copy either
    one of those links and paste it in a new tab in your browser, you’ll see a
    lot of raw code. By linking to the source, we avoid having to carry this
    text into our own document, while also being assured that the code we’re
    using is up-to-date.
  </head>

  <body>
    The body contains what you see formatted in your browser. In the code above,
    the body contains directions for rendering and displaying an interactive map
    centered on the Bay Area of California that takes up the entire document.
    <script>
      Nested inside the body is a page-specific block of JavaScript that loads the map on the screen.
    </script>
  </body>
</html>
```

## Data Sources

Beneath the Mapbox CSS and Javascript source links in the `head` is the line `<script src="./data.js" charset="utf-8"></script>`. This is a link to the map data, wrapped inside a JavaScript variable. You'll notice that this is linking to a file called **data.js** by using its relative path. Currently, that file is empty, but we will us our GeoJSON code from previous workshops to populate that file later on.
