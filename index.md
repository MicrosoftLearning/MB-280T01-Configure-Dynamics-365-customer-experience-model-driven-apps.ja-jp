---
title: 演習の手順
permalink: index.html
layout: home
---

# 演習

このページには、[Microsoft Learn](https://learn.microsoft.com) の Microsoft スキルアップ コンテンツに関連付けられている演習が記載されています

{% assign labs = site.pages | where_exp:"page", "page.url contains '/Instructions/Labs'" %} {% for activity in labs  %}
- [{{ activity.lab.title }}]({{ site.github.url }}{{ activity.url }}) {% endfor %}

