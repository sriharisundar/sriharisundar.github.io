---
layout: page
title: Publications
permalink: /pubs/
group: "navigation"
---


## Publications (peer reviewed)

{% assign thumbnail="left" %}
### Materials research
{% for pub in site.data.pubs.pubs.materials %}
{% if pub.image %}
{% include image.html url=pub.image caption="" height="100px" align=thumbnail %}
{% endif %}
[**{{pub.title}}**]({% if pub.internal %}{{pub.url | prepend: site.baseurl}}{% else %}{{pub.url}}{% endif %})<br />
{{pub.author}}<br />
*{{pub.journal}}*
{% if pub.note %} *({{pub.note}})*
{% endif %} *{{pub.year}}* {% if pub.doi %}[[doi]({{pub.doi}})]{% endif %}
{% if pub.arxiv %}[[arxiv]({{pub.arxiv}})]{% endif %}
{% if pub.data %}[[data]({{pub.data}})]{% endif %}
{% if pub.media %}<br />Media: {% for article in pub.media %}[[{{article.name}}]({{article.url}})]{% endfor %}{% endif %}

{% endfor %}
