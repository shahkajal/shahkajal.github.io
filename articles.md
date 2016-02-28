---
layout: default
title: Your New Jekyll Site
---
<!-- Articles by category-->
<div class="cat-tag-articles">
  <p class="pageTitle">Articles</p>
  <table >
  <td style="vertical-align:top">
    <img src="{{ site.baseurl}}/assets/img/catbig.png" /><h2>Category Wise</h2>
    {% assign sorted_categories= (site.categories | sort ) %}
    {% for cat in sorted_categories %}
      <h3 id="{{cat[0]}}-header"  class="next button__outline" onclick = "toggleList('{{cat[0]}}')" >{{ cat[0] }}</h3><br>
      <ul id="{{cat[0]}}" style="display: show;">
      {% assign sorted_posts= (cat[1] | sort : 'title')%}
      {% for post in sorted_posts %}
        <li><a href="{{ site.baseurl}}{{ post.url }}">{{ post.title }}</a></li>
      {% endfor %}
      </ul>
    {% endfor %}
  </td>
   <td style="vertical-align:top">
    <img src="{{ site.baseurl}}/assets/img/tagbig.png" /><h2>Tag Wise</h2>
    {% assign sorted_tags = (site.tags | sort ) %}
    {% for tag in sorted_tags %}
      <h3 id="{{tag[0]}}-header"class="next button__outline" onclick = "toggleList('{{tag[0]}}')" >{{ tag[0] }}</h3><br>
      <ul id="{{tag[0]}}" style="display: show;">
      {% assign sorted_posts=(tag[1]|sort:'title') %}
      {% for post in sorted_posts %}
        <li><a href="{{ site.baseurl}}{{ post.url }}">{{ post.title }}</a></li>
      {% endfor %}
      </ul>
    {% endfor %}
  </td>
</table>
</div>