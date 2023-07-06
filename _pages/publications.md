---
title: "MIIL - Publications"
layout: gridlay
excerpt: "MIIL -- Publications."
sitemap: false
permalink: /publications/
---


### Publications


<div class="row">
<div class="col-sm-1 clearfix"><h4>2023</h4>
</div>
<div class="col-sm-11 clearfix">

{% for publi in site.data.publist %}
<div class="well" style="padding-top: 5px; padding-bottom: 5px; padding-right: 10px; padding-left: 10px; margin-bottom: 3px;">
<p style="margin-bottom: 0px;">
<a href="{{ publi.link }}" target="_blank">**{{ publi.title }}**</a> 
<br />
{{ publi.authors }}<br />
In <i>{{ publi.venue }}</i>
</p>
</div>
{% endfor %}
</div>
</div>

{% assign year_last = 0 %}
{% for publi in site.data.publist %}


{% if year_last != publi.year %}
{% if year_last != 0 %}
</div>
</div>
{% endif %}
{% assign year_last = publi.year %}
<div class="row">
<div class="col-sm-1 clearfix"><h4>{{ publi.year }}</h4>
</div>
<div class="col-sm-11 clearfix">
{% assign div_opened = 1 %}
{% endif %}

<div class="well" style="padding-top: 5px; padding-bottom: 5px; padding-right: 10px; padding-left: 10px; margin-bottom: 3px;">
<p style="margin-bottom: 0px;">
<a href="{{ publi.link }}" target="_blank">**{{ publi.title }}**</a> 
<br />
{{ publi.authors }}<br />
In <i>{{ publi.venue }}</i>
</p>
</div>
{% endfor %}

{% if div_opened == 1 %}
</div>
</div>
{% endif %}