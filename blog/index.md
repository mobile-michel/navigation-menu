---
title: All the menus
link-name: Menu list
description: This blog is about photography.
author: Michel Maillard
date: 2024-01-03
layout: layouts/default
tags: ["primary", "footer"]
css2: /assets/css/menu.css
---
{% for post in collections.blog %}
- [{{ post.data.title }}]({{ post.url | url }}) published on {{ post.data.date | date: '%d  %b %Y' }} on [this website]({{ post.data.url }})
{% endfor %}