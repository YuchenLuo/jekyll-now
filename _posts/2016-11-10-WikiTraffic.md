---
layout: post
title: Wiki Traffic
---

I was digging around for some real world web traffic stats to help validate some machine learning capabilities under development and came across wikipedia's dataset.
I did some work on aggregate hourly page views and thought it would be cool to share some of the results.

---
![alt tag](https://raw.githubusercontent.com/YuchenLuo/yuchenluo.github.io/master/images/2016-11-10-WikiTraffic.fig1.png)
We can see that the traffic patterns are quite predictable and highly periodic, with pronounced daily and weekly cycles.  I did an autoregression and a fourier transform to extract the frequency distribution.  

Based on identified periods, the appropriate time window size for ML regression operations can be selected.  Experiments with random forest based regressor resulted in about 4% deviation for 24 hour predicitons.

[Code for the project here](https://github.com/YuchenLuo/WikiTraffic)
