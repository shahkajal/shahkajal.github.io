---
layout: default
title: Categories
---
<!-- Articles by category-->
<div id="articles">
  <p class="pageTitle">Categories</p>
  {% assign sorted_categories= (site.categories | sort ) %}
    {% for cat in sorted_categories %}
      <a href="{{ site.baseurl}}/articles/#{{cat[0]}}-header"><h3 class="next button__outline" >{{ cat[0] }}</h3></a>
    {% endfor %}
</div>