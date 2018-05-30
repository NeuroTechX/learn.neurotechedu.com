---
layout: page-fullwidth
show_meta: false
title: "New Emerging Technologies"
subheadline: ""
teaser: "This module covers some of the cutting-edge technologies being developed in neurotechnology! New methodologies for recording from the brain, recording to the brain, and closed-loop systems are covered, as well as consumer-facing devices and public perception."
header: ""
image_fullwidth: ""
permalink: "/template/"
---
<div class="row">
<div class="medium-4 medium-push-8 columns" markdown="1">
<div class="panel radius" markdown="1">


**Table of Contents**
{: #toc }
*  Introduction
*  Reading (Recording)
*  Writing (Modulating)
*  Read/Write (Closed Loop Systems)
*  Applications/Public Perception
*  References
{:toc}
</div>
</div><!-- /.medium-4.columns -->


<div class="medium-8 medium-pull-4 columns" markdown="1">


# New Emerging Technologies


## Introduction

![Recording techniques](https://www.the-scientist.com/Nov2014/Neuroprosthetics_Finalcmyk.jpg)

Neurotechnology is a broad term, encompassing any tool-based method of interacting with the brain. Driven by rapid technical development and neuroscientific research, it has exploded as a field in recent decades, inviting collaboration between biology, physics, computer science, materials science, and many engineering disciplines.

At its core, neurotechnology is working toward two types of interactions: “reading” information *from* the brain and “writing” information *to* the brain. [(1)](#references) “Reading” can be done by noninvasive imaging methods such as MRI, or invasive methods like directly recording signals from neurons with implanted electrodes. “Writing” refers to activating neurons in specific ways, and can be done with a number of modalities, like electricity, sound, and light. Many exciting developing efforts aim to build “Read/Write” devices that “close the loop” between these two activities, allowing for more complex and capable self-regulating systems.

This module is meant to introduce some of the latest developments and improvements on these methods from a technical side, as well as addressing how they are being applied outside of the research lab.


## Reading

![Neural recording](https://www.researchgate.net/profile/Elliot_Ludvig/publication/269517554/figure/fig4/AS:295080465321988@1447364073922/Single-unit-recording-A-Schematic-showing-the-placement-of-the-tip-of-an-electrode.png)

Observing the brain is one of the oldest methods used to understand its function. By looking at neural patterns of activity and correlating them with organism behavior or capabilities, we have already been able to make great progress in our understanding.

While there are many tools already used to observe the brain [(2)](#references), new innovations in this area are focused on overcoming the current limitations of those devices, while also building out downstream applications for the data. (Some basic considerations include invasive vs. non-invasive usage and higher temporal vs. spatial imaging resolution.)

One challenge is getting high quality data from specific brain areas in a non-invasive and more accessible way. To solve this, groups like Openwater, led by Mary Lou Jepsen, are building “wearable MRI” devices. Using new developments in optics and flexible electronics, this class of imaging sets out to address the cost and portability issues of MRI while providing spatial information currently unattainable from EEG devices. [(3)](#references) These units could potentially be integrated into clothing for continuous monitoring and also target other internal organs besides the nervous system.

Even when invasive methods are used to get direct neural recordings, the data quality problems aren’t completely solved, as there are hardware difficulties to contend with! The stiff nature of metal recording electrodes triggers an inflammatory response and scar tissue production, which causes signal quality to degrade over time and shortening the time between surgeries to replace electrodes. It is also difficult to get signal out of the brain through the skull without leaving a permanently open surgical site. To address these, many groups are building new electrodes to be flexible and highly biocompatible to integrate with brain tissue, smaller to minimize scarring, and wireless to transmit data to external devices. [(4, 5, 6)](#references)

“Neural dust” is a project from the Carmena lab at UCSC building a network of low-power, distributed recording devices that could be chronically implanted into the brain and work together to wirelessly transmit neural data from a relatively broad area. [(7)](#references) The small footprint of each device would allow it to move with its surrounding tissue instead of remaining stationary, and each unit would be powered by and communicated with via ultrasound, allowing them to operate without external power cables.

![Injectable mesh electronics](https://i0.wp.com/news.harvard.edu/wp-content/uploads/2015/06/lieber_pressfigure2_605.jpg?zoom=2&resize=808%2C539&ssl=1)

Another method to create chronic implants takes the route of highly flexible electronics, using injectable electrode arrays that unfold into a mesh on the surface of the brain. [(8, 9)](#references) This approach would allow neural implants with only very minimally invasive surgery. These arrays too would be able to move with the brain while reducing tissue damage and inflammation.


#### BCI
* Varsh’s BrainGate material
* Varsh’s VR material?

## Writing
“Writing” to the brain, i.e. stimulating neurons in purposeful ways, opens up new possibilities for interaction. It can be used to help understand brain function by looking for changes resulting from the stimulation, but it is also increasingly used therapeutically to treat chronic pain, movement disorders, and some psychiatric disorders.

Innovations in this arena have been focused mainly on specificity of simulation and discovery of new stimulation modalities.

![Noninvasive deep brain stimulation](http://blogs.discovermagazine.com/neuroskeptic/files/2017/06/grossman_cell.png)

Unlike observational neural recordings, neural stimulation has classically been limited to invasive methods only, generally by applying direct electrical stimulation to a neuron. New modalities have recently been investigated, with an incentive to reduce the number of risky brain surgeries required to implant current stimulator devices. One such option is to deliver electrical stimulation to deep brain areas noninvasively, recently demonstrated by the Boyden lab at MIT. By stimulating with two high-frequency electrical currents, they were able to produce a targeted “beat frequency” at the points where the currents interfered with each other. [(10)](#references) This method was able to successfully reach areas deep in the brain, previously only accessible by highly invasive deep brain stimulation (DBS) probes.


## Read/Write

Taking any of “Reading” and “Writing” methods alone represents an “open-loop” system. This means that in each case, the information is only flowing one way, so there is no feedback available to improve the system or change its behavior.

This can be a problem for neural stimulation in particular if there is no immediate data about how the stimulator is affecting its targets. So far, in cases like spinal implants for chronic pain, this has been addressed by relatively frequent doctor visits and parameter tuning of the device, but this latency between turning the stimulation on and having someone evaluate the results could be months.

With more mature methods of recording and stimulation, there have been many successful projects to close the data loop and combine both technologies into more intelligent and adaptable systems. [(11)](#references)

A first application is an improved version of the chronic spinal cord stimulator mentioned above. Rather than running without feedback, if a device knows the stimulation patterns it is using and takes those into account while recording, it can isolate what effects the stimulation is having on the surrounding neurons. These systems can adapt on the fly by adjusting the dosage of stimulation to have the best therapeutic effects. [(12, 13)](#references)

Similarly, other systems listen to cortical activity for signs of epileptic seizure activity. When early signs of a seizure are detected, the device can immediately intervene by delivering stimulation meant to halt the spread of abnormal neural firing and stop the seizure. [(14, 15)](#references) Systems like this, designed for immediate intervention, may be built for motor disorders or other patterns of neural activity as well.

![Regaining locomotion](https://www.nature.com/polopoly_fs/7.40458.1478773480!/image/monkey-graphic-online_NATURE.jpg_gen/derivatives/landscape_630/monkey-graphic-online_NATURE.jpg)

Separating the targets of recording and stimulation to different areas of the nervous system can also have compelling and restorative applications. Several groups have combined recording from motor areas in the brain with neural stimulation in lower limbs to regain the ability to walk in animals with spinal cord injury. [(16, 17)](#references) By listening for characteristic patterns of activity signaling leg movements and using those as triggers for the lower-limb stimulation, the spinal cord damage was bypassed and the animals were able to walk using their own voluntary mental activity. This type of device has a promising future in overcoming paralysis and spinal cord damage. [(18)](#references)


## Applications and Public Perception
Gena’s material


## References

1. *Disclaimer:* this terminology isn’t technically correct! It is only meant here to intuitively indicate the direction of data flow. More accurate terms would be “recording” and “modulating”. “Reading” and “writing” have been used to set up an analogy of the brain to a hard drive, which is an outdated comparison. That analogy would imply a number of incorrect things about brain function, including an overestimation of how precisely we can decode neural information or elicit specific effects. For those reasons, I am not promoting that analogy.
2. https://en.wikipedia.org/wiki/Neuroimaging
3. https://www.openwater.cc/technology
4. Lu, Y., Lyu, H., Richardson, A. G., Lucas, T. H., & Kuzum, D. (2016). Flexible Neural Electrode Array Based-on Porous Graphene for Cortical Microstimulation and Sensing. Scientific Reports, 6(1). https://www.nature.com/articles/srep33526
5. Neely, R. M., Piech, D. K., Santacruz, S. R., Maharbiz, M. M., & Carmena, J. M. (2018). Recent advances in neural dust: towards a neural interface platform. Current Opinion in Neurobiology, 50, 64–71. https://www.ncbi.nlm.nih.gov/pubmed/29331738
6. Schwarz, D. A., Lebedev, M. A., Hanson, T. L., Dimitrov, D. F., Lehew, G., Meloy, J., … Nicolelis, M. A. L. (2014). Chronic, wireless recordings of large-scale brain activity in freely moving rhesus monkeys. Nature Methods, 11(6), 670–676. https://www.nature.com/articles/nmeth.2936
7. http://news.berkeley.edu/2016/08/03/sprinkling-of-neural-dust-opens-door-to-electroceuticals/
8. Hong, G., Yang, X., Zhou, T., & Lieber, C. M. (2018). Mesh electronics: a new paradigm for tissue-like brain probes. Current Opinion in Neurobiology, 50, 33–41. https://www.sciencedirect.com/science/article/pii/S0959438817301952
9. Zhou, T., Hong, G., Fu, T.-M., Yang, X., Schuhmann, T. G., Viveros, R. D., & Lieber, C. M. (2017). Syringe-injectable mesh electronics integrate seamlessly with minimal chronic immune response in the brain. Proceedings of the National Academy of Sciences, 114(23), 5894–5899. http://www.pnas.org/content/114/23/5894
10. http://news.mit.edu/2017/noninvasive-method-deep-brain-stimulation-0601
11. Cha, K.S., Yeo, D. & Kim, K.H. Biomed. Eng. Lett. (2016) 6: 113. https://link.springer.com/article/10.1007/s13534-016-0231-5
12. https://neuronewsinternational.com/closed-loop-spinal-cord-stimulation-may-represent-new-paradigm-mitigate-tolerance/
13. Russo, M., Cousins, M. J., Brooker, C., Taylor, N., Boesel, T., Sullivan, R., … Parker, J. (2017). Effective Relief of Pain and Associated Symptoms With Closed-Loop Spinal Cord Stimulation System: Preliminary Results of the Avalon Study. Neuromodulation: Technology at the Neural Interface, 21(1), 38–47. https://www.ncbi.nlm.nih.gov/pubmed/28922517
14. Pais-Vieira, M., Yadav, A. P., Moreira, D., Guggenmos, D., Santos, A., Lebedev, M., & Nicolelis, M. A. L. (2016). A Closed Loop Brain-machine Interface for Epilepsy Control Using Dorsal Column Electrical Stimulation. Scientific Reports, 6(1). https://www.nature.com/articles/srep32814
15. https://www.epilepsy.com/learn/treating-seizures-and-epilepsy/devices/vagus-nerve-stimulation-vns
16. Wenger, N., Moraud, E. M., Raspopovic, S., Bonizzato, M., DiGiovanna, J., Musienko, P., … Courtine, G. (2014). Closed-loop neuromodulation of spinal sensorimotor circuits controls refined locomotion after complete spinal cord injury. Science Translational Medicine, 6(255), 255ra133-255ra133. http://stm.sciencemag.org/content/6/255/255ra133
17. Borton, D., Bonizzato, M., Beauparlant, J., DiGiovanna, J., Moraud, E. M., Wenger, N., … Courtine, G. (2014). Corticospinal neuroprostheses to restore locomotion after spinal cord injury. Neuroscience Research, 78, 21–29. https://www.sciencedirect.com/science/article/pii/S0168010213002228
18. https://www.sciencedaily.com/releases/2014/06/140625130137.htm


</div> <!-- end of content column -->
</div> <!-- end of row -->
