---
layout: page
permalink: /talks/
title: Talks
description: 
nav: true
nav_order: 1

---
<!-- _pages/publications.md -->
<div class="publications">
<h1 class="post-title">Conferences</h1>
{% bibliography -f {{ site.scholar.bibliography }} -q @*[keywords=intconf || keywords=natconf]* %}

<h1 class="post-title">Workshops</h1>
{% bibliography -f {{ site.scholar.bibliography }} -q @*[keywords=workshop]* %}

<h1 class="post-title">Seminar</h1>
{% bibliography -f {{ site.scholar.bibliography }} -q @*[keywords=seminar]* %}
<!-- {%- for y in page.years %}
{% bibliography -f myall -q @*[keywords={{new}}]* %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f {{ site.scholar.bibliography }} -q @*[year={{y}}]* %}
{% endfor %} -->

</div>
