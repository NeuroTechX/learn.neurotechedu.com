---
layout: page
show_meta: false
title: "Style your content!"
subheadline: "Layouts of Feeling Responsive"
header:
   image_fullwidth: "header_unsplash_5.jpg"
permalink: "/design/"
---
<ul>
    {% for post in site.categories.design %}
    <li><a href="{{ site.url }}{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
</ul>

# How to Design an Experimental Protocol

You have your EEG headset, software to use it, and a burning desire to analyze an EEG signal. Awesome! In this module we're going
to discuss best practices for designing an experiment. 

