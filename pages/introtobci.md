---
layout: page-fullwidth
show_meta: false
title: "Intro to BCI"
subheadline: "Intro to BCI"
teaser: "Intro to BCI"
header:
   image_fullwidth: ""
permalink: "/introtobci/"
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

# Intro to BCI

## What is the definition

## What are  the types of BCI's
There are many different techniques to measure brain signals. 

We can divide them into Invasive, Semi-invasive and Non-Invasive. 

| Option | Description | Pic | 
| ------ | ----------- | ---- |
| Non-invasive   | The sensors are placed on the scalp to measure the electrical potentials produced by the brain (EEG) or the magnetic field (MEG). | ![Emotiv headset](../images/introtobci/emotiv_epoc_large.jpg) |
| Semi-invasive | The electrodes are placed on the exposed surface of the brain(ECoG).| ![EcoG](../images/introtobci/ecog.png) |
| Invasive    | The micro-electrodes are placed directly into the cortex, measuring the activity of a single neuron. | ![Utah Array](../images/introtobci/Utah_array.jpg) |

The following image shows the different layers of the brain and where the signal is taken from.
 
**Non-invasive**: the EEG signal is taken placing electrodes on the scalp, so on the most external part.

**Semi-invasive**: the ECoG signal is taken from electrodes placed in the dura or in the arachnoid.

**Invasive**: the Intraparenchymal signal is taken directly implanting electrodes in the cortex.


### Invasive

Invasive types of BCI are implanted directly into the brain during a neurosurgery.
There are single unit BCIs, which detect the signal from a single area of brain cells, and multi units BCIs which detects from multiple areas. Electrodes have different lengths, for example, up to 1.5 mm (Utah, Blackrock Microsystems) or 10 mm (FMA, MicroProbes) in a MEA. The quality of the signal is the highest, but the procedure has several problematics , as the risk of forming scar tissues. The body reacts to the foreign object and build the the scar around the electrodes, which cause deterioration in the signal. Because neurosurgery can be a risky and expensive process, the target of invasive BCI are mainly blind and paralyzed patients.

### Non Invasive

## Components
### Brain activity
### Signal acquisition
### Preprocessing
### Feature Extraction
### Classification
### Translation
### Feedback device

## Applications

## Examples

## Limitations

## Ethics

## Safety

## Future of the field


# h1 Heading :)
<hr>
<div class="row">
<div class="large-6 columns" markdown="1">

## h2 Heading
### h3 Heading
#### h4 Heading
##### h5 Heading
###### h6 Heading


## Horizontal Rules

___

---

***
</div>
<div class="large-6 columns" markdown="1">
</div>
</div> <!-- end of row -->


## Emphasis

**This is bold text**

__This is bold text__

*This is italic text*

_This is italic text_

~~Strikethrough~~


## Blockquotes


> Blockquotes can also be nested...
>> ...by using additional greater-than signs right next to each other...
> > > ...or with spaces between arrows.


<hr>

<div class="row">
<div class="large-6 columns" markdown="1">

## Tables

| Option | Description |
| ------ | ----------- | 
| data   | path to data files to supply the data that will be passed into templates. |
| engine | engine to be used for processing templates. Handlebars is the default.  |
| ext    | extension to be used for dest files. |

Right aligned columns

| Option | Description |
| ------:| -----------:|
| data   | path to data files to supply the data that will be passed into templates. |
| engine | engine to be used for processing templates. Handlebars is the default. |
| ext    | extension to be used for dest files. |


## Links

[link text](http://dev.nodeca.com)

[link with title](http://nodeca.github.io/pica/demo/ "title text!")

Autoconverted link https://github.com/nodeca/pica (enable linkify to see)


## Images

![Minion](https://octodex.github.com/images/minion.png)
![Stormtroopocat](https://octodex.github.com/images/stormtroopocat.jpg "The Stormtroopocat")

Like links, Images also have a footnote style syntax

![Alt text][id]

With a reference later in the document defining the URL location:

[id]: https://octodex.github.com/images/dojocat.jpg  "The Dojocat"

</div>
<div class="large-6 columns" markdown="1">

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
The Emotiv Epoc is one of the first consumer EEG devices which was released on the market. The popularity of the company surged in 2012 and 2013, which can be reflected by its sales and number of DIY projects.

The Epoc is more stylish and easier to wear. It has 14 channel EEG which has a static form factor. This board is a good option for easy development and it only requires software experience. It is also a popular device to use for EEG research as the cost is much better versus other research grade mobile EEG providers. The major downside of the Epoc is the cost and the fact that they charge you to get access to raw data. Multiple people have complained that the provided electrodes are not very good.
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
The Neurosky is one of the original consumer EEGs on the market. The design is toy-like and only has 1 channel meant for simple use cases. Some people say they have built more complicated products with them.
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

| Device |	Channels | ADC Bits |	Sample Rate | Motion sensors |	LSL Support |	SD Card Support |	TTL |	Battery Length |	Cost (US) as of Jan 2017 |
|--------|-----------|----------|--------------|----------------|--------------|-----------------|-----|----------------|---------------------------|
| Muse 2016 |	4-6               |	12     |	256 Hz | 3 axis |	Yes      |	No             |	Maybe |	5 hours|	$200 |
| Epoc      |	14+2 ref          |	16 bit |	256 Hz | 9 axis |	Possible |	With accessory |	N/A   |	6 hours using BTLE |	$799 |
| Insight   |	5+2 ref           |	15 bit |	28 Hz  | 9 axis |	Possible |	With accessory |	N/A   |	4 hours using Bluetooth |	$300 |
| OpenBCI   |	up to 16 channels |	24     |	250 Hz | 3 axis |	Yes      |	Yes            |	Yes   |	~26 hours |	$500 for 8 channels, $949 for 16 |
| Neurosky Mindwave |	1+1 ref   |	12     |	512Hz  | N/A    |	N/A      |	N/A            |	N/A   |	8 hours |	$99.99 |

</div> <!-- end of table section -->
