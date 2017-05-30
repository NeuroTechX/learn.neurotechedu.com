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

### Semi-Invasive
#### ECoG
Electrocorticography uses electrodes placed on the exposed surface of the brain to measure electrical activity from the cerebral cortex. It has been used for the first time in the 1950s at the Montreal Neurological Institute.
It is called semi-invasive but it still requires a craniotomy to implant the electrodes. For this reason it is used only when surgery is necessary for medical reasons (epilepsy for example). 
 
The electrodes may be placed outside the dura mater (epidural) or under the dura mater (subdural).
The strip or grid electrodes covers a large area of the cortex (from 4 to 256 electrodes), allowing a diverse range of cognitive studies. 

![EcoG](../images/introtobci/ecog1.jpg)

*In the image: MRI reconstruction of the patient’s brain with electrodes overlaid (red: grid array; blue: strip arrays) to allow precise matching of neurophysiological activity to neuroanatomical structures (Image from: Yang et al., Neuroimage, 2012)*

![EcoG](../images/introtobci/ecog.png)

The positive characteristics of ECoG are:
 
*         high spatial resolution and signal fidelity
*         resistance to noise
*         lower clinical risk and Robustness over long recording period[1] 
*         higher amplitude
 
 
**Spatial resolution**

A benefit of the ECoG over EEG, is that the spatial resolution is much higher because the signal doesn’t have to travel to reach the scalp. The spatial resolution in ECoG is tenths of millimeters, while it is centimeters in EEG (Leuthardt et al., 2004). 
 
---------------------------------------------------------------------------------------------------------------------
What do we mean by spatial resolution?
We can take, as an analogy, the clarity of an image.
A picture with a higher spatial resolution is “clearer”; in other words, it looks more precise because it is composed of more pixels per inch, showing more details. A picture with lower spatial resolution appears less clear, or more blurry because it is composed of fewer pixels per inch. 
Better spatial resolution allows us to understand with better precision where the signal is coming from. In the case of EEG, when the electrical signal travels through the skull, it is attenuated due to the low conductivity of the bones.
---------------------------------------------------------------------------------------------------------------------

**resistance to noise**

ECoG signal is not impacted by noise and artifacts as for example EMG (electromyographic - caused by muscles movements) and EOG (electrooculographic - caused by eyes movements)
 
**lower clinical risk**

The electrode arrays doesn’t need to penetrate into the cortex, which makes it safer than invasive recording (Leuthardt et al., 2004) 
 
**higher amplitude**

ECoG recordings are 50–100 µV maximum versus 10–20 µV
 
**In BCI**

There have been different studies about the use of ECoG in BCI, but they are all limited to cases where surgery was needed to remove an epileptic focus.
 
In one study (Schalk et al., 2008) for example, the researcher used ECoG to control a computer cursor in two dimensions.
Five patients, in preparation of surgery for epilepsy, had a subdural array of electrodes implanted for 7-14 days.  After a short training of less than 30 minutes, the patients have been able to control a cursor in two dimensions, with an average success rate of 53-73%. 
 


### Non Invasive

In the following section we will review briefly the main non-invasive techniques.
There are several non-invasive techniques used to study the brain, where EEG is the most common used because of the cost and hardware portability.

*     MEG magnetoencephalography
*     PET positron emission tomography
*     fMRI functional magnetic resonance imaging
*     fNIRS near-infrared spectroscopy
*     EEG Electroencephalography

In the following image is possible to see the different brain imaging techniques, compared by spatial and temporal resolution:

![brainImagineTecniques](../images/introtobci/brainimaging.png)

### MEG magnetoencephalography

** What is it? **

From Wikipedia “is a functional neuroimaging technique for mapping brain activity by recording magnetic fields produced by electrical currents occurring naturally in the brain, using very sensitive magnetometers.“

![MEG](../images/introtobci/MEG.png)

** How does it work? **
MEG measures the magnetic field caused by the currents in the brain, and it offers a better spatial resolution compared to EEG . Why? Because magnetic fields suffer far less than electric fields from the spatial blurring effect of the skull and intracerebral fluid.
“MEG is maximally sensitive to tangential sources and has low sensitivity to radial sources”
“MEG is better than EEG at detecting high-frequency activity (e.g., above 60 Hz). This is
because magnetic fields pass through the skull and scalp, whereas the electrical fields are
volume conducted through these tissues, which decreases signal-to-noise ratio at higher
frequencies.”



### PET positron emission tomography

** What is? **
PET is a nuclear imaging technique used in medicine to observe different processes, such as blood flow, metabolism, neurotransmitters, happening  in the body.

![PET](../images/introtobci/PET.png)
*“This image shows a picture taken from a typical PET facility equipped with an ECAT Exact HR+ PET scanner. PET scanners such as this are steadily being replaced by systems that combine both PET and CT scanners into a single PET/CT imaging device.”*

** How does it work? **
 
A small amount of radioactive material, called radiotracer, is injected in the bloodstream to reach the brain. In the case of the brain, the radiotracer get attached to the glucose and creates a radionuclide called fluorodeoxyglucose (FDG). The brain uses glucose and it will show different levels based on the level activity of the different regions.
The images of the PET scan are multicolored, where areas with more activities are in warmer colors as yellow and red. PET scans of the brain are used often to detect illnesses as cancer or others.

![PET](../images/introtobci/PET2.png)
*PET scan of a normal human brain*

### fMRI functional magnetic resonance imaging

**What is?**
Functional magnetic resonance imaging or functional MRI (fMRI) is a functional neuroimaging procedure using MRI technology that measures brain activity by detecting changes associated with blood flow.[1][2] This technique relies on the fact that cerebral blood flow and neuronal activation are coupled. When an area of the brain is in use, blood flow to that region also increases.[3]
 
fMRI had been developed in the 1990s. It is a non-invasive and safe technique, it doesn’t use radiation, it’s easy to use and it has excellent spatial and good temporal resolution.

![FMRI](../images/introtobci/fmri.png)

**How does it work?**
 
In the brain, haemoglobin in capillary red blood cells delivers oxygen to the neurons. Activity causes more demand for oxygen, which leads to an increase of blood flow.
The magnetic characteristics of haemoglobin change if it is or not oxygenated. This difference allows the MRI machine, which is a cylindrical tube with a powerful electro-magnet, to detect which areas of the brain are active in a specific moment.

![FMRI](../images/introtobci/fmri2.png)
*fMRI images from a study showing parts of the brain lighting up on seeing houses and other parts on seeing faces. The 'r' values are correlations, with higher positive or negative values indicating a better match.*

### fNIRS near-infrared spectroscopy

**What is?**
Functional Near-Infrared Spectroscopy (fNIR or fNIRS), is the use of NIRS (near-infrared spectroscopy) for the purpose of functional neuroimaging. Using fNIR, brain activity is measured through hemodynamic responses associated with neuron behaviour. 

An optical technique to measure localized cortical brain activity 
 
**How does it work?**
fNIRS measures the changes in blood flow as fMRI, but using a different technique, infrared light vs magnetic field.
![FNIRS](../images/introtobci/fnirs.png)
*In the image: fNIRS during table-tennis experiment*

When a task begins there is consumption of oxygen, as the complexity increases, also the request for oxygen increases. fMRI measures how much oxygen is consumed. fNIRS measures also how much oxygen is available in the area (overshot). 
 
Still, the temporal quality of fNIRS is not as good as EEG. fNIRS takes 10 samples per second, which is trumped by EEG’s 500 to 1000 samples per second. And the spatial resolution is not as good as fMRI. For example, fMRI can image subcortical brain regions, while fNIRS cannot analyze past the cortex, unable to capture any subcortical activation. Indeed, many researchers who presented their fNIRS at SfN are using the instrument as a supplement to their EEG or fMRI data.
 
Benefits:
* Non-invasive
* Portable
* Accessible
* Less sensible to artifacts compared to fMRI and EEG
 
Has a temporal resolution more similar to EEG
fMRI may record one sample per 2 seconds, fNIRS can record 10 samples per 1 second
 
fNIRS better spatial resolution than EEG and better temporal resolution than fMRI

### EEG

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
