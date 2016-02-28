---
layout: default
title: Tags
---
<!-- Articles by tags-->
<div id="articles">
  <p class="pageTitle">Tags</p>
  	{% assign sorted_tags = (site.tags | sort ) %}
    {% for tag in sorted_tags %}
      <a href= "{{ site.baseurl}}/articles/#{{tag[0]}}-header" class="next button__outline" <h3>{{ tag[0] }}</h3></a>
    {% endfor %}
</div>