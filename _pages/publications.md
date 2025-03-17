---
layout: page
permalink: /publications/
title: Publications
description: 
years: [2025, 2022, 2021, 2019]
nav: true
nav_order: 1

---
<!-- _pages/publications.md -->
<div class="publications">

<h1 class="post-title">Preprints</h1>
{%- for y in page.years %}
  {% capture bib_count %} 
    {% bibliography_count -f {{ site.scholar.bibliography }} -q @*[keywords=report && year={{y}}]* %}
  {% endcapture %}
  {% assign bib_count = bib_count | plus: 0 %}
  {% if bib_count > 0 %}
    <h2 class="year">{{y}}</h2>
    {% bibliography -f {{ site.scholar.bibliography }} -q @*[keywords=report && year={{y}}]* %}
  {% endif %}
{% endfor %}

<h1 class="post-title">Peer-reviewed journal</h1>
{%- for y in page.years %}
  {% capture bib_count1 %} 
    {% bibliography_count -f {{ site.scholar.bibliography }} -q @*[keywords=intjour && year={{y}}]* %}
  {% endcapture %}
  {% capture bib_count2 %}
    {% bibliography_count -f {{ site.scholar.bibliography }} -q @*[keywords=natjour && year={{y}}]* %}
  {% endcapture %}
  {% assign bib_count1 = bib_count1 | plus: 0 %}
  {% assign bib_count2 = bib_count2 | plus: 0 %}
  {% if bib_count1 > 0 or bib_count2 > 0 %}
    <h2 class="year">{{y}}</h2>
    {% bibliography -f {{ site.scholar.bibliography }} -q @*[tag=journal && year={{y}}]*  %}
  {% endif %}
{% endfor %}


<h1 class="post-title">Other works</h1>
{%- for y in page.years %}
  {% capture bib_count %} 
  {% bibliography_count -f {{ site.scholar.bibliography }} -q @*[keywords=thesis && year={{y}}]* %}
  {% endcapture %}
  {% assign bib_count = bib_count | plus: 0 %}
  {% if bib_count > 0 %}
    <h2 class="year">{{y}}</h2>
    {% bibliography -f {{ site.scholar.bibliography }} -q @*[keywords=thesis && year={{y}}]* %}
  {% endif %}
{% endfor %}
</div>
