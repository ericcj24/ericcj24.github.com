---
layout: post
title: "A Little Note on Renren API"
tags: [API]
author_name: CJ
author_uri: ericcj24.github.io
---

### Overview

Renren is popular Chinese social website. This post introduces an easy
way, and yet different from Douban’s photo uploading previews
introduced, to upload photo to your Renren albums with Python requests.

### Python code

{% highlight python %}
import requests
access_token = YOUR_ACCESS_TOKEN
fh = open('YOUR_IMAGE_FILE_PATH','rb')
files = {'file':fh}
url = 'https://api.renren.com/v2/photo/upload'
text = 'WORDS_TO_DESCRIBE_YOUR_PHOTO' 
v = {'description':text, 'albumId':YOUR_ALBUMID, 'access_token':access_token}
r = requests.post(url, data=v, files=files)
r.status_code # would give you the http call result
r_json = r.json() # would give the result in json format
{% endhighlight %}

Things to take extra care are: use ‘data’ to pass your dictionary when
make a POST call with requests, Multipart-Encoded File should be put in
a dictionary and pass to ‘files’.  
cheers!
