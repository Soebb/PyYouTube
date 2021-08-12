# PyYouTube 

<p align="center">
  <a href="https://www.python.org">
    <img src="https://tg-link.herokuapp.com/dl/0/AgADhawxGz-ZkVQ.jpg">

  </a>


Get Video Data from YouTube link 

## Installation 
```bash
pip install PyYouTube
```

## How to use it ?
#### Get Videos Data 

```python
from pyyoutube import Data
yt = Data("https://youtu.be/HhHzCfrqsoE")

id = yt.id
title = yt.title
thumbnails = yt.thumbnails
views = yt.views
likes = yt.likes
dislikes = yt.dislikes
publishdate = yt.publishdate
category = yt.category
channel_name = yt.channel_name
subscriber = yt.subscriber
```

</details>

#### Search Videos
 Get videos link 
```python 
from pyyoutube import Search
yt = Search("ln technical")
print(yt.videos)
```
<details>
  <summary><b>Example Results</summary>
<br/>

```bash
['https://youtu.be/jEnlga0hYyY', 'https://youtu.be/jEnlga0hYyY', 'https://youtu.be/Fxj5ZpaNq24', 'https://youtu.be/bAyh6FU01ho', 'https://youtu.be/DPCN3abXmsc', 'https://youtu.be/ros6m2BBI84', 'https://youtu.be/jEnlga0hYyY', 'https://youtu.be/hbtfaAx4bBE', 'https://youtu.be/qvBt04Q60Mg', 'https://youtu.be/1T3rAZH4rmw']
```

</details>

 Get Video Data 
```python 
from pyyoutube import Search ,Data 
yt = Search("ln technical" , limit = 2).videos
for vid in yt:
  res = Data(vid).data
  print(res)
```
<details>
  <summary>Example Results</summary>
<br/>

```json
[
  {
    "id": "jEnlga0hYyY",
    "title": "Tutorial 1 - History of Infor ERP LN",
    "thumbnails": "https://i.ytimg.com/vi/jEnlga0hYyY/hqdefault.jpg?sqp=-oaymwEiCKgBEF5IWvKriqkDFQgBFQAAAAAYASUAAMhCPQCAokN4AQ==\\u0026rs=AOn4CLC9vnXpG2XmDpNfwZHEBMdo8GVf-A",
    "views": "9957",
    "likes": "80",
    "dislikes": "1",
    "publishdate": "2017-11-07",
    "category": "Education",
    "channel_name": "Infor LN Technical Trainer",
    "subscriber": "935 subscribers"
  },
  {
    "id": "jEnlga0hYyY",
    "title": "Tutorial 1 - History of Infor ERP LN",
    "thumbnails": "https://i.ytimg.com/vi/jEnlga0hYyY/hqdefault.jpg?sqp=-oaymwEiCKgBEF5IWvKriqkDFQgBFQAAAAAYASUAAMhCPQCAokN4AQ==\\u0026rs=AOn4CLC9vnXpG2XmDpNfwZHEBMdo8GVf-A",
    "views": "9957",
    "likes": "80",
    "dislikes": "1",
    "publishdate": "2017-11-07",
    "category": "Education",
    "channel_name": "Infor LN Technical Trainer",
    "subscriber": "935 subscribers"
  }
]
```
</details>

#### Search Limits Video 
```python 
from pyyoutube import Search ,Data 
yt = Search("ln technical", limit = 3).videos
print(yt)
```
>Example Result 
```bash
['https://youtu.be/jEnlga0hYyY', 'https://youtu.be/jEnlga0hYyY', 'https://youtu.be/Fxj5ZpaNq24']
```
## License 
Copyright (c) 2021 Lntechnical

This repository is licensed under the MIT license.
