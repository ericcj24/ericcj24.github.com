---
layout: post
title: "Bitstamp API Monitor on Android with Websocket"
tags: [API, Bitstamp, Android, websocket]
author_name: CJ
author_uri: ericcj24.github.io
---

Hello there!

Things are getting more interesting! I am trying Bitstamp's websocket api now. Basicly, it uses a third-party tool called [Pusher](http://pusher.github.io/pusher-java-client/) to open a websocket to stream all transactions in real time to your device.

Here are some specs of this version of my app:
DrawerLayout
Fragments: 3, for each of transaction, orderbook, and ticker
Service: 1, in it: AsyncTask fired to pull data from Bitstamp API and store to database if first time use; after that, use pusher to open socket to listen for the streaming data, and store new data to database. This technique used both for transaction and orderbook. another handler for repeatly updating ticker info
Sqlite: 3, for each of the transaction, orderbook, and ticker
ContentProvider: 3, for each of transaction, orderbook and ticker, monitoring the change in database, and presenting the new data to fragments
sharedPreference
TODO: internet connection check on start, and resume pusher after internet reconnected, check user setting, with connectivityManager.getActiveNetworkInfo(), isConnected(), public static final String CONNECTIVITY_ACTION.
first time open without internet, would cause transaction db to be empty afterwards (bulkinsert never called)

repo [here](https://github.com/ericcj24/bitstamp-websocket-v0)

the app is in [Google Play Store](https://play.google.com/store/apps/details?id=edu.illinois.jchen93.bitstampwebsockettest) now

I will try to add more functionality in project in the following days :)


Cheers
