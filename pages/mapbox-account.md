---
layout: article
title: Mapbox Account Setup
permalink: /setting-up/mapbox-account/
aside:
  toc: true
sidebar:
  nav: webmap-workshop
---

For this workshop, we're going to use the web map library **Mapbox GL JS** for our hands-on section to build a web map. Mapbox offers a robust suite of tools for building custom web-native mapping applications. The company has been around since the early 2010s and has remained a leader in offering innovative toolkits for web cartographers and web map developers.

## Mapbox GL JS Pricing

Mapbox GL JS is not entirely free, but it offers a generous free tier, often sufficient for testing and experimenting with a limited number of datasets and maps. More details about pricing can be found on Mapbox's [pricing model description page](https://www.mapbox.com/pricing#map-loads-for-web) and the [Invoices and Billing](https://docs.mapbox.com/accounts/guides/invoices/#what-to-expect) guide.

The hands-on portion of this workshop will remain within the free tier, so no payment information is required.  
{:.info}

## Create Your Mapbox Account

Your Mapbox account will give you access to all the resources offered by Mapbox.

`To Do`{:.info}

1. Head to [account.mapbox.com/auth/signup](https://account.mapbox.com/auth/signup/).
2. Select "Individual" for account type, fill in your information, agree to the terms, and submit.
3. Check your inbox for a confirmation email and verify your account.
4. Add your address for billing information – you don't need to provide payment information!

Once you've completed this step, you'll have access to your [Mapbox account dashboard](https://console.mapbox.com/).

![Mapbox Account Dashboard](../../assets/images/mapbox-account-dashboard.png "Mapbox Account Dashboard")

## Create Your Mapbox Access Token

Your Mapbox access token will provide API access to Mapbox GL JS so that we can build and test our maps locally and eventually deploy them to the web. For this workshop, we will create a new access token for testing, which you can optionally delete afterward. Mapbox's documentation provides [more information about securely using your access tokens](https://docs.mapbox.com/help/troubleshooting/how-to-use-mapbox-securely/#access-tokens).

`To Do`{:.info}

1. From your [Mapbox account dashboard](https://console.mapbox.com/), click on **"Tokens"** in the left navigation.
2. At the top of the page, click the button **"+ Create a token"**.
3. Give your token a name such as **_LDW2025-test_**.
4. Optional: If you already know where you will be hosting your map, provide a URL restriction.
5. Click the **"Create token"** button and confirm your password.
