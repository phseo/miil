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
      <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" width="33%" style="float: left" />
      <p>{{ publi.description }}</p>
      <p><em>{{ publi.authors }}</em></p>
      <p><strong><a href="{{ publi.link.url }}">{{ publi.link.display }}</a></strong></p>
      <p class="text-danger"><strong> {{ publi.news1 }}</strong></p>
      <p> {{ publi.news2 }}</p>
    </div>
  </div>
</div>

{% endfor %}