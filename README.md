[![DOI](https://img.shields.io/badge/DOI-10.82901%2Fnemar.nm000216-blue)](https://doi.org/10.82901/nemar.nm000216)

# P300 dataset BI2015a from a "Brain Invaders" experiment

P300 dataset BI2015a from a "Brain Invaders" experiment.

## Dataset Overview

- **Code**: BrainInvaders2015a
- **Paradigm**: p300
- **DOI**: https://doi.org/10.5281/zenodo.3266929
- **Subjects**: 43
- **Sessions per subject**: 3
- **Events**: Target=2, NonTarget=1
- **Trial interval**: [0, 1] s
- **File format**: mat and csv

## Acquisition

- **Sampling rate**: 512.0 Hz
- **Number of channels**: 32
- **Channel types**: eeg=32
- **Channel names**: Fp1, Fp2, AFz, F7, F3, F4, F8, FC5, FC1, FC2, FC6, T7, C3, Cz, C4, T8, CP5, CP1, CP2, CP6, P7, P3, Pz, P4, P8, PO7, O1, Oz, O2, PO8, PO9, PO10
- **Montage**: 10-10
- **Hardware**: g.USBamp (g.tec, Schiedlberg, Austria)
- **Software**: OpenVibe
- **Reference**: right earlobe
- **Ground**: Fz
- **Sensor type**: wet electrodes
- **Line frequency**: 50.0 Hz
- **Online filters**: no digital filter applied
- **Cap manufacturer**: g.tec
- **Cap model**: g.GAMMAcap
- **Electrode type**: wet
- **Electrode material**: Silver/Silver Chloride

## Participants

- **Number of subjects**: 43
- **Health status**: healthy
- **Age**: mean=23.7, std=3.19
- **Gender distribution**: male=31, female=12
- **BCI experience**: mostly students and young researchers

## Experimental Protocol

- **Paradigm**: p300
- **Task type**: target detection
- **Number of classes**: 2
- **Class labels**: Target, NonTarget
- **Study design**: calibration-less P300-based BCI with modulation of flash duration; three game sessions (9 levels each) with different flash durations (110ms, 80ms, 50ms); resting state and eyes closed recorded before and after sessions; subjects instructed to limit eye blinks, head movements and face muscular contractions
- **Feedback type**: visual (game interface with real-time adaptive Riemannian RMDM classifier)
- **Stimulus type**: oddball paradigm on grid of 36 symbols (1 Target, 35 Non-Target) flashed pseudo-randomly
- **Stimulus modalities**: visual
- **Primary modality**: visual
- **Synchronicity**: synchronous
- **Mode**: online
- **Training/test split**: False
- **Instructions**: destroy target symbol within 8 attempts; aliens move slowly and regularly according to predefined path to maintain attention
- **Stimulus presentation**: SoftwareName=OpenViBE

## HED Event Annotations

Schema: HED 8.4.0 | Browse: https://www.hedtags.org/hed-schema-browser

```
  Target
    ├─ Sensory-event
    ├─ Experimental-stimulus
    ├─ Visual-presentation
    └─ Target

  NonTarget
    ├─ Sensory-event
    ├─ Experimental-stimulus
    ├─ Visual-presentation
    └─ Non-target

```
## Paradigm-Specific Parameters

- **Detected paradigm**: p300
- **Number of targets**: 1
- **Number of repetitions**: 12

## Data Structure

- **Trials**: variable per subject (up to 8 attempts per level, 9 levels per session, 3 sessions)
- **Blocks per session**: 3
- **Trials context**: 9 levels per session with variable duration (average ~5 minutes per session, max 10 minutes)

## Preprocessing

- **Data state**: raw EEG with synchronized USB tagging (reduced jitter using USB digital-to-analog converter)
- **Preprocessing applied**: False
- **Notes**: no digital filter applied during acquisition; tags synchronized with EEG signals to reduce jitter; consistent tagging latency across Brain Invaders databases

## Signal Processing

- **Classifiers**: Riemannian Minimum Distance to Mean (RMDM), adaptive
- **Feature extraction**: Covariance/Riemannian

## Cross-Validation

- **Evaluation type**: cross_session

## BCI Application

- **Applications**: gaming
- **Environment**: small room (4 square meters) with 24 inch screen
- **Online feedback**: True

## Tags

- **Pathology**: Healthy
- **Modality**: Visual
- **Type**: Perception

## Documentation

- **DOI**: 10.5281/zenodo.3266930
- **Associated paper DOI**: hal-02172347
- **License**: CC-BY-4.0
- **Investigators**: Louis Korczowski, Martine Cederhout, Anton Andreev, Grégoire Cattan, Pedro Luiz Coelho Rodrigues, Violette Gautheret, Marco Congedo
- **Senior author**: Marco Congedo
- **Institution**: GIPSA-lab, CNRS, University Grenoble-Alpes, Grenoble INP
- **Address**: GIPSA-lab, 11 rue des Mathématiques, Grenoble Campus BP46, F-38402, France
- **Country**: FR
- **Repository**: Zenodo
- **Data URL**: https://doi.org/10.5281/zenodo.3266930
- **Publication year**: 2019
- **Ethics approval**: Ethical Committee of the University of Grenoble Alpes (Comité d'Ethique pour la Recherche Non-Interventionnelle)
- **How to acknowledge**: Korczowski, L., Cederhout, M., Andreev, A., Cattan, G., Rodrigues, P.L.C., Gautheret, V., Congedo, M. (2019). Brain Invaders calibration-less P300-based BCI with modulation of flash duration Dataset (bi2015a). Technical Report, GIPSA-lab.
- **Keywords**: Electroencephalography (EEG), P300, Brain-Computer Interface, Experiment

## Abstract

This dataset contains electroencephalographic (EEG) recordings of 50 subjects playing to a visual P300 Brain-Computer Interface (BCI) videogame named Brain Invaders. The interface uses the oddball paradigm on a grid of 36 symbols (1 Target, 35 Non-Target) that are flashed pseudo-randomly to elicit the P300 response. EEG data were recorded using 32 active wet electrodes with three conditions: flash duration 50ms, 80ms or 110ms. The experiment took place at GIPSA-lab, Grenoble, France, in 2015.

## Methodology

The experiment was designed to study the influence of the flash duration on a calibration-less P300-based BCI system with wet electrodes and as a screening session for potential candidates for a broader multi-user BCI study. The visual P300 is an event-related potential (ERP) elicited by an expected but unpredictable target visual stimulation (oddball paradigm), with peaking amplitude 240-600 ms after stimulus onset. During the experiment, the output of a real-time adaptive Riemannian Minimum Distance to Mean (RMDM) classifier was used for assessing the participants' command. This scheme allows a calibration-free classifier. Before and after the three game sessions, around one minute of resting state and eyes closed conditions were recorded. The interface of Brain Invaders is composed of 36 aliens. In the Brain Invaders P300 paradigm, a repetition is composed of 12 flashes of pseudo-random groups of six symbols chosen in such a way that after each repetition each symbol has flashed exactly two times. A game session was compounded by nine levels, consisting in a unique and predefined configuration of the 36 symbols of the interface. Aliens slowly and regularly moved according to a predefined path keeping constant the inter-distance between adjacent aliens to maintain high player's attention during the whole experiment.

## References

Korczowski, L., Cederhout, M., Andreev, A., Cattan, G., Rodrigues, P. L. C., Gautheret, V., & Congedo, M. (2019). Brain Invaders calibration-less P300-based BCI with modulation of flash duration Dataset (BI2015a) https://hal.archives-ouvertes.fr/hal-02172347
Appelhoff, S., Sanderson, M., Brooks, T., Vliet, M., Quentin, R., Holdgraf, C., Chaumon, M., Mikulan, E., Tavabi, K., Hochenberger, R., Welke, D., Brunner, C., Rockhill, A., Larson, E., Gramfort, A. and Jas, M. (2019). MNE-BIDS: Organizing electrophysiological data into the BIDS format and facilitating their analysis. Journal of Open Source Software 4: (1896). https://doi.org/10.21105/joss.01896

Pernet, C. R., Appelhoff, S., Gorgolewski, K. J., Flandin, G., Phillips, C., Delorme, A., Oostenveld, R. (2019). EEG-BIDS, an extension to the brain imaging data structure for electroencephalography. Scientific Data, 6, 103. https://doi.org/10.1038/s41597-019-0104-8

---
Generated by MOABB 1.5.0 (Mother of All BCI Benchmarks)
https://github.com/NeuroTechX/moabb
