---
layout: article
title: Introduction
url: /overlaying-the-past/
show_title: false
aside:
  toc: true
sidebar:
  nav: webmap-workshop
---

This workshop is still being developed and not yet complete. Please excuse the mess.
{:.warning}

# Overview

This beginner-level workshop is intended for anyone interested in overlaying and sharing historical spatial data in the web. We will use modern frameworks and applications including [IIIF](https://iiif.io/), [Allmaps](https://allmaps.org/), [ArcGIS Online](https://www.arcgis.com/index.html), [Visual Studio Code](https://code.visualstudio.com/), and [Mapbox GL JS](https://docs.mapbox.com/mapbox-gl-js/guides) to move from a scanned digital map image, to publishing a georeferenced overlay and extracted historical data on a web map. This workshop builds on previous workshops:

- [Discovering IIIF enabled historical maps online](#)
- [Georeferencing maps using the Allmaps toolkit](#)
- [Combining historical maps and spatial data with Mapbox GL JS](#)

The workshop aims to develop the fundamental knowledge and skills to begin sharing historical map overlays using web maps, while providing opportunities to ask questions along the way. There are two main sections: an introduction to web maps, and a hands-on where we will will learn to customize boilerplate code from within a source code editor to make an interactive map showing a historical map overlay and modern data, powered by Mapbox GL JavaScript library.

# What You Will Build

 <iframe height="600px" width="100%" src="maps/map1.html" title="Example webmap with historical map overlay"></iframe>

# Agenda

| Time | Section                        | Objectives                                                                                                                     |
| ---- | ------------------------------ | ------------------------------------------------------------------------------------------------------------------------------ |
| 0:00 | Welcome                        | Who is this for?<br>What will we be covering?                                                                                  |
| 0:10 | Introduction                   | What is a Web Map?<br>Which web mapping are best for me?                                                                       |
| 0:35 | Setting Up                     | How do I set up my local environment?<br>How do I set up my MapBox account?                                                    |
| 0:45 | Adding a Base Map              | What's important in a base map?<br>How do I add a base map?                                                                    |
| 0:55 | Adding Historical Map Overlays | What are my options for adding historical map overlays?<br>How do I add an XYZ tileset?<br>How do I add a transparency slider? |
| 1:05 | Adding Custom Data             | Which kinds of data can I add to my map?<br>How do I add a geojson layer?<br>How do I add a transparency slider?               |
| 1:15 | Customizing and Finalizing     | How do I customize the style of my data?<br>What options do I have for sharing my web map in the web?                          |
| 1:35 | Next Steps                     | Where do I go for help?<br>Which options do I have for creating web maps at scale?                                             |

# Pre-Workshop Setup

You will need to arrived prepared for the workshop by:

1. Installing and configuring Visual Studio Code
2. Setting up your free MapBox account
3. Creating a free GitHub account

Each of these steps is detailed in the [Setting Up](/overlaying-the-past/setting-up/) section.

# Workshop Source Code

The content making up this workshop is being managed in [GitHub](https://github.com/), and we welcome suggestions for how to improve in the form of GitHub Issues. Please use Issues to let us know about things like grammatical errors, broken links, or other suggested updates.

<div style="text-align: center;">
  <a href="https://github.com/davidrumseymapcenter/overlaying-the-past" target="_blank" style="display: inline-block; width: 100px;">
    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 98 96" width="100" height="100">
      <path fill-rule="evenodd" clip-rule="evenodd" d="M48.854 0C21.839 0 0 22 0 49.217c0 21.756 13.993 40.172 33.405 46.69 2.427.49 3.316-1.059 3.316-2.362 0-1.141-.08-5.052-.08-9.127-13.59 2.934-16.42-5.867-16.42-5.867-2.184-5.704-5.42-7.17-5.42-7.17-4.448-3.015.324-3.015.324-3.015 4.934.326 7.523 5.052 7.523 5.052 4.367 7.496 11.404 5.378 14.235 4.074.404-3.178 1.699-5.378 3.074-6.6-10.839-1.141-22.243-5.378-22.243-24.283 0-5.378 1.94-9.778 5.014-13.2-.485-1.222-2.184-6.275.486-13.038 0 0 4.125-1.304 13.426 5.052a46.97 46.97 0 0 1 12.214-1.63c4.125 0 8.33.571 12.213 1.63 9.302-6.356 13.427-5.052 13.427-5.052 2.67 6.763.97 11.816.485 13.038 3.155 3.422 5.015 7.822 5.015 13.2 0 18.905-11.404 23.06-22.324 24.283 1.78 1.548 3.316 4.481 3.316 9.126 0 6.6-.08 11.897-.08 13.526 0 1.304.89 2.853 3.316 2.364 19.412-6.52 33.405-24.935 33.405-46.691C97.707 22 75.788 0 48.854 0z" fill="#24292f"/>
    </svg>
  </a>
</div>
<div style="text-align: center;">
    <a href="https://github.com/davidrumseymapcenter/overlaying-the-past" target="_blank">github.com/davidrumseymapcenter/overlaying-the-past</a>
</div>
