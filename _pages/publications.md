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
<div class="well">
<a href="{{ publi.link }}" target="_blank">**{{ publi.title }}**</a> 
<br />
{{ publi.authors }}<br />
In <i>{{ publi.venue }}</i>
</div>
{% endfor %}
</div>
</div>
