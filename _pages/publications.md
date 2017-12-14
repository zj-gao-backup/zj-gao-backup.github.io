---
layout: page
permalink: /publications/
title: publications
description: <em class="star">*</em> denotes equal contribution and joint lead authorship.
years: [2017, 2015]
---

{% for y in page.years %}
  <h3 class="bibliography-year">{{y}}</h3>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}
