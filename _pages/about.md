---
title: "About"
layout: gridlay
sitemap: false
permalink: /about/
---

## About

<b>I'm looking forward to join a research team whose main target [research interests]({{ site.url }}{{ site.baseurl }}/interests) are</b>

{% for member in site.data.pi %}
<div class="jumbotron">
<div class="row">
<div class="col-sm-3">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" width="100%" style="max-width:250px"/>
</div>
<div class="col-sm-9 col-xs-12">
  <h4>{{ member.name }}</h4>
  <h5><i>{{ member.info }}</i></h5> 
  {% if member.email %}<a href="mailto:{{ member.email }}" target="_blank"><i class="fa fa-envelope-square fa-3x"></i></a> {% endif %}
  {% if member.cv %} <a href="{{ site.url }}{{ site.baseurl }}/{{ member.cv }}" target="_blank"><i class="ai ai-cv-square ai-3x"></i></a> {% endif %}
  {% if member.scholar %} <a href="{{ member.scholar }}" target="_blank"><i class="ai ai-google-scholar-square ai-3x"></i></a> {% endif %}
  {% if member.github %} <a href="{{ member.github }}" target="_blank"><i class="fa fa-github-square fa-3x"></i></a> {% endif %}
  {% if member.researchgate %} <a href="{{ member.researchgate }}" target="_blank"><i class="ai ai-researchgate-square ai-3x"></i></a> {% endif %}

  <ul style="overflow: hidden">
  {% if member.education1 %} <li> {{ member.education1 | replace: "-","&#8211;"}} </li> {% endif %}
  {% if member.education2 %} <li> {{ member.education2 | replace: "-","&#8211;"}} </li> {% endif %}
  {% if member.education3 %} <li> {{ member.education3 | replace: "-","&#8211;"}} </li> {% endif %}
  {% if member.education4 %} <li> {{ member.education4 | replace: "-","&#8211;"}} </li> {% endif %}
  {% if member.education5 %} <li> {{ member.education5 | replace: "-","&#8211;"}} </li> {% endif %}
  </ul>
</div>
</div>
</div>
{% endfor %}

{% if site.data.collaborators %}
<div class="jumbotron">
### Collaborators
<ul>
{% for collab in site.data.collaborators %}
 <li> <a href="{{collab.url}}" target="_blank">{{collab.name}}</a> ({{collab.title}})</li>
{% endfor %}
</ul>
</div>
{% endif %}

{% if site.data.coursework %}
<div class="jumbotron">
### Important Coursework
<ul>
{% for coursework in site.data.coursework %}
 <li> {{ coursework.name }} </li>
{% endfor %}
</ul>
</div>
{% endif %}

{% if site.data.softwares %}
<div class="jumbotron">
### Softwares
<ul>
{% for softwares in site.data.softwares %}
 <li> {{ softwares.name }} </li>
{% endfor %}
</ul>
</div>
{% endif %}

{% if site.data.awards %}
<div class="jumbotron">
### Awards
<ul>
{% for award in site.data.awards %}
 <li> {{ award.name | replace: "-","&#8211;"}} </li>
{% endfor %}
</ul>
</div>
{% endif %}