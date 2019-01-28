---
layout: page-fullwidth
show_meta: false
title: Consumer EEG Headsets
subheadline: Compare and Contrast
teaser: >-
  Your choice of headset will depend on what you intend to use it for. The
  answer will depend on your budget, interest, project idea and the number of
  electrodes required. Before purchasing a headset, think about your programming
  experience and Project Idea.
header:
  image_fullwidth: neurons.jpg
permalink: /headsets/
published: true
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

# What to look for in a headset.

When deciding which EEG to purchase, there are a few features you should look at when making your decision.

## Number and Placement of Electrodes:

Depending on the type of brain response you want to measure, your system may need a minimum number of electrodes. Measuring Relaxation levels is easy with 1 or 2 electrodes but measuring other brain activity can be difficult.  In most eeg papers, they will state where on the brain the strong response came from.

Also, many consumer EEG's have electrodes which are rigid and can't be moved. If you want to measure [Motor Imagery](https://en.wikipedia.org/wiki/Motor_imagery) with the Muse, you won't have much success. You would be better off with an OpenBCI so that you can place the electrodes where you want.

**Reference and more information**

[IMOTIONS EEG 101 Guide](https://imotions.com/blog/eeg/)

## Sampling Rate:  

The Sampling Rate of an EEG is the number of sample a second you can get from your device. Most devices will have a minimum of 256 samples a second, but you can find some which have a higher sampling rate. Depending on the frequency you are interested in studying, your sampling rate needs to be at least 2.5 times greater.

**Reference and more information**

[This EEG tutorials has some more details on the sampling rate](http://www.ebme.co.uk/articles/clinical-engineering/56-introduction-to-eeg)

## ADC Bits:

Simply put, the Analog to Digital Converter (ADC) Bits is the resolution of the signal. The number of bits is important in being able to accurately estimate the voltage, but more bits doesn't necessarily mean better quality data. To give an idea of how it would work with eeg data, let's say your system has 4 ADC bits and you want to measure a signal between 0 and 10 Volts. This would mean that your computer would represent the data in the following way:

|Voltage||2- Bit Digital Representation|
|0-2.5   ||00|
|2.5-5.0 ||01|  
|5.0-7.5 ||10|
|7.5-10.0||11|

**Reference and more information**

[What does 12 or 16 bit resolution mean?](https://labjack.com/support/faq/what-does-12-or-16-bit-resolution-mean)
[ What are the advantages of a 24 bit system?](https://www.biosemi.com/faq/24bitsystem.htm)


# Devices

## Muse

<hr>

<div class="row">
<div class="large-6 columns" markdown="1">
Muse is an EEG device which has developed as a meditation device. It has 4 channels, 1 reference and two ground electrodes. The Muse headband comes with electrodes placed on Af7 and Af8 location if you are following 10-20 International Standards. It is one of the easier bands to get started with if you are interested in learning EEG as it requires no head prep.
</div>

<div class="large-6 columns" markdown="1">
![Muse Headset](../images/muse-white.png)
</div>
</div> <!-- end of row -->

#### Features:

* 4 electrodes
* Static Electrode Placement (Af7 and Af8)
* Dry Electrodes
* 256 Hz Sampling Rate
* 12 bits
* Research Tools for Windows, Mac and Linux
* SDK for Android, IOS, Windows

#### Known Recordable EEG Paradigms:
* "Relaxation" Level
* "Concentration" levels
* Frontal Asymmetry  
* P300

**US Price (as of January 2017):**  $200


## OpenBCI

<hr>

<div class="row">
<div class="large-6 columns" markdown="1">

The OpenBCI is an open source EEG and can go to a maximum of 16 channels. It was originally a 2013 Kickstarter project, but has expanded the original concept to include an open source 3D printed cap. There is also a 4 channel system which can be purchased if you need something cheaper.

</div>
<div class="large-6 columns" markdown="1">
![OpenBCI headset](../images/openBCI.png)
</div>
</div> <!-- end of row -->


#### Features:

* up to 16 channels
* Flexible Electrode Placement
* Compatible with both Dry and Wet electrodes
* 256 Hz Sampling Rate
* 24 bits
* Open Source Software and Hardware

#### Known Recordable EEG Paradigms:

Any paradigm which needs only 16 channels or less


**US Price (as of January 2017):**  
4 channels: $200
8 channels: $500
16 channels: $945




## Emotiv Epoc

<hr>

<div class="row">
<div class="large-6 columns" markdown="1">
The Emotiv Epoc is one of the first consumer EEG devices released on the market. The popularity of the company surged in 2012 and 2013, which can be reflected by its sales and number of DIY projects.

The Epoc is more stylish and easier to wear. It has 14 channel EEG which has a static form factor. This board is a good option for easy development and it only requires software experience. It is a popular device to use for EEG research as the cost is much better versus other research grade mobile EEG providers. It is however less economic than other commercial headsets and has an additional cost for accessing the data that the headset collects. 

</div>

<div class="large-6 columns" markdown="1">
![Emotiv headset](../images/emotiv_epoc_600.png)
</div>
</div> <!-- end of row -->

#### Features

* 14 channels
* Rigid Electrode Placement (AF3, F7, F3, FC5, T7, P7, O1, O2, P8, T8, FC6, F4, F8, AF4)
* Wet Electrodes (require saline water)
* 2048 Hz Sampling Rate
* 14 bits

#### Known Recordable EEG Paradigms:

Many paradigms which need only 14 channels or less

**US Price (as of January 2017):**   $800





## Emotiv Insight

<hr>

<div class="row">
<div class="large-6 columns" markdown="1">
The Emotiv Insight was the second product which Emotiv brought the market, and was marketed as a more economic option to their first product. 
</div>

<div class="large-6 columns" markdown="1">
![Emotiv Insight](../images/emotiv-insight.png)
</div>
</div> <!-- end of row -->


#### Features

* 5 channels
* Rigid Electrode Placement (AF3, AF4, T7, T8, Pz)
* Dry Electrodes
* Min 126 and Max 256 Hz Sampling Rate
* 15 bits

#### Known Recordable EEG Paradigms:

Many paradigms which need only 5 channels or less

**US Price (as of January 2017):**   $300


## Neurosky Mindwave

<hr>

<div class="row">
<div class="large-6 columns" markdown="1">
The Neurosky is one of the original consumer EEGs on the market. The design is simple and only has 1 channel meant for use. Some people say they have built more complicated products with them.
</div>

<div class="large-6 columns" markdown="1">
![Neurosky Mindwave](../images/NeuroskyMindwave.png)
</div>
</div> <!-- end of row -->



#### Features

* 1 channel
* Rigid Electrode Placement (AFz)
* Dry Electrodes
* 512 Hz Sampling Rate
* 12 bits
* Available SDK

#### Known Recordable EEG Paradigms:
* "Relaxation" Level
* "Concentration" levels

**US Price (as of January 2017):** : $100

</div> <!-- end of content column -->
</div> <!-- end of row -->

<div class="row" markdown="1">
## Features Comparison <!-- table has its own row so that it can occupy whole width of page -->
<hr>

| Device |	Channels | ADC Bits |	Sample Rate | Motion sensors |	LSL Support |	SD Card Support |	TTL |	Battery Length |	Cost (US) as of Jan 2017 |
|--------|-----------|----------|--------------|----------------|--------------|-----------------|-----|----------------|---------------------------|
| Muse 2016 |	4-6               |	12     |	256 Hz | 3 axis |	Yes      |	No             |	Maybe |	5 hours|	$200 |
| Epoc      |	14+2 ref          |	16     |	256 Hz | 9 axis |	Possible |	With accessory |	N/A   |	6 hours using BTLE |	$799 |
| Insight   |	5+2 ref           |	15     |	2048 Hz  | 9 axis |	Possible |	With accessory |	N/A   |	4 hours using Bluetooth |	$300 |
| OpenBCI   |	up to 16 channels |	24     |	250 Hz | 3 axis |	Yes      |	Yes            |	Yes   |	~26 hours |	$500 for 8 channels, $949 for 16 |
| Neurosky Mindwave |	1+1 ref   |	12     |	512Hz  | N/A    |	N/A      |	N/A            |	N/A   |	8 hours |	$99.99 |

</div> <!-- end of table section -->
