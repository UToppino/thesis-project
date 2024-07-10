# Hardware acceleration of machine learning algorithms for extreme edge computing
#### Master's Thesis Project - Computer Engineering (Embedded Systems) @ Politecnico di Torino

## Introduction
Some model results are available at [models_info](/models_info.md)
## Results
### MLP Networks
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

### KNN Networks
#### Major Peaks (old system) - KNN - 12 features
```
Num features: 12
     K  Test Score  Train Score
0    3    0.633250     0.825078
1    4    0.644459     0.793134
2    5    0.647015     0.772689
3    6    0.649666     0.756384
4    7    0.651305     0.743553
5    8    0.650852     0.733722
6    9    0.650238     0.725078
7   10    0.648870     0.717870
8   11    0.646339     0.711128
9   12    0.644050     0.705194
10  13    0.643859     0.699329
11  14    0.642633     0.694102
12  15    0.641281     0.689236
13  16    0.638970     0.684766
14  17    0.637627     0.680797
15  18    0.636307     0.676727
16  19    0.634025     0.673042
```
#### Major Peaks - KNN - 15 features
```
Num features: 15
     K  Test Score  Train Score
0    3    0.671955     0.848366
1    4    0.682430     0.818626
2    5    0.684354     0.798191
3    6    0.683772     0.782340
4    7    0.682366     0.769308
5    8    0.681351     0.758000
6    9    0.678770     0.748967
7   10    0.674217     0.741149
8   11    0.673804     0.733657
9   12    0.671998     0.727280
10  13    0.670204     0.721296
11  14    0.667902     0.716099
12  15    0.666427     0.711187
13  16    0.664202     0.706882
14  17    0.661706     0.703044
15  18    0.660305     0.699380
16  19    0.658310     0.695382
```
#### Major Peaks + 3 middle points - KNN - 21 features
```
Num features: 21
     K  Test Score  Train Score
0    3    0.666491     0.844553
1    4    0.676129     0.815413
2    5    0.679218     0.795164
3    6    0.680350     0.779253
4    7    0.679626     0.766453
5    8    0.676771     0.756164
6    9    0.676867     0.746620
7   10    0.674868     0.738770
8   11    0.673640     0.731812
9   12    0.671858     0.725601
10  13    0.669880     0.720217
11  14    0.667959     0.714916
12  15    0.664496     0.710375
13  16    0.662128     0.705370
14  17    0.659858     0.701349
15  18    0.658376     0.697538
16  19    0.656946     0.693732
```

#### All points - 187 pts/beat
```
     K  Test Score  Train Score
0    3    0.784120     0.903849
1    4    0.788346     0.883752
2    5    0.785270     0.869251
3    6    0.782037     0.857141
4    7    0.781152     0.847405
5    8    0.775007     0.839027
6    9    0.771242     0.830971
7   10    0.765896     0.824527
8   11    0.764168     0.817941
9   12    0.761722     0.812988
10  13    0.758812     0.807945
11  14    0.756247     0.803636
12  15    0.753874     0.799205
13  16    0.751658     0.795307
14  17    0.748242     0.791357
15  18    0.745489     0.788013
16  19    0.743943     0.784569
```
