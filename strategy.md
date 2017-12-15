---
layout: page
title: Strategy Index
permalink: /strategy
---

These are all the wiki pages related to design strategy.

{% for item in site.strategy %}
  * [{{ item.title }}]({{ item.url }})
      * Categories
          {% for category in item.categories %}
          * {{ category }}
          {% endfor %}

{% endfor %}
