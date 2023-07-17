---
layout: post
title: "Bitstamp API"
tags: [API, Bitstamp, GUI]
author_name: CJ
author_uri: ericcj24.github.io
---

I am making a simple GUI java app to graphically display Bitstamp’s
trading data through their [API](https://www.bitstamp.net/api/).

The java app utilizes apache’s [httpclient
library](http://hc.apache.org/httpclient-3.x/) to make http connection,
uses [Jackson](http://jackson.codehaus.org/) to bind JSON data to Java
class and/or generic containers.

~~The app also uses [jmathplot
libary](https://code.google.com/p/jmathplot/) to help plot the
data.~~  
After some considration, I switched my ploting tool to
[JFreeChart](http://www.jfree.org/jfreechart/) for its detailed
documentation.

~~Find it at my project
[repo](https://github.com/ericcj24/bitstamp.api.monitor).~~
I have also changed the new project to a newer
[repo](https://github.com/ericcj24/bitstamp.api.monitor1)

I will try to add more functionality in project in the following days :)

Cheers
