---
layout: post
category: "linux"
title:  "linux下while删除多个文件显示进度"
tags: [linux]
---
linux下while删除多个文件显示进度

####linux下使用while read line去逐行删除的时候看到不进度
####在echo的时候加上参数，如下
{% highlight bash %}
i=0;cat rmdir | while read line ;do ((i++));rm $line;echo -ne "\033[20D\033[K$i/1352" ;done
{% endhighlight %}

####
每删除1个会加1,显示：<br/>
{% highlight bash %}
1/1352
15/1352
1352/1352
{% endhighlight %}
