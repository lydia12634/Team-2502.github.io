---
layout: page
title: Meta Index
permalink: /wiki
---

These are all the wiki pages related to adding to and maintaining the wiki.

{% assign groups = site.wiki | group_by: "category" | sort: "name" %}
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
