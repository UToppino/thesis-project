# Thesis structure

## Chaper 0: Introduction
### ECG classification
### Hardware constraints
### Previous results
### Dataset explanation
#### Dataset generation in python
### Description of metrics to consider

## Chapter 1: CNN + MLP normalized dataset
### Problems with using this method
### Results

## Chapter 2: Picchi/Valli + MLP normalized dataset
### Idea behind Picchi/Valli alogorithm
### Problems
#### Low precision
#### Parameters depend on the current signal
### Results

## Chapter 3: moving to the raw waveforms
### Difference between normalized dataset and raw dataset

## Chapter 4: Picchi/Valli + MLP original dataset
### Improvement w.r.t. same method on normalized dataset
#### Realistic algorithm to use in "real-time"
### Results

## Chapter 5: Major Peaks + MLP original dataset
### Improvements w.r.t picchi/valli
#### More specialized algorithm to extract specific points of the ECG signal
#### More overhead in terms of computational power
### Results
#### Comparison of results with picchi/valli with similar MLP classifiers

## Chapter 6: Picchi/valli + MLP on single heartbeat
### Improvement w.r.t. picchi/valli
#### Points are around the R-peak
#### Easier to optimize the classification model

## Chapter 7: comparison of all methods
### Graph of different methods together
### Comparison with KNN classifier as golden model

## Chapter 8: future steps
### Hardware implementation
### Different model types
#### Spiking Neural Networks
#### Long Short Term Memory

