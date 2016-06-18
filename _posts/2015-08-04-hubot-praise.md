---
layout: post
title:  "Hubot praise"
date:   2015-08-04
excerpt: "Api wrapper for the Exact Online API"
project: true
feature: "http://i.giphy.com/diKF8kxuomAxy.gif"
tag:
- hubot
- javascript
- slack
- open-source
- hubot
- joyofcoding
comments: true
---

<center><b>hubot-praise</b> is a Hubot plugin for praising your colleagues.</center>

Do you use slack or hipchat or any other messaging platform that supports hubot and you wanna compliment or thank or just acknowledge the people you communicate with? Use hubot-praise, they get a random message telling them they're awesome with an amazing GIF with it.

## How to use

Between current user @cortana and @masterchief

```bash
cortana> hubot high five @cortana
hubot> you can’t high five yourself. that’s just clapping
cortana> hubot praise @masterchief
hubot> @cortana high fives @masterchief
hubot> The world is a better place with you around, @masterchief
hubot> http://i.giphy.com/3o85xr46bezqkTazsc.gif
```

![yougotitdude](http://i.giphy.com/3o85xr46bezqkTazsc.gif)

## You wanna help?

There are tests! So run them when you are working on the code. Other than that you know the drill, fork it, pull request it and tada!

### Add more gifs!

We can always use more gifs so if you find an awesome high five gif thats not in here already please add it!

### Add more praise!

You can also add a new praise line, something you would say to someone who's being totally awesome!

## Authors and Contributors

@marthyn
@rolfvandekrol

## Support

You can always open up an issue [here](https://github.com/Marthyn/hubot-praise/)

## Inspiration

First and foremost, inspiration came from [Ben Straub](https://github.com/ben). He gave a talk at (Joy of coding about [Hubot](https://twitter.com/joyofcoding). We left out the gift cards for now though :smile:. You can view the slides [here](http://ben.straub.cc/talks/robots/)

This script was heavily inspired by [hubot-motivate](https://github.com/hubot-scripts/hubot-motivate) and [hubot-highfive](https://github.com/wjbeckett/hubot-highfive). I used some code and some images and texts, but extended it with storage and more images and texts.

{% capture images %}
http://i.imgur.com/LgXev.gif
http://stream1.gifsoup.com/view1/1148368/top-gun-high-five-o.gif
http://i.giphy.com/diKF8kxuomAxy.gif
http://i.giphy.com/aT8xFndP3Kpeo.gif
http://i.giphy.com/9o67upvAnOqRy.gif
http://i.giphy.com/C4lSxWjqSJLfG.gif
http://i.giphy.com/C9xw4gfOpfW6c.gif
http://i.giphy.com/gXBmPuqnc4cve.gif
http://i.giphy.com/hxnQBgpL29lyU.gif
http://i.giphy.com/112VS6QqBw52Ks.gif
http://i.giphy.com/cJgkhpLgsuTkY.gif
http://i.giphy.com/1HPzxMBCTvjMs.gif
http://i.giphy.com/Dwu7IpRyVA5Nu.gif
http://i.giphy.com/LdnaND03GRE9q.gif
http://i.giphy.com/NjOk8dfSlUv1S.gif
http://i.giphy.com/RLn2w2fLpcwTu.gif
http://i.giphy.com/rM9Cl7MZphBqU.gif
http://i.giphy.com/X7xPZ5jUGLUrK.gif
http://i.giphy.com/4SS0kfzRqfBf2.gif
http://i.giphy.com/IxJMT1ugyBMdy.gif
http://i.giphy.com/DohrJX1h2W5RC.gif
http://i.giphy.com/mHEes6Quf8XK0.gif
http://i.giphy.com/10LKovKon8DENq.gif
http://i.giphy.com/zl170rmVMCpEY.gif
http://i.giphy.com/3tpinSPvGf8MU.gif
http://i.giphy.com/Ch7el3epcW3Wo.gif
http://i.giphy.com/djc4SxBZtVHhe.gif
http://i.giphy.com/3o85xr46bezqkTazsc.gif
http://i.giphy.com/VtLkuCkObNC6c.gif
http://i.giphy.com/10LNj580n9OmiI.gif
http://i.giphy.com/1GlDW1HBD3q2A.gif
http://i.giphy.com/tcGxgQGmE2d2w.gif
http://i.giphy.com/xfqZR7wRwOIx2.gif
{% endcapture %}
{% include gallery images=images caption="GIF AWESOMENESS (submit a PR if you miss one)" cols=3 %}
