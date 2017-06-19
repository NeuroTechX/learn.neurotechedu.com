# What are Neural Oscillations?

Neural oscillations are repetitive, rhythmic synchronized frequency patterns in the central nervous system.
They occur during activation of large clusters of neurons, though they can occur with a single neuron as well.
Although the raw data obtained from  electroencephalograms are formatted as a function of time, neural oscillations are visualized in terms of frequency and measured in units of Hertz (Hz); one cycle per second.
As such the neural clusters generate neural oscillations that can be characterized by the frequency range in which they occur:
![Image] (file:///Users/JDF/Desktop/Figures%20generated%20from%20topomap%20example%20with%20eegbci/Brain%20wave%20frequency%20chart.png)
List point:
* Alpha waves (7.5-12.5 Hz). Alpha waves also contain a subset of waves known as mu waves, which occur in the same frequency range but are correlated to the motor cortex. (Need examples of that these connect to)
* Beta waves (13-30 Hz) (need examples of what these connect to)
* Delta waves (1-4 Hz) (need examples of what these connect to)
* Gamma waves (30-70 Hz) (need examples of what these connect to)
* Theta waves (4-8 Hz) (Need examples of what these connect to)

# Why do we produce neural oscillations? 

We do not fully understand why our brain produces neural oscillations.
Some researchers theorize that neural oscillations are nothing more than byproducts of brain activity, indicators of expected brain pattern in response to events of stimulus.
For example, motion produces prdecitable occurrences of alpha waves (in the mu frequency) in the motor cortex,
and sleep cycles are characterized by the alternating flux of different neural waves.
Other researchers have theorized that cetain oscillations, like those that occur in the delta range, are critical to unlocking the mystery of our consciousness. 

# So why do neural oscillations matter?

Neural oscillations are useful in variety of ways.
From a diagnostic and imaging persepective, they can be used as indicators of specific neurological phenomena such as:
* Sleep and the state of consciousness
* Motor control
* Perception and information processing
* Pattern generation
* Memory
* Abnormal neural function, such as epilepsy, and Parkinsons.

Practical applications for extracting neural oscillations using your own BCI could be
looking at the presence of mu waves during motion, or to check if there is a presence of alpha
and beta waves during meditation. You may even want to look at all the different waves that occur
when you are performing a specific task.

# How do we extract neural oscillations as a feature of our EEG data?

As previously mentioned the data obtained by EEF is captured as a function of time, but neural
oscillations are described in units of frequency. In order to transform the data we must
employ a Fourier transform.

<Include image of basic equation>

The Fourier transform is a highly regarded formula which is the mainstay formula
for signal processing and signal decompistion.

<Include gif>

The best way to extract neural oscillations is to perform a Fourier transform on
your preprocessed data and then plot the resulting frequency patterns in the category of
brain waves your interested in seeing. 
You can further preprocess your data to exlude certain channels, or target specific 
frequency ranges to oberseve features of the neural oscillation. 
>See NeuroTechX.edu "Preprocessing" for a detailed look at the preprocessing steps that 
that can be applied to your data.

Before extracting neural oscillations there are several steps that must be undertaken
to prepare you data:
* Importing data, reading data, and formatting data
* Preprocessing
* Epoching
* Assemble a classifier (plotting a topomap)
* and finally, plotting the relevant figure

### Importing, reading, and formatting data

In the below example I have used a dataset created by experimental runs by (reserach reference)
so when the data is fetched it will have already underwent some preprocessing which will not be covered in 
either examples. However in both cases the data will be fetched using the below commands:

subject = 1 <br/>
runs = [3] <br/>
tmin = -0.1 <br/>
tmax = 0.3 <br/>
raw_fnames = eegbci.load_data(subject,runs) <br/>
raw_files = [read_raw_edf(f, preload=True) for f in raw_fnames] <br/>
raw = concatenate_raws(raw_files) <br/>
raw.ch_names.index('STI 014') <br/>
__NEED TO EXPLAIN WHAT THESE DO__ <br/>

Line 2 is relevant in this example, as there are 14 experimental runs to choose from
that were performed in this study and each was tested under different conditions. 
In this experiemtn run 3 measured the eeg signal obtained during movement of the left and right
hands, both speerately and simultaneously. 

### Preprocessing

When plotting power spectral density (psd), only epoching is necessary as we want to see the psd
accross the entire available frequency range. However for topomap plotting you
will need to prepocess you data with a band pass filter to isolate the specific
frequency range you want to visualize. The example below aslo strips the channel names
of their default "." keys to avoid errors when reading your channel names.

### Epoching the data

Epoching is basically segmenting your data into smaller chunks of readable data that contain
events, or fluctuations in the eeg signal (caused by changing signal potential?).
Epoching helps to trunkate the objects you need to analyze into more manageable bytes that contain the 
information you actually want. To epoch your data you can follow the steps below:

events = mne.find_events(raw, stim_channel='STI 014', verbose=True) <br/>
picks = pick_types)raw.info, meg=Fale, eeg=True, stim=False, eog=False, exclude='bas') <br/>
baseline = 0, None <br/>

