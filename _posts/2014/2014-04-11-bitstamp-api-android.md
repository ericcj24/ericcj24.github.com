---
layout: post
title: "Bitstamp API Client on Android"
tags: [API, Bitstamp, Android]
author_name: CJ
author_uri: ericcj24.github.io
---

I am making a simple Android app to graphically display Bitstamp's trading data through their [API](https://www.bitstamp.net/api/)

The app utilizes an open source Android charting library called [Androidplot](http://androidplot.com/), and a slide menu from [here](https://github.com/dmitry-zaitsev/AndroidSideMenu/).
The app features AlarmManager to repeatly firing IntentService, the later's working thread would be pulling data from Bitstamp API (making http calls), and if there are new data, update database (sqlite) accordingly, once database is updated, a Broadcast is sent to the main UI thread and updates the chart.

<strike>[Check it out](https://github.com/ericcj24/simple-bitstamp-api-androidclient)</strike>
<strike>new repo [here](https://github.com/ericcj24/bitstamp-api-android2) </strike>
I have been exploiting with different designs to approach this problem, [here](https://github.com/ericcj24/bitstamp-api-android3) is the newest version, check it out :)


I will try to add more functionality in project in the following days :)


Cheers
