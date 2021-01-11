---
layout: page
permalink: /publications/
title: Publications
---

# Publications 

{% assign thumbnail="left" %}

{% for pub in site.data.pubs %}

{% if pub.pdf and pub.software %}
  [**{{pub.title}}**]({{pub.url}})<br/>
  {{pub.authors}} <br/>
  <i>{{pub.journal}}</i> ({{pub.year}})<br/>
  [[PDF]({{pub.pdf}})] [[Software]({{pub.software}})]
{% elsif pub.pdf %}
  [**{{pub.title}}**]({{pub.url}})<br/>
  {{pub.authors}} <br/>
  <i>{{pub.journal}}</i> ({{pub.year}})<br/>
  [[PDF]({{pub.pdf}})] 
{% else %}
  [**{{pub.title}}**]({{pub.url}})<br/>
  {{pub.authors}} <br/>
  <i>{{pub.journal}}</i> ({{pub.year}})<br/>
{% endif %}

{% endfor %}