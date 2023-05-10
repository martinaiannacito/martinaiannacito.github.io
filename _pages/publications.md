---
layout: page
permalink: /publications/
title: Publications
description: 
nav: true
nav_order: 1

---
<!-- _pages/publications.md -->
<div class="publications">
<h1 class="post-title">Peer-reviewed journal</h1>
{% bibliography -f {{ site.scholar.bibliography }} -q @*[keywords=intjour || keywords=natjour]* %}

<h1 class="post-title">Preprints</h1>
{% bibliography -f {{ site.scholar.bibliography }} -q @*[keywords=report]* %}

<h1 class="post-title">Other works</h1>
{% bibliography -f {{ site.scholar.bibliography }} -q @*[keywords=thesis]* %}
<!-- {%- for y in page.years %}
{% bibliography -f myall -q @*[keywords={{new}}]* %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f {{ site.scholar.bibliography }} -q @*[year={{y}}]* %}
{% endfor %} -->

</div>
