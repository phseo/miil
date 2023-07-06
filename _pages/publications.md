---
title: "MIIL - Publications"
layout: gridlay
excerpt: "MIIL -- Publications."
sitemap: false
permalink: /publications/
---


### Publications

{% for publi in site.data.publist %}

<div class="row">
<div class="col-sm-1 clearfix"><h4>2023</h4>
</div>
<div class="col-sm-11 clearfix">
<div class="well">
<pubtit>{{ publi.title }}</pubtit>
<p><em>{{ publi.authors }}</em></p>
<pubtit>{{ publi.title }}</pubtit>

<a href="{{ publi.link }}" target="_blank">**{{ publi.title }}**</a> 
<br />
{{ publi.authors }}<br />
In <i>{{ publi.venue }}</i>
</div>
</div>
</div>

{% endfor %}