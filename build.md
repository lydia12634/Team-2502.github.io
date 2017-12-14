---
layout: page
title: Build Index
permalink: /build
---

These are all the wiki pages related to the fabrication and design of the robot, more colloquially known as "build stuff".

{% for item in site.build %}
  * [{{ item.title }}]({{ item.url }})
{% endfor %}
