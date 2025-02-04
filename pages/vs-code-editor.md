---
layout: article
title: Visual Studio Code Editor
permalink: /setting-up/vs-code-editor/
aside:
  toc: true
sidebar:
  nav: webmap-workshop
---

In the hands-on portion of this workshop, we'll use [Visual Studio Code (VS Code)](https://code.visualstudio.com/) to edit our web map's code. VS Code is a free software from Microsoft that offers a wide range of features designed to make coding easier. Its extensive repository of extensions allows you to customize its base features according to the type of coding work you do. For example, since we need to view our web map in a local server, we will install a plugin called **Live Server**.

## Download and Install VS Code

You will need VS Code installed on your local computer for the hands-on portion of this workshop.

`To Do`{:.info}

1. Head to [code.visualstudio.com/download](https://code.visualstudio.com/Download) and download the installer for your platform.
2. Install the software on your computer and open the application.

Once VS Code is installed, you are ready to proceed with installing your first extension.

## Install the Live Server Extension

Once VS Code is installed, you can install the [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) extension. We'll use this to launch a local server, allowing us to view our web map as a working web application in a browser.

![Live Server VS Code Extension](../../assets/images/live-server.png "Live Server VS Code Extension")

`To Do`{:.info}

1. In VS Code, press `Ctrl+P` (Windows) or `Command+P` (Mac) to bring up the search console.
2. In the search console, type `ext install ritwickdey.liveserver` and press **Enter**.

Once installed, you should see the **"Go Live"** icon in the bottom right corner of the VS Code window.
