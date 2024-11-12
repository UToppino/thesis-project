# Thesis structure

## Chaper 0: Introduction
### ECG classification
### Hardware constraints
### Previous results
### Dataset explanation
#### Dataset generation in python

## Chapter 1: CNN + MLP normalized dataset
### Problems with using this method
### Results

## Picchi/Valli + MLP normalized dataset
### Idea behind Picchi/Valli alogorithm
### Problems
#### Low precision
#### Parameters depend on the current signal
### Results

## Picchi/Valli + MLP original dataset
### Improvement w.r.t. same method on normalized dataset
#### Realistic algorithm to use in "real-time"
### Results

## Major Peaks + MLP original dataset
### Improvements w.r.t picchi/valli
#### More specialized algorithm to extract specific points of the ECG signal
#### More overhead in terms of computational power
### Results
#### Comparison of results with picchi/valli with similar MLP classifiers

## Picchi/valli + MLP on signale heartbeat
### Improvement w.r.t. picchi/valli
#### Points are around the R-peak
#### Easier to optimize the classification model

