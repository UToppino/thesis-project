# Hardware acceleration of machine learning algorithms for extreme edge computing
## Master's Thesis Project - Computer Engineering (Embedded Systems) @ Politecnico di Torino

### Introduction
### Results
#### Major Peaks - 15 features
The algorithms finds the heartbeat major peaks (P,Q,R,S,T) and uses them as inputs to the NN
NN inputs:
- R(i-1) ampl only
- S(i-1) ampl and time
- T(i-1) ampl and time
- P(i) ampl and time
- Q(i) ampl and time
- R(i) ampl and time
- S(i) ampl and time
- T(i) ampl and time
  
Total of 15 features.

Amplitudes are calculated with the total average of the signal as 0 reference

Times of the various points are calculated as offsets from the R(i-1) point of each heartbeat
```
MODEL NAME: 
```

#### Major Peaks + middle points - 
Same as above but in between two major peaks the middle point of the signal is added.
NN inputs:
- R(i-1) ampl only
- R(i-1)-S(i-1) middle point ampl and time
- S(i-1) ampl and time
- S(i-1)-T(i-1) middle point ampl and time
- T(i-1) ampl and time
- T(i-1)-P(i) middle point ampl and time
- P(i) ampl and time
- P(i)-Q(i) middle point ampl and time
- Q(i) ampl and time
- Q(i)-R(i) middle point ampl and time
- R(i) ampl and time
- R(i)-S(i) middle point ampl and time
- S(i) ampl and time
- S(i)-T(i) middle point ampl and time
- T(i) ampl and time
