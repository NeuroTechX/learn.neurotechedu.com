---
#
# Use the widgets beneath and the content will be
# inserted automagically in the webpage. To make
# this work, you have to use › layout: frontpage
#
layout: frontpage
header:
  image_fullwidth: gallery-example-1.jpg
widget1:
  title: "Getting Started"
  url: '/getting-started/'
  image: openBCI-303x182.jpg
  text: 'An easy project for one person might be difficult for someone else. Therefore we have broken down the projects as to either requiring no programming experience (plug and play) or requiring some experience. You will notice that with certain EEG headsets that there is more tutorials than others. <br>
  The best way to get started will also depend on the headset that you have available.'
widget2:
  title: "Headsets"
  url: '/headsets/'
  image: openbci-3d-303x182.jpg
  text: 'Your choice of headset will depend on what you intend to use it for. The answer will depend on your budget, interest, project idea and the number of electrodes required. Before purchasing a headset, think about your programming experience and Project Idea.'
#  video: '<a href="#" data-reveal-id="videoModal"><img src="http://phlow.github.io/feeling-responsive/images/start-video-feeling-responsive-302x182.jpg" width="302" height="182" alt=""/></a>'
widget3:
  title: "Neurotech Applications"
  url: '/applications/'
  image: applications-thumbnail2.jpg
  text: 'Anything that records from or directly interfaces with the human brain. For the time being, we are excluding technologies that rely on downstream signals like EMG (muscles) and EKG (heartrate).
What are the fields that are involved/interested in non-pharmaceutical Neurotech? Click to learn more.'
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
