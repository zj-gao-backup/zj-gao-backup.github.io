---
layout: page
permalink: /publications/
title: publications
nav: publications
description: <nobr><em>*</em></nobr> denotes equal contribution and joint lead authorship.
years: [2024, 2023, 2021, 2020, 2019, 2017, 2015]
---

<br/>
{% for y in page.years %}
  <div class="row m-0 p-0" style="border-top: 1px solid #ddd; flex-direction: row-reverse;">
    <div class="col-sm-1 mt-2 p-0 pr-1">
      <h3 class="bibliography-year">{{y}}</h3>
    </div>
    <div class="col-sm-11 p-0">
      {% bibliography -f papers -q @*[year={{y}}]* %}
    </div>
  </div>
{% endfor %}