The above defines the events you want to look for, as well as the type of signal your
program should expect to analyze (meg vs. eeg vs. eog). I selected the eeg=True as the data
we will be looking at was obtained using an EEG headset. Below we continue the 
necessary inputs for epoching:

epochs = Epochs(raw, events, event_id, tmin, tmax, proj=True, picks=picks, baseline-baselin, preload=True) <br/>
epochs_train=epochs.copy().crop(tmin=-0.2,tmax=0.5) <br/>
labels=epochs.events[:,-1]- <br/>

The above code defines the epochs which will be further manipulated. Try the function 
__plot.epochs()__ to see how your data has transformed!

The following steps will diverge depending on the methods of visualization you want 
to apply. Below I will highlight how to use psd to visualize dominant frequencies as well
as topomaps to highlight specific frequencies in localized areas.

### Using PSD to categorize oscillatory occurance based on power spectral content 

Power spectral density measure the power of a signal in (UNITS). The function 
__epochs[events].plot_psd()__ can be used to plot specific epoched events as a function
of power spectral desnity over a specific frequency range. Below is an example of a
script you can run to achieve this. Note that the dataset imported from eegbci is already
preprocessed and transformed using the Fourier function, so the steps you should see below
are:
* Importing, read, and format your data
* Epoch the data
* Plot the data with the __epochs[events].plot_psd()__ 

{{{{Insert figures}}}

### Using a topomap to visualize local oscillations

A classifier will be applied to visualizethe presence of neural oscillations using a 
binary discrimination to highlight whether you have the presence of waves at certain
frequencies or not. While there is a bit of variability on visualizing the strenght of your
signal, this is really simply a "there" or "not there" method of looking at neurons
firing over specific electrodes. Understanding which electrodes correspond to which regions of the brain
will help you to understand where the majority of activity is occurring in the brain.
Plotting PSD to visualize frequency is limited to specific chanels and may require excess work to view the 
local presence of waves. By contrast, topomap offers specific feedback on the local
presence of waves. The classifier assembled in the below example uses a binary 
range characteried by the red positive values and the blue negative values. The total range is from
-0.1 to 1.0 and refers to the electric potential with 1.0 indicating the presence 
of a measureable signal. 

There are several more steps involved with topomap visualization. The first occurs 
in the preprocessing step as you must apply a band pass filter (raw.filter(fmin,fmax)) to
isolate the frequency range that interests you. Refer to the above section where
I break down each wave into their respective frequency range. The below example will be using
a band pass filter for alpha and beta waves isnce the eegbci dataset runs are based on 
on motor cortex activity. 

Five arbitrary time points were chosen in the below example to highlight the shift in wave 
presence over time. Since the run involves squeezing the right and left hands,
we should expect an increase in the alpha wave presence (specifically the mu frequency)
and a reciprocal decrease in beta wave frequency in the area corresponding to either
right or left hand (oposite sides of the brain from the hand involved). Timepoints
4 and 5 illustrate this difference:

