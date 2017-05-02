---
layout: page-fullwidth
show_meta: false
title: "Prerpocessing IPython Notebook"
subheadline: ""
teaser: "Add a short introduction/teaser about your content here. A short paragraph will do. Perhaps be specific about what you cover so that people reading have a clear idea of what they will find. "
header:
   image_fullwidth: ""
permalink: "/preprocessing_notebook/"
---

[Download the notebook](../scripts/preprocessing.ipynb)

```python
import mne
from mne.datasets.brainstorm import bst_raw  
data_path = bst_raw.data_path()

raw_fname = data_path + '/MEG/bst_raw/' + \
                        'subj001_somatosensory_20111109_01_AUX-f_raw.fif'
raw = mne.io.read_raw_fif(raw_fname, preload=True)
raw.plot()
```

    Using default location ~/mne_data for brainstorm...
    
    License
    -------
    This tutorial dataset (EEG and MRI data) remains a property of the MEG Lab,
    McConnell Brain Imaging Center, Montreal Neurological Institute,
    McGill University, Canada. Its use and transfer outside the Brainstorm
    tutorial, e.g. for research purposes, is prohibited without written consent
    from the MEG Lab.
    
    If you reference this dataset in your publications, please:
    
        1) acknowledge its authors: Elizabeth Bock, Esther Florin, Francois Tadel
           and Sylvain Baillet, and
        2) cite Brainstorm as indicated on the website:
           http://neuroimage.usc.edu/brainstorm
    
    For questions, please contact Francois Tadel (francois.tadel@mcgill.ca).
    Agree (y/[n])? y
    Downloading or reinstalling data archive bst_raw.tar.gz at location C:\Users\Yana\mne_data
    
