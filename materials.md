---
layout: page
title: Materials Science
permalink: /materials/
group: "navigation"
---
My prior research in materials science from undergrad through early years of grad school was at the intersection of materials informatics and solid mechanics. 

### <a name="pubspres"> Publications and Presentations </a>
{% for pub in site.data.publications.materials %}
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

