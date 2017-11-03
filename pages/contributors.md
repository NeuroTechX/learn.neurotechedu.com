s---
layout: page-fullwidth
title: "Contributors"
teaser: "These are the people who made NeuroTechEDU what it is today."
header:
    image_fullwidth: "header_drop.jpg"
permalink: "/contributors/"

---

{% for member in site.data.contributors %}
<div class="row">
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
</p>
{% endfor %}
</div>
</div>
{% endfor %}






{% include _improve_content.html %}
