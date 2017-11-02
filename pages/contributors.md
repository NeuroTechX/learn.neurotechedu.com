---
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

<div class="row">
<div class="medium-6 columns contributor" markdown="1">
### Francesca Placido

#### Roles

* Content Builder

#### Contributed to

* Intro to BCI

<p>
<a href="http://twitter.com/francescacoo_j" class="icon-twitter"></a>
<a href="http://github.com/francescacoo" class="icon-github"></a>
</p>
</div>

<div class="medium-6 columns contributor" markdown="1">
### Davide Valeriani

#### Roles

* Mentor

#### Contributed to

* ERP feature extraction
<p>
<a href="http://www.davidevaleriani.it/" class="icon-globe"></a>
</p>
</div>
</div>




<div class="row">
<div class="medium-6 columns contributor" markdown="1">
### Ryan Lintott

#### Roles

* Editor
* Content Builder

#### Contributed to

* Feature Extraction ERP
<p>
<a href="http://ryanlintott.com/" class="icon-globe"></a>
<a href="http://linkedin.com/in/ryanlintott/" class="icon-linkedin"></a>
<a href="http://twitter.com/ryanlintott" class="icon-twitter"></a>
<a href="http://github.com/ryanlintott" class="icon-github"></a>
</p>
</div>



<div class="medium-6 columns contributor" markdown="1">
### Hector Orozco

#### Roles

* Editor
* Mentor

#### Contributed to

* Preprocessing 
* Intro to neuroscience

<p>
<a href="https://www.linkedin.com/in/hector-domingo-orozco-perez-2017a4105/" class="icon-linkedin"></a>
<a href="http://twitter.com/neurohazardous" class="icon-twitter"></a>
<a href="http://github.com/neurohazardous" class="icon-github"></a>
</p>
</div>
</div>


<div class="row">
<div class="medium-6 columns contributor" markdown="1">
### Yu Min Chuang

#### Roles

* Content Builder

#### Contributed to

* Feature Extraction ERP

<p>
<a href="https://www.linkedin.com/in/yu-min-chuang-30a41b48/" class="icon-linkedin"></a>
</p>
</div>


<div class="row">
<div class="medium-6 columns contributor" markdown="1">
### Patrick Coleman

#### Roles

* Content Builder

#### Contributed to

* Preprocessing

<p>
<a href="https://padsterprogramming.blogspot.com/" class="icon-globe"></a>
<a href="https://www.linkedin.com/in/padsterpat/" class="icon-linkedin"></a>
<a href="https://github.com/padster" class="icon-github"></a>
</p>
</div>
</div>

<div class="row">
<div class="medium-6 columns contributor" markdown="1">
### Sheida Rabipour

#### Roles

* Editor
* Mentor

#### Contributed to

* Intro to BCI
* Signal Preprocessing 
<p>
<a href="https://www.linkedin.com/in/sheidarabipour/" class="icon-linkedin"></a>
<a href="https://www.researchgate.net/profile/Sheida_Rabipour" class="icon-globe"></a>
<a href="https://github.com/thesheid" class="icon-github"></a>
</p>
</div>
</div>


{% include _improve_content.html %}
