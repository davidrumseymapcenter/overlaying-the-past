---
layout: article
title: Map Boilerplate
permalink: /setting-up/map-boilerplate/
aside:
  toc: true
sidebar:
  nav: webmap-workshop
---

## The Map HTML Document

A [boilerplate](https://www.freecodecamp.org/news/whats-boilerplate-and-why-do-we-use-it-let-s-check-out-the-coding-style-guide-ac2b6c814ee7/){:target="\_blank"} is a chunk of code that can be used as-is in multiple contexts and often provides the basis for more advanced operations. The boilerplate code for this workshop renders a basemap which we will tinker with and add to in order to build our own map.

Our boilerplate is an HTML document. The HTML document is split into two main sections: the `head` and the `body`. Each of these sections are contained within opening `<` tags `>` and closing `</` tags `>`. Notice that because the document is in HTML format, everything is contained within the `html` tag.

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

## Workshop Boilerplate

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
      /* transparency slider styles below */
    </style>
  </head>
  <body>
    <div id="map"></div>
    <!-- Add a container for the transparency slider to the map. -->

    <script>
      mapboxgl.accessToken = "[your access token]"; // add your own access token. Don't use your default public one.
      const map = new mapboxgl.Map({
        container: "map", // container ID
        style: "mapbox://styles/mapbox/satellite-v9", // style URL
        center: [-122.169462, 37.429889], // starting position [lng, lat]. Note that lat must be set between -90 and 90
        zoom: 13, // starting zoom
      });
      // Add variables for the slider and its value.

      // Add a raster source to the map.

      // Add an event listener for the slider.

      // Add your geojson data source here.

      // Add your popup event listener here.

      // Add a mouseover event listener to the layer.

      // Add zoom and rotation controls to the map.
      map.addControl(new mapboxgl.NavigationControl());
    </script>
  </body>
</html>
```

## Deconstructing This Doc

Let's take a closer look at some of the most important parts of this doc.

### Document Title

The document title is near the top of your HTML file. In addition to being important for web accessibility, this text is what appears in your browser tab.

```html
<title>Add a title here!</title>
```

`To Do`{:.info}

1. In VS Code, change the text inside the `<title>` tag.
2. Save your document.
3. Refresh your browser and view the change.

### External Sources

These two elements of the code appear in the document's `<head>` and are references to external `css` and `js` sources from Mapbox. These are links that your html document needs when Mapbox-specific styles or functions are used. Using these links allow us to keep our code clean and concise, while preserving the source code in an a safe and reliable location.

```html
<link
  href="https://api.mapbox.com/mapbox-gl-js/v3.9.4/mapbox-gl.css"
  rel="stylesheet"
/>
<script src="https://api.mapbox.com/mapbox-gl-js/v3.9.4/mapbox-gl.js"></script>
```

### Doc-Specific CSS Styles

You’ll also want to add styles beyond those provided by Mapbox to customize your document. For example, below is a `<style>` section inside the `<head>` of your HTML document. These styles are instructions to the browser for how to render the page. In this case:

- The body is set to have no margin or padding, allowing the content to take up the full width and height of the viewport.
- The #map element (your map container, which we'll look at next) is [positioned absolutely](https://developer.mozilla.org/en-US/docs/Web/CSS/position) to fill the entire page.

Also note the snippet `/* transparency slider styles below */`. This is CSS comment that your browser ignores – it's only there for developers to be better able to read the code and understand what is happening inside the doc. In this workshop, we're also using them to note where in the code to paste additional blocks.

```html
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
  /* transparency slider styles below */
</style>
```

### Map Container

The first element inside of the `<body>` section is our map container which will "hold" our map. This is an HTML `<div>` container, which is a generic container element used to group other elements in your doc together. One advantage to using a `<div>` is that you can apply styles to the container and everything inside.

```html
<div id="map"></div>
```

Our `<div>` has an ID we've decided to call "**map**". The styles for this container are defined above, and this is the only container we've added to our doc. If we wanted to add more non-map containers to our webpage, such as a side panel, or a narrative introduction to your map, we can do so inside the `<body>` section.

### Map Script

The map script is contained inside a `<script>` tag and is made up of JavaScript that makes our map interactive. The JavaScript written here relies on the Mapbox GL JS library, which we included in the `<head>` of our HTML document. We’re extending that library with our own custom code to define how this particular map behaves.

```js
<script>
    mapboxgl.accessToken = "[your access token]"; // add your own access token. Don't use your default public one.
    const map = new mapboxgl.Map({
      container: "map", // container ID
      style: "mapbox://styles/mapbox/satellite-v9", // style URL
      center: [-122.169462, 37.429889], // starting position [lng, lat]. Note that lat must be set between -90 and 90
      zoom: 13, // starting zoom
    });
    // Add variables for the slider and its value.

    // Add a raster source to the map.

    // Add an event listener for the slider.

    // Add your geojson data source here.

    // Add your popup event listener here.

    // Add a mouseover event listener to the layer.

    // Add zoom and rotation controls to the map.
    map.addControl(new mapboxgl.NavigationControl());
</script>
```

There are three important parts inside this block:

1.  `mapboxgl.accessToken` sets your Mapbox access token, which is required to authenticate your use of Mapbox services. You’ll need to add your own token here — avoid using the default public one.
2.  `const map = new mapboxgl.Map({...})` creates a new map object using Mapbox GL JS. This object holds all the map’s configuration, like which container to use, the style, the initial center point, and the zoom level.
    - `const` is a modern JavaScript keyword for declaring variables that won’t be reassigned.
    - `map` is the name we've chosen for this variable.
3.  `map.addControl(new mapboxgl.NavigationControl());` adds zoom and rotation controls to your map. This is a built-in method provided by Mapbox GL JS.
