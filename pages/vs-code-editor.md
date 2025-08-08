---
layout: article
title: Visual Studio Code Editor
permalink: /setting-up/vs-code-editor/
aside:
  toc: true
sidebar:
  nav: webmap-workshop
---

In the hands-on portion of this workshop, we'll use [Visual Studio Code (VS Code)](https://code.visualstudio.com/){:target="\_blank"} to edit our web map's code. VS Code is a free software from Microsoft that offers a wide range of features designed to make coding easier. Its extensive repository of extensions allows you to customize its base features according to the type of coding work you do. For example, since we need to view our web map in a local server, we will install a plugin called **Live Server**.

## Installing VS Code

You will need VS Code installed on your local computer for the hands-on portion of this workshop.

`To Do`{:.info}

1. Head to [code.visualstudio.com/download](https://code.visualstudio.com/Download){:target="\_blank"} and download the installer for your platform.
2. Install the software on your computer and open the application.

Once VS Code is installed, you are ready to proceed with installing your first extension.

## Live Server Extension

Once VS Code is installed, you can install the [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer){:target="\_blank"} extension. We'll use this to launch a local server, allowing us to view our web map as a working web application in a browser.

![Live Server VS Code Extension](../../assets/images/live-server.png "Live Server VS Code Extension")

`To Do`{:.info}

1. In VS Code, press `Ctrl+P` (Windows) or `Command+P` (Mac) to bring up the search console.
2. In the search console, type `ext install ritwickdey.liveserver` and press **Enter**.

Once installed, you should see the **"Go Live"** icon in the bottom right corner of the VS Code window.\

![Go Live!](../../assets/images/golive.png "Going Live!")

## Prettier Code Formatter Extension

Another very useful extension is [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode), which automatically formats your code into a consistant style and keeps your documents easy to read. It is "opinionated", meaning it has it's own set of rules for how your code should appear (i.e. `'single quotes'` vs `"double quotes"`), but these can be customized extensively in Prettier's settings.

![Prettier VS Code Extension](../../assets/images/prettier.png "Prettier VS Code Extension")

`To Do`{:.info}

1. In VS Code, press `Ctrl+P` (Windows) or `Command+P` (Mac) to bring up the search console.
2. In the search console, type `ext install esbenp.prettier-vscode` and press **Enter**. **Once installed and enabled, you may need to restart VS Code.**
3. Now we need to define Prettier as our default code formatter. Go to VS Code's **Preferences**, and select **Settings**.
4. In the Settings search box, search for `Editor: Default Formatter`, and select **Prettier - Code Formatter** (esbenp.prettier-vscode).
5. Now we need to set Prettier to format your code every time you save your file. In the Settings search box, search for `Editor: Format On Save` and make sure the box is selected.
