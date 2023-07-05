---
title: "MIIL - Team"
layout: gridlay
excerpt: "MIIL: Team members"
sitemap: false
permalink: /members/ 
---

<!---
# Group Members

 **We are  looking for new PhD students, Postdocs, and Master students to join the team** [(see openings)]({{ site.url }}{{ site.baseurl }}/vacancies) **!**


Jump to [staff](#staff), [master and bachelor students](#master-and-bachelor-students), [alumni](#alumni), [administrative support](#administrative-support), [lab visitors](#lab-visitors). 
--->
 
### Faculty
{% assign number_printed = 0 %}
{% for member in site.data.professors %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left; margin-top: 10px; " />
  {% if member.homepage != null %}
  <span class="member_name"><a href="{{ member.homepage }}" target="_blank">**{{ member.name }}**<span class="icon-link"></span></a></span><br/>
  {% else %}
  <span class="member_name"><a>**{{ member.name }}**</a></span><br/>
  {% endif %}
  <span class="position" style="font-style: italic;">{{ member.position }}</span><br/>
  <span class="email" style="color: #888;">{{ member.email }}</span> 
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}


### Students
{% assign number_printed = 0 %}
{% for member in site.data.students %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left; margin-top: 10px; " />
  {% if member.homepage != null %}
  <span class="member_name"><a href="{{ member.homepage }}" target="_blank">**{{ member.name }}**<span class="icon-link"></span></a></span><br/>
  {% else %}
  <span class="member_name"><a>**{{ member.name }}**</a></span><br/>
  {% endif %}
  <span class="email" style="color: #888;">{{ member.email }}</span> <br/>
  <span class="interests" style="font-style: italic;">{{ member.interests }}</span>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}


### Interns
{% assign number_printed = 0 %}
{% for member in site.data.interns %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left; margin-top: 10px; " />
  {% if member.homepage != null %}
  <span class="member_name"><a href="{{ member.homepage }}" target="_blank">**{{ member.name }}**<span class="icon-link"></span></a></span><br/>
  {% else %}
  <span class="member_name"><a>**{{ member.name }}**</a></span><br/>
  {% endif %}
  <span class="email" style="color: #888;">{{ member.email }}</span> <br/>
  <span class="interests" style="font-style: italic;">{{ member.interests }}</span>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 6 %}
{% if even_odd != 0 %}
</div>
{% endif %}


### Alumni

{% assign number_printed = 0 %}
{% for member in site.data.alumni %}

{% assign even_odd = number_printed | modulo: 6 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-2 clearfix">
  {% if member.homepage != null %}
  <span class="member_name"><a href="{{ member.homepage }}" target="_blank">**{{ member.name }}**<span class="icon-link"></span></a></span><br/>
  {% else %}
  <span class="member_name"><a>**{{ member.name }}**</a></span><br/>
  {% endif %}
  <span class="degree_year" style="font-style: italic;">{{ member.degree }}, {{ member.year }}</span><br/>
  <span class="career" style="color: #888;">{{ member.career }}</span> 
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 5 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}