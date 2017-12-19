---
layout: page
title: Strategy Index
permalink: /strategy
---

These are all the wiki pages related to design strategy.

{% assign groups = site.strategy | group_by: "category" | sort: "name" %}
{% for group in groups %}
{% if group.name != "" %}
#### {{ group.name}}
{% else %}
{% if group.items %}
#### General
{%endif%}
{% else %}
{%endif%}
{% for item in group.items %}
[{{ item.title }}]({{ item.url }})
{%endfor%}
{%endfor%}
