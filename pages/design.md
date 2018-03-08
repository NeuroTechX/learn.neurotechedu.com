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

## Design an Experiment
### What is your hypothesis?
### How are you going to test your hypothesis?

### Quirks of an EEG headset

The human brain is an incredibly complex organ, with potentially hundreds of thousands of neurons firing in response to different 
thoughts and stimuli. When measuring EEG it is important to use contrasting mental states to filter out noise. For example, if you were trying to capture an EEG response to visual stimuli, you may want to include a sampling run where the participant has their eyes closed. This provides you a baseline of EEG data that you know is not connected to the stimulus you are looking to analyze.

Here's another example: in an experiment conducted by [REFERENCE], the 


### Setting up EEG electrodes

### How do you interpret your data

insert images of unfiltered EEG data

insert images of filtered EEG data through each step of data analysis

### How to draw conclusions from your data
