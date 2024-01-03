---
layout: page
permalink: /talks/
title: Talks
years: [2023, 2022, 2021, 2020, 2019]
description: 
nav: true
nav_order: 1

---
<!-- _pages/publications.md -->
<div class="publications">
<h1 class="post-title">Conferences</h1>
{%- for y in page.years %}
  {% capture bib_count %} 
    {% bibliography_count -f {{ site.scholar.bibliography }} -q @*[tag=conference && year={{y}}]* %}
  {% endcapture %}
  {% assign bib_count = bib_count | plus: 0 %}
  {% if bib_count > 0 %}
    <h2 class="year">{{y}}</h2>
    {% bibliography -f {{ site.scholar.bibliography }} -q @*[tag=conference && year={{y}}]* %}
    {% endif %}
{% endfor %}

<h1 class="post-title">Workshops</h1>
{%- for y in page.years %}
  {% capture bib_count %} 
    {% bibliography_count -f {{ site.scholar.bibliography }} -q @*[keywords=workshop && year={{y}}]* %}
  {% endcapture %}
  {% assign bib_count = bib_count | plus: 0 %}
  {% if bib_count > 0 %}
    <h2 class="year">{{y}}</h2>
    {% bibliography -f {{ site.scholar.bibliography }} -q @*[keywords=workshop && year={{y}}]* %}
    {% endif %}
{% endfor %}

<h1 class="post-title">Seminar</h1>
{%- for y in page.years %}
  {% capture bib_count %} 
    {% bibliography_count -f {{ site.scholar.bibliography }} -q @*[keywords=seminar && year={{y}}]* %}
  {% endcapture %}
  {% assign bib_count = bib_count | plus: 0 %}
  {% if bib_count > 0 %}
    <h2 class="year">{{y}}</h2>
    {% bibliography -f {{ site.scholar.bibliography }} -q @*[keywords=seminar && year={{y}}]* %}
    {% endif %}
{% endfor %}
</div>
