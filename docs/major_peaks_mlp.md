# Major Peaks + MLP / KNN

## Background
The important waves of the ECG signal are identified (P-Q-R-S-T waves), the peak amplitude of each wave is extracted, and these points are used as inputs to the MLP classifier.

Some model results are available at [Major Peaks MLP/KNN - results](/docs/major_peaks_mlp_results.md)
## Feature extraction algorithms
Details on the considered points for each version of the Major Peaks algorithm.
#### Major Peaks (old system) - MLP - 12 features
The algorithm extracts features from the major peaks and uses them as inputs to the NN

NN inputs:
```
- T(i-1) - R(i-1) amplitude
- P(i) - T(i-1) amplitude
- Q(i) - P(i) amplitude
- R(i) - Q(i) amplitude
- S(i) - R(i) amplitude
- T(i) - S(i) amplitude
- R(i) - R(i-1) time
- T(i-1) - R(i-1) time
- P(i) - T(i-1) time
- R(i) - P(i) time
- S(i) - T(i) time
- T(i) - R(i) time
```

#### Major Peaks - MLP - 15 features
The algorithm finds the heartbeat major peaks (P,Q,R,S,T) and uses them as inputs to the NN

NN inputs:
```
- R(i-1) ampl only
- S(i-1) ampl and time
- T(i-1) ampl and time
- P(i) ampl and time
- Q(i) ampl and time
- R(i) ampl and time
- S(i) ampl and time
- T(i) ampl and time
```
  
Total of 15 features.

Amplitudes are calculated with the total average of the signal as 0 reference

Times of the various points are calculated as offsets from the R(i-1) point of each heartbeat


#### Major Peaks + 3 middle points - MLP - 21 features
Same as above but in between two major peaks the middle point of the signal is added.

NN inputs:
```
- R(i-1) ampl only
- S(i-1) ampl and time
- S(i-1)-T(i-1) middle point ampl and time
- T(i-1) ampl and time
- T(i-1)-P(i) middle point ampl and time
- P(i) ampl and time
- P(i)-Q(i) middle point ampl and time
- Q(i) ampl and time
- R(i) ampl and time
- S(i) ampl and time
- T(i) ampl and time
```

#### Multiple beats v1 - 19 features
The extracted features belong to two different beats.

NN inputs:
```
- R(i-2) ampl only
- T(i-2) ampl and time
- P(i-1) ampl and time
- R(i-1) ampl and time
- T(i-1) ampl and time
- P(i) ampl and time
- Q(i) ampl and time
- R(i) ampl and time
- S(i) ampl and time
- T(i) ampl and time
```

#### Multiple beats v2 - 15 features
Like the previous method, but the T and P peaks of the previous beat are removed. The idea is that only the amplitude and time of the R peak (and so the RR time) is needed

NN inputs:
```
- R(i-2) ampl only
- R(i-1) ampl and time
- T(i-1) ampl and time
- P(i) ampl and time
- Q(i) ampl and time
- R(i) ampl and time
- S(i) ampl and time
- T(i) ampl and time
```

#### Multiple beats v3 - 17 features
An expansion of the v2 method. An additional beat is considered (i-3) and the amplitude and time of R(i-3) are provided

