---
title: "News"
layout: textlay
sitemap: false
permalink: /allnews.html
---

## News

<div class="jumbotron">
{% for news in site.data.news %}
<b>{{ news.date }}</b>

{{ news.headline }}
{% endfor %}
</div>
