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
<div class="col-sm-1 clearfix"><h4>{{ article.year }}</h4>
</div>
<div class="col-sm-11 clearfix">
{% assign div_opened = 1 %}
{% endif %}

<div class="col-sm-3">
<img src="{{ site.url }}{{ site.baseurl }}/images/newspic/{{ article.img }}" width="100%"/>
</div>

<div class="col-sm-9">
<!-- style="padding-top: 5px; padding-bottom: 5px; padding-right: 10px; padding-left: 10px; margin-bottom: 3px; box-shadow: none;"> -->
<p style="margin-bottom: 0px;">
<span style="color: black;">{{ article.category }}</span><br /><span>
{% if article.long_description != null %}
{{ article.long_description | markdownify }}
{% else %}
{{ article.description | markdownify }}
{% endif %}
</span>
</p>
</div>
{% endfor %}

{% if div_opened == 1 %}
</div>
</div>
{% endif %}