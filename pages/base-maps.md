---
layout: article
title: Adding a Base Map Layer
permalink: /base-maps/
aside:
  toc: true
sidebar:
  nav: webmap-workshop
---

Let's try adding a new base map to our map. Mapbox comes with several options for styling your base map layer, which is documented in their [Styles API](https://docs.mapbox.com/api/maps/styles/){:target="\_blank"} pages. For this workshop, we're going to switch from the boilerplate's satellite to imagery to something lighter and with labels for geographic features. This will work best when we overlay a historical map and data.

`To Do`{:.info}

1. In VS Code, identify the line in your boilerplate which defines the source of your base map layer. It should look like `style: "mapbox://styles/mapbox/satellite-v9"`.
2. Change the style to `mapbox://styles/mapbox/light-v11`.
3. Save these changes in VS Code and observe the changes to your map in the browser.

 <iframe height="600px" width="100%" src="/overlaying-the-past/maps/map01.html" title="Dislaying the map boilerplate as a web map"></iframe>
