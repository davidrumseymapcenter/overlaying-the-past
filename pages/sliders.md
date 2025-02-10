---
layout: article
title: Transparency Sliders
permalink: /historical-overlays/sliders/
aside:
  toc: true
sidebar:
  nav: webmap-workshop
---

Mapbox Example: [Adjust a layer's opacity](https://docs.mapbox.com/mapbox-gl-js/example/adjust-layer-opacity/){:target="\_blank"}
{:. .info}

Since we probably want to be able to view the modern base map below the georeferenced map we just added, let's make transparency slider. A transparency slider (sometimes also called opacity slider) gradually reduces the transparency of a layer from 0% to 100% transparent. Other common ways of doing this are by using a [swipe method](https://github.com/mapbox/mapbox-gl-compare){:target="\_blank"}, or by [toggling layers](https://docs.mapbox.com/mapbox-gl-js/example/toggle-layers/){:target="\_blank"}.

For this to work, we will need to:

1.  Define the style of the new controls on the web map,
2.  Create the html container for where the controls will be placed on the web map,
3.  Add a **variable** for the slider and its status. A variable in JavaScript is something that holds a defined value.
4.  Add an **event listener** for the slider to work with our layer. An event listener is a JavaScript method for how we make our web page respond to something, such as clicking on a button, moving a mouse over a transpareny slider control.

`To Do`{:.info}

- In VS Code, find the comment for the CSS of the controls in the `<head>`. Insert the following style just below the comment.

```css
.map-overlay {
  font: bold 12px/20px "Helvetica Neue", Arial, Helvetica, sans-serif;
  position: absolute;
  width: 25%;
  top: 0;
  left: 0;
  padding: 10px;
}

.map-overlay .map-overlay-inner {
  background-color: #fff;
  box-shadow: 0 1px 2px rgba(0, 0, 0, 0.2);
  border-radius: 3px;
  padding: 10px;
  margin-bottom: 10px;
}

.map-overlay label {
  display: block;
  margin: 0 0 10px;
}

.map-overlay input {
  background-color: transparent;
  display: inline-block;
  width: 100%;
  position: relative;
  margin: 0;
  cursor: ew-resize;
}
```

- Add the container for the slider to be visible on the web map. Save and view the map in your browser. You should notice a new control in the top left of your map. It won't work until we've added the rest of the code to set it to work with our map layer.

```html
<div class="map-overlay top">
  <div class="map-overlay-inner">
    <label>Layer opacity: <span id="slider-value">100%</span></label>
    <input id="slider" type="range" min="0" max="100" step="0" value="100" />
  </div>
</div>
```

- Add the variables for the slider and its status

```js
const slider = document.getElementById("slider");
const sliderValue = document.getElementById("slider-value");
```

- Add the event listener for the slider interaction. Save yand view the map in your browser.

```js
slider.addEventListener("input", (e) => {
  // Adjust the layers opacity. layer here is arbitrary - this could
  // be another layer name found in your style or a custom layer
  // added on the fly using `addSource`.
  map.setPaintProperty(
    "historical-overlay",
    "raster-opacity",
    parseInt(e.target.value, 10) / 100
  );

  // Value indicator
  sliderValue.textContent = e.target.value + "%";
});
```

You should see your map with the transparency slider controls, which should work if you click and drag the controls to change the transparency.

 <iframe height="600px" width="100%" src="/overlaying-the-past/maps/map03.html" title="Dislaying the map boilerplate with a historical map overlay and transparency slider"></iframe>
