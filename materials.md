---
layout: page
title: Materials Science
permalink: /materials/
group: "navigation"
---
My prior research in materials science from undergrad through early years of grad school was at the intersection of materials informatics and solid mechanics. You can read about the various projects here:
* [Process design for obtaining useful material structures and properties](#process)
* [Lawrence Livermore](#LLNL)


[Publications and Presentations](#pubspres)

### <a name="process"> Process design for obtaining useful material structures and properties </a>
Correlating microstructural features to processes is an essential first step to answer the difficult problem of process sequence design. The inverse problem of designing processing stages that lead to a desired texture or texture-dependant property is addressed here. Preliminary results indicate that different points in the database are mapped to different regions in the latent space based on the last process in any sequence. The present work will expand on that result to use process sequences as an input to the model, and further deconstruct process - structure linkages.

{% include image.html url="/images/processdesign.png" width="700px" align="center" %}


{% assign thumbnail="left" %}

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
