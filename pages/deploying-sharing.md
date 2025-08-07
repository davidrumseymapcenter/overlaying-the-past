---
layout: article
title: Deploying and Sharing in the Web
permalink: /publishing/deploying-sharing/
aside:
  toc: true
sidebar:
  nav: webmap-workshop
---

We're now finally ready to share our map and data over the web using [GitHub Pages](https://pages.github.com/){:target="\_blank"}. Since our map document `html` and data `geojson` are text-based data, GitHub is a good choice to store and manage them. GitHub does have hard limits when it comes to file storage, so be careful not to load anything too big, like cloud optimized geoTIFFs.

Before we move our map into the web, be sure that you're not using your Mapbox default public access token. If you are, you risk others copying and using it for their own projects.
{:.warning}

`To Do`{:.info}

- Save your map in VS Code to verify everything looks good in your browser.
- [Log into your GitHub account](https://github.com/login){:target="_blank"} and go to your repository you set up for this workshop. You may need to click on your profile image in the top right and select \*\*\_Repositories_\*\* to see your list.
- _Drag and drop_ your `map.html` and `snow_water_pumps.geojson` file into your repository. You will be asked to add a commit message – add a short description.
- In GitHub, click on **_Settings_** in the top menu bar.
- On the left side navigation, click **_Pages_**.
- Under _Branch_ select **_main_** from the dropdown, assuming you have no other branches. Click **_Save_**

Now count to 30 and view your map online at the URL `https://[your-username].github.io/[your-repository-name]/map.html`
