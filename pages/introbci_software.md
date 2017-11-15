---
layout: page-fullwidth
show_meta: false
title: "Introduction to BCI: Software Tools to Use"
subheadline: ""
teaser: "This tutorial serves as an introduction to software tools that you can use to analyze EEG and MEG data."
header: ""
image_fullwidth: ""
permalink: "/introbci_software/"
---
<div class="row">
<div class="medium-4 medium-push-8 columns" markdown="1">
<div class="panel radius" markdown="1">
**Table of Contents**
{: #toc }
*  TOC
{:toc}
</div>
</div><!-- /.medium-4.columns -->

<div class="medium-8 medium-pull-4 columns" markdown="1">

# Introduction to Brain Computer Interfaces: Software to Use

###__Psychopy__

[Psychopy](http://www.psychopy.org/about/index.html) is an open-source (GPLv2 license) Python application to build experiments.
It is often used in psychology or cognitive neuroscience labs as an alternative to the proprietary
E-Prime. Since it is written in Python, it's cross platform and scripts usually work on masOS
and Windows with no tweaking. It can allow timing based on frames, which it
[claims](http://www.psychopy.org/coder/codeStimuli.html#timing) is more accurate than
measuring with a clock.
It includes an interface to [write code](http://www.psychopy.org/coder/coder.html#coder)
for experiments:

__insert image with code interface__

And [visual interface](http://www.psychopy.org/builder/builder.html) to make experiments by
dragging blocks around:

__insert image with visual interface__

### __Pygame__

[Pygame](https://www.pygame.org/wiki/about) is an open (LGPL license) Python library to build games.
Due to its simple library, it is also used in some labs to build experiments. As it is
targeted to a wider audience, it has a pretty good set of [tutorials](https://www.pygame.org/wiki/GettingStarted)
and [docs](https://www.pygame.org/docs/). It has fewer dependencies and is generally
easier to install than psychopy, and can sometimes give you greater control over
what you display.
However, it's also not geared towards experiments, and you may have to build up some helper
functions to use pygame effectively.

__insert image of pygame interface__

### __OpenViBE__

[OpenViBE](http://openvibe.inria.fr/) is an open-source (AGPLv3) platform specifically
geared towards BCI experiments.
It has a visual interface consisting of "blocks" that can be used to build experiments.
These blocks can be extended using Python, Lua, C++, or Matlab.

__insert graph expaning OpenViBE__

As it's geared towards BCI development, it has [comprehensive support](http://openvibe.inria.fr/supported-hardware/)
for streaming EEG data from a lot of different devices, and [a lot of algorithms](http://openvibe.inria.fr/documentation/1.3.0/Doc_BoxAlgorithms.html)
specifically for BCIs.
It also has neat 3D interfaces for trying out BCI paradigms, like lifting a spaceship
using motor imagery:

__insert that picture of a... spaceship?__

The main downsides are that its interface can sometimes be intimidating and it does
not have a library, so you cannot use OpenViBE without launching the full interface.
Overall, OpenViBE is a great tool for getting started and experimenting ## various BCI paradigms.

### __OpenEXP__
[OpenEXP](https://github.com/openexp/OpenEXP) is an open-source (MIT license) desktop
app for running experiments and collecting behavioural and physiological data. IT is still in alpha stage,
so may not be ready for experiments yet, but shows great promise for the future, as
it is developed by [key NeurotechX members](https://github.com/openexp/OpenEXP/graphs/contributors).

__insert picture of OPENEXP__

It is based on [jsPsych](https://github.com/jspsych/jsPsych) and is written using
Javascript, so it could run in a web browser for scalable data collection.

### __Psychtoolbox__
[Psychtoolbox](http://psychtoolbox.org/) is an open-source (MIT license) set of functions
for running psychophysics experiments in Matlab or Octave. It has a lot of [tutorials](http://peterscarfe.com/ptbtutorials.html)
geared towards psychophysics experiments and a comprehensive [FAQ](https://github.com/Psychtoolbox-3/Psychtoolbox-3/wiki/FAQ).

It can performa pretyy much any visual, text, or audio you might need for
psychophysics, such as a set of [rotating 3D cubes:](http://peterscarfe.com/rotatingcubesdemo.html)

__insert image of rotating cubes__

The functions provided can sometimes be close to the graphics pipeline, so it may
have set textures or explicitly ask for anti-aliasing. However, this does provide more control.

</div> <!-- end of content section -->
</div> <!-- end of row -->
