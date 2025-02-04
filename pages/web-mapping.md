---
layout: article
title: Web Mapping
permalink: /introduction/web-mapping/
aside:
  toc: true
sidebar:
  nav: webmap-workshop
---

## Digital Map vs Web Map

The term **_digital map_** is broadly used to describe any map that exists in a digital environment — whether viewed in a web browser, within a software application, or as a file on a computer. This definition aligns with the recent redirection of Wikipedia's _Digital Mapping_ entry to _Computer Cartography_, which is defined as:

> the art, science, and technology of making and using maps with a computer.

This definition highlights that digital maps exist in a computer-based environment, but it does not distinguish between static digital representations and interactive web-based mapping technologies. Let’s break this down further with a focus on understaning web maps.

### Digital and Scanned Paper Maps

A digital map is any map created, processed, or stored in a digital format. This broad category is made up of two main types:

1. **Scanned paper maps** – Historical or analog maps that have been scanned and reformatted into digital images, such as this historical map of Vancouver:

<iframe src="https://embed.stanford.edu/iframe?url=https://purl.stanford.edu/yn409cz7502" title="Image viewer" width="800" height="600" allowfullscreen frameborder="0">Map of Leland Stanford Junior University, c1934.</iframe>
<sub><sup>[Map reproduction courtesy of the David Rumsey Map Center, Stanford University Libraries](https://purl.stanford.edu/yn409cz7502)</sup></sub>

2. **Born-digital maps** – Maps created using geospatial data and Geographic Information Systems (GIS). These are designed digitally from the outset, like this City of Vancouver bicycle map, which was generated with GIS data and published as a static file with a set scale:

   ![Palo Alto Bicycle Map 2021](../../assets/images/vancycle.jpg "Palo Alto Bicycle Map 2021")

<sub><sup>[Front of City of Vancouver Cycling 2019 Map](https://vancouver.ca/streets-transportation/cycling-routes-maps-and-trip-planner.aspx)</sup></sub>

### What Makes a Web Map Different?

A **web map** is a specific type of digital map designed for interaction and distribution over the internet using web protocols and technologies. While all web maps are digital maps, not all digital maps are web maps. The main characteristics that set web maps apart include:

- **Dynamic scales and content** – Unlike static digital maps, web maps adjust their level of detail based on zoom level. As you zoom in, more detailed information appears; zooming out provides a broader overview. Because of this adaptability, web maps are not intended to be printed.
- **Interactivity** – Web maps allow users to explore data, toggle layers, and customize views. For example, Climate Central’s [Surging Seas Risk Zone Map](https://ss2.climatecentral.org/#11/37.6121/-122.2778?show=satellite&projections=1-K14_RCP85-SLR&level=4&unit=feet&pois=hide) lets users see projected impacts of sea level rise. Or, spin the globe and listen to radio broadcasts from anywhere in the world with [radio.garden](http://radio.garden/visit/vancouver/Lc5d7EdP).
- **Real-time data integration** – Web maps can pull in live data, making them useful for visualizing changing conditions like weather patterns. See [Nullschool's](https://earth.nullschool.net/#current/wind/surface/level/overlay=temp/orthographic=-99.29,44.51,582) real-time wind and temperature data.
- **Reliance on web and mobile technology** – Web maps are embedded in websites and mobile applications, making them widely accessible. Examples include:
  - Everyday navigation with [Google Maps](https://www.google.com/maps)
  - Small business location services like [Luppolo Brewing’s contact page](https://luppolobrewing.ca/contact/)
  - Mobile geolocation-based routing via [Pokémon GO’s web maps](https://www.pogomap.info/)
  - Research communication, as seen in [UVic’s substance use research map](https://www.uvic.ca/research/centres/cisur/projects/map/index.php)
  - Data-driven journalism, like [this analysis of Amazon warehouse locations](https://storymaps.arcgis.com/stories/adc5ff253a3643f88d39e7f3ef1a09ee)

Understanding this distinction helps us appreciate the unique capabilities and applications of web maps.
