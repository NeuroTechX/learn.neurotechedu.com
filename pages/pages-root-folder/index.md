---
#
# Use the widgets beneath and the content will be
# inserted automagically in the webpage. To make
# this work, you have to use › layout: frontpage
#
layout: frontpage
header:
  image_fullwidth: "earth.jpg"
widget1:
  title: "Tutorials"
  url: 'http://learn.neurotechedu.com/tutorials/'
  image: openBCI-303x182.jpg
  text: 'This page features learning materials grouped by category and give you an insight into learning tracks.'
widget2:
  title: "Resources"
  url: 'https://github.com/NeuroTechX/awesome-bci'
  image: openbci-3d-303x182.jpg
  text: 'Your choice of headset will depend on what you intend to use it for. The answer will depend on your budget, interest, project idea and the number of electrodes required. Before purchasing a headset, think about your programming experience and Project Idea.'
#  video: '<a href="#" data-reveal-id="videoModal"><img src="http://phlow.github.io/feeling-responsive/images/start-video-feeling-responsive-302x182.jpg" width="302" height="182" alt=""/></a>'
widget3:
  title: "How to Contribute"
  url: 'https://github.com/NeuroTechX/learn.neurotechedu.com'
  image: applications-thumbnail.jpg
  text: 'Click to contribute to our Github page directly. You may also choose to join the NeurotechX committee or our Slack group.'
#
# Use the call for action to show a button on the frontpage
#
# To make internal links, just use a permalink like this
# url: /getting-started/
#
# To style the button in different colors, use no value
# to use the main color or success, alert or secondary.
# To change colors see sass/_01_settings_colors.scss
#

callforaction:
  url: https://tinyletter.com/feeling-responsive
  text: Inform me about new updates and features ›
  style: alert
permalink: /index.html
#
# This is a nasty hack to make the navigation highlight
# this page as active in the topbar navigation
#
homepage: true
---

<div id="videoModal" class="reveal-modal large" data-reveal="">
  <div class="flex-video widescreen vimeo" style="display: block;">
    <iframe width="1280" height="720" src="https://www.youtube.com/embed/3b5zCFSmVvU" frameborder="0" allowfullscreen></iframe>
  </div>
  <a class="close-reveal-modal">&#215;</a>
</div>
