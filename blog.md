---
layout: page
title: Blog
permalink: /blog/
---

I use this space to talk about things I find useful, my experiences, and some thoughts I think. My intentions for having this blog are: 1) record things for myself, 2) share things I learn - someone could benefit as I have from other such blogs, 3) for me to just write. I don't think having comments in these posts will be warranted, and this may change, but if you have any comments/suggestions which will add value to them please [let me know!](/contact) 

Posts (maybe ;) ) coming soon!

<ul class="listing">
{% for post in site.posts %}
  {% capture y %}{{post.date | date:"%Y"}}{% endcapture %}
  {% if year != y %}
    {% assign year = y %}
    <li class="listing-seperator">{{ y }}</li>
  {% endif %}
  <li class="listing-item">
    <time datetime="{{ post.date | date:"%Y-%m-%d" }}">{{ post.date | date:"%Y-%m-%d" }}</time>
    <a href="{{ post.url | prepend: site.baseurl }}" title="{{ post.title }}">{{ post.title }}</a>
  </li>
{% endfor %}
</ul>
