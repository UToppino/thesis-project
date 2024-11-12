# Introduction

## Scope of the project
The project aim is to develop and implement an efficient classifier for ECG signals in order to recognize different types of arrythmias. The ideal conclusion would be a trained model able to be implemented on the hardware platform described below. Many different routes were followed in order to reach the goal of the project and their results are presented and discussed in this thesis.


## Hardware platform
The hardware platform on which the algorithm is meant to run is a low-power and low-spec chip called Sensiplus developed by Sensichips. The Sensiplus contains an NPU core called uSLM which implements the standard RISC operations in addition to two ML-oriented custom instructions.
**List and describe the instructions of the uSLM**
### uSLM
The uSLM NPU is composed of 5 main blocks: a 16x16bit FIFO memory which receives the signal data converted by the ADC, a block of registers, the main modified RISC core, an ALU implementing simple arithmetic operations and a 512x16bit RAM memory containing both code instructions and data.
The aim of the project is to minimize the number of operations needed to carry out the classification and the memory footprint of the paramenters and intermediate results of the model.


## Previous results
Results of the previous classification model both before and after quantization

**Describe results of previous works**


## ECG Classification
The aim of the project is to classify ECG signals into 5 different categories:
- [N] Normal Beats
- [S] Supraventricular Premature Beats
- [V] Premature Ventricular Contraction
- [F] Fusion of Ventricular and Normal Beat
- [Q] Unclassifiable Beat
Each of the heartbeat classes has one or more distrinct shapes or timings in the appearance of the different parts of the beat.
The shape of an heartbeat is composed of different waves or peaks: P, Q, R, S, T

**Images of the heartbeats and their peaks**


## Dataset
The dataset utilized is the MIT-BIH Arrhythmia Database, which is openly avalilable on PhysioNet. The dataset is composed of 48 half-hour recordings obtained from 47 subjects. Of these 48 recordings, 23 were chosen randomly from a set containing 4000 24-hour ambulatory ECG recordings and the remaining 25 were chosen to include less common but clinically significant arrhythmias which wouldn't be present in a small random sample.

Each recording is digitized at 360 samples per second per channel with 11-bit resolution over a 10mV range. For each recording only the main channel VLII was considered in this project in order to have a more consistent dataset.

**Describe annotations of the dataset**

**Describe other dataset derived by this one**

## Dataset generation in python
The dataset is downloaded from the PhysioNet site and it's accessible from the code using the wfdb library. Importing the code using the wfdb functions results in multiple numpy arrays containing the ECG recordings in mV as float numbers and arrays containing the annotations of the ECG signals. For the first few tests another dataset derived from the original one was used. 
This second dataset consists of all the ECG heartbeats already cut to a fixed length of 187 samples, all of which are normalized with values between 0 and 1. 
