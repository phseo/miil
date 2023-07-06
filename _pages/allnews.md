---
title: "MIIL - News"
layout: textlay
excerpt: "MIIL - News"
sitemap: false
permalink: /allnews.html
---

### News

{% assign year_last = 0 %}
{% for article in site.data.news %}


{% if year_last != article.year %}
{% if year_last != 0 %}
</div>
</div>
{% endif %}
{% assign year_last = article.year %}
<div class="row">
<div class="col-sm-1 clearfix"><h4 style="margin-top: 0px;">{{ article.year }}</h4>
</div>
<div class="col-sm-11 clearfix">
{% assign div_opened = 1 %}
{% endif %}
<div class="row">
<div class="col-sm-3">
<img src="{{ site.url }}{{ site.baseurl }}/images/newspic/{{ article.img }}" style="width: 100%; aspect-ratio: 2/1; object-fit: contain; margin-bottom: 0px; margin-top: 0px;"/>
</div>
<div class="col-sm-9">
<span style="color: black;">{{ article.category }}</span><br />
{% if article.long_description != null %}
<span>{{ article.long_description }}</span>
{% else %}
<span>{{ article.description }}</span>
{% endif %}
<span style="color: #999; font-size: 80%;">{{ article.month }}, {{ article.year }}</span>
</div>
</div>
{% endfor %}

{% if div_opened == 1 %}
</div>
</div>
{% endif %}