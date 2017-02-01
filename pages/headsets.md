---
layout: page-fullwidth
show_meta: false
title: "Headsets"
subheadline: "Compare and Contrast"
teaser: "Your choice of headset will depend on what you intend to use it for. The answer will depend on your budget, interest, project idea and the number of electrodes required. Before purchasing a headset, think about your programming experience and Project Idea."
header:
   image_fullwidth: "header_homepage_13.jpg"
permalink: "/headsets/"
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

## Muse
<hr>

<div class="row">
<div class="large-6 columns" markdown="1">
Muse is an EEG device which has developed as a meditation device. It has 4 channels, 1 reference and two ground electrodes.
</div>

<div class="large-6 columns" markdown="1">
![Muse Headset](../images/muse-white.png)
</div>
</div> <!-- end of row -->

#### Pros

* Easy to use SDK.
* Easy to wear
* Works well for doing resting state experiments
* Relatively cheap and has a 1 year warranty


#### Cons

* Limited to 4 channels
* Electrodes are not movable
* Not all head sizes will fit
* Difficult to do ERP experiments

## OpenBCI
<hr>

<div class="row">
<div class="large-6 columns" markdown="1">

The OpenBCI is an open source eeg and can go to a maximum of 16 channels. It was originally a 2013 Kickstarter project, but has expanded the original concept to include an opensouce 3D printed cap and will launch a 4 channel board in 2017.

</div>
<div class="large-6 columns" markdown="1">
![OpenBCI headset](../images/openBCI.png)
</div>
</div> <!-- end of row -->

#### Pros

* Can go up to 16 channels
* 256 Hz Sampling Rate
* Modifiable to your own needs
* Can use your own electrodes
* Can add other inputs into the board
* Open Source (Hardware schematics and Software)
* Well Priced

#### Cons
* Higher Learning Curve
* Must print or get your own headset
* Must get your own electrodes


## Emotiv Epoc
<hr>

<div class="row">
<div class="large-6 columns" markdown="1">
T The Emotiv Epoc is one of the first consumeer eeg devices which was released on the market. The popularity of the company surged in 2012 and 2013, which can be reflected by its sales and number of DIY projects.

The Epoc is more stylish and easier to wear. It is also a popular device to use for EEG research as the cost is much better versus other research grade mobile EEG providers. However multiple people have complained that the provided electrodes are not very good.
</div>

<div class="large-6 columns" markdown="1">
![Emotiv headset](../images/emotiv_epoc_600.png)
</div>
</div> <!-- end of row -->

#### Pros

* Easy to put on.
* Good option for mobile eeg research
* Multiple apps to go along with the headset if you are into controlling things with your mind.

#### Cons

* The free SDK does not give you the raw data
* More Pricey
* The SDK is a little bit more clunky versus the alternatives and requires some technical experience
* Some people have complained about the electrodes not being high quality or not getting good contact

## Emotiv Insight
<hr>

<div class="row">
<div class="large-6 columns" markdown="1">
The Emoti Insight was the Section version of product with Emotiv brought the market. They positioned this product to be cheaper and a better option for people who don't want to spend too much money.
</div>

<div class="large-6 columns" markdown="1">
![Emotiv Insight](../images/emotiv-insight.png)
</div>
</div> <!-- end of row -->


#### Pros

* Cost is lower
* Design is sleek
* Easy to wear and use
* Uses Dry Electrodes

#### Cons

* The free SDK does not give you the raw data
* The SDK is a little bit more clunky versus the alternatives and requires some technical experience

## Neurosky Mindwave
<hr>

<div class="row">
<div class="large-6 columns" markdown="1">
The Neurosky is one of the original consumer eeg's to go to the market. It's product is design primarily to be toy like in nature and only has 1 channel.
</div>

<div class="large-6 columns" markdown="1">
![Neurosky Mindwave](../images/NeuroskyMindwave.png)
</div>
</div> <!-- end of row -->


#### Pros

* Low cost
* Easy to wear and use
* Available SDK
* Uses Dry Electrodes

#### Cons

* Only 1 channel
* Can't move the electrode
* The SDK is a little bit more clunky versus the alternatives and requires some technical experience


</div> <!-- end of content column -->
</div> <!-- end of row -->

<div class="row" markdown="1">
## Features Comparison <!-- table has its own row so that it can occupy whole width of page -->
<hr>

<table>
  <caption></caption>
  <colgroup>
  <!-- here you can set column width using       <col span="1" style="width: 10%;">   
      see template typography page for details  https://phlow.github.io/feeling-responsive/design/typography/typography/ -->
  </colgroup>
  <thead>
    <tr>
      <th>Device</th>
      <th>Channels</th>
      <th>ADC Bits</th>
      <th>Sample Rate</th>
      <th>Motion sensors</th>
      <th>LSL Support</th>
      <th>SD Card Support</th>
      <th>TTL</th>
      <th>Battery Length</th>
      <th>Cost (US) as of Jan 2017</th>
    </tr>
  </thead>
  <tbody>
  <tr> <!-- row 2 -->
    <td>Muse 2016</td><!--  Device Name -->
    <td>4-6</td><!--  # of Channels -->
    <td>12</td> <!--  ADC Bits -->
    <td>256</td><!--  Sampling Rate -->
    <td>3 axis</td> <!--  Motion Sensor -->
    <td>Yes</td> <!--  LSL Support -->
    <td>No</td> <!-- SD Card Support -->
    <td>Maybe</td> <!-- TTL -->
    <td>5 hours</td> <!-- Battery Length -->
    <td>200</td><!-- Cost -->
  </tr>
  <tr> <!-- row 3 -->
    <td>Epoc</td><!--  Device Name -->
    <td>14 + 2 ref</td><!--  # of Channels -->
    <td>16 bit</td> <!--  ADC Bits -->
    <td>256 HZ</td> <!--  Sampling Rate -->
    <td>9 axis</td> <!--  Motion Sensor -->
    <td>Possible</td> <!--  LSL Support -->
    <td>With accessory</td> <!-- SD Card Support -->
    <td>N/A</td> <!-- TTL -->
    <td>6 hours using BTLE</td> <!-- Battery Length -->
    <td>799$</td><!-- Cost -->
  </tr>

  <tr> <!-- row 4 -->
  <td>Insight</td> <!-- Device Name -->
  <td>5+2 ref</td> <!-- # of Channels  -->
  <td>15 bit</td> <!--  ADC Bits -->
  <td>28 HZ</td> <!--  Sampling Rate -->
  <td>9 axis</td> <!--  Motion Sensor -->
  <td>Possible</td> <!--  LSL Support -->
  <td>With accessory</td> <!-- SD Card Support -->
  <td>N/A</td> <!-- TTL -->
  <td>4 hours using Blutooth</td> <!-- Battery Length -->
  <td>300</td> <!-- Cost -->
  </tr>

  <tr> <!-- row 5 -->
  <td>OpenBCI</td><!-- Device Name -->
  <td>up to 16 channels</td> <!-- # of Channels  -->
  <td>24</td>  <!--  ADC Bits -->
  <td>250 HZ</td> <!--  Sampling Rate -->
  <td>3 axis</td> <!--  Motion Sensor -->
  <td>Yes</td> <!--  LSL Support -->
  <td>Yes</td> <!-- SD Card Support -->
  <td>Yes</td> <!-- TTL -->
  <td>~26 hours</td> <!-- Battery Length -->
  <td>500 for 8 channels 949 for 16 </td> <!-- Cost -->
  </tr>

  <tr> <!-- row 6 -->
  <td>Neurosky Mindwave</td> <!-- Device Name -->
  <td>1 +1 ref</td> <!-- # of Channels  -->
  <td>12</td> <!-- ADC Bits  -->
  <td>512Hz</td><!-- Sampling Rate -->
  <td>this</td><!-- Motion Sensor -->
  <td>is</td><!-- LSL Support -->
  <td>spartaaaa</td> <!-- SD Card Support-->
  <td>derp</td> <!-- TTL -->
  <td>8 hours</td><!-- Battery Length -->
  <td>99.99 </td><!-- Cost -->
  </tr>
  </tbody>
</table>
</div> <!-- end of row -->

 [1]: {{ site.url }}{{ site.baseurl }}/documentation/
