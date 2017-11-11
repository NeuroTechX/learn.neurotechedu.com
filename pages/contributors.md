---
layout: page-fullwidth
title: "Contributors"
teaser: "These are the people who made NeuroTechEDU what it is today."
header:
    image_fullwidth: "header_drop.jpg"
permalink: "/contributors/"

---


{% assign track_index = 0 %}

{% for member in site.data.contributors %}
{%capture track_index %}{{forloop.index0 | modulo: 2}}{%endcapture%}
{% if track_index == "1" %}
<div class="row">
{% endif %}

<div class="medium-6 columns contributor" markdown="1">
### {{ member.name }}
#### Roles:
{% for role in member.roles %}
* {{ role }}
{% endfor %}
#### Contributed to:
{% for contribution in member.contributed %}
* {{ contribution }}
{% endfor %}

<p>
{% for link in member.links %}
<a href="{{ link.url }}" class="icon-{{ link.name }}"></a>
{% endfor %}
</p>
</div>
{% if track_index == "1" %}
</div>
{% endif %}

{% endfor %}




{% include _improve_content.html %}
