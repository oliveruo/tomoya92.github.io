---
layout: post
title: underscore自定义函数，处理数据
date: 2016-07-22 01:15:01
categories: javascript学习笔记
tags: javascript template
---

* content
{:toc}

引入js

```
<script src="http://cdn.bootcss.com/underscore.js/1.8.3/underscore-min.js"></script>
```

创建自定义函数

```
_.template.formatdate = function (stamp) {
    var d = new Date(stamp), // or d = new Date(date)
            fragments = [
                d.getFullYear(),
                d.getMonth() + 1,
                d.getDate()
            ];
    return fragments.join('-');
};
```




调用

```
<%=_.template.formatdate(data)%>
```