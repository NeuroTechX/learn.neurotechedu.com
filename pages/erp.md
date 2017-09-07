---
layout: page-fullwidth
show_meta: false
title: "Event Related Potentials"
subheadline: ""
teaser: "This tutorial will explain how to extract Event Related Potentials "
header:
   image_fullwidth: ""
permalink: "/erp/"
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

# Goals:

* Readers should know which ERP to use in which situation
* Be able to code an algorithm that will extract P300 ERP features for a speller type program

# Terms/Topics to be defined/covered ahead of this article:

* Basics of Machine Learning (features, classifiers, unsupervised, supervised)

1 Feature Extraction
1.1 What is feature extraction
Raw neural data, recorded from an EEG or other BCI device, includes a broad set of information about brain activity and some noise from external interference. Even with minimal noise, the complexity of the data in its raw form can be difficult to interpret. Feature extraction is the process of identifying and extracting meaningful information from raw neural data. This reduces the noise as well as the volume of data, making it easier to identify patterns and improves the accuracy of the BCI.

Some feature extraction methods are unsupervised. They do not use example data labelled with features to learn from. They simply extract the most significant information on their own by discarding similarities and focusing on the differences in the data. These methods include Principal Component Analysis (PCA), Wavelet transform, and more. Other methods like Common Spatial Patterns (CSP) are supervised. They require a set of labelled data to determine the specific patterns you would like to extract.

1.2 Which features to extract
The choice of feature extraction methods will depend on several design choices including the type of brain processes being captured. In this document, we will focus on BCIs based on event-related potentials (ERPs).

The feature extraction step for ERP-based BCIs is fairly simple. The first step is to extract epochs. An epoch is a chunk of an EEG signal with a specified length and synchronised with an event (i.e. the presentation of a stimulus). Statistics of these epochs are then computed to extract features. For example, one may  simply compute the mean voltage recorded at each electrode site during the epoch. This feature is usually sufficient for identifying ERPs.




</div> <!-- end of table section -->
