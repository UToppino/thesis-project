# Major Peaks + MLP / KNN - Results

## MLP Classification
### 12 features (old system):
#### 2 dense layers size 10
- mjpk_00 - avg categories 0.713
- mjpk_01 - accuracy: 0.8525 - avg categories 0.601
- mjpk_02 - accuracy: 0.7700 - avg categories 0.586
#### 2 dense layers size 20
- mjpk_03 - accuracy: 0.8670 - avg categories 0.720
- mjpk_04 - accuracy: 0.8650 - avg categories 0.749
- mjpk_05 - accuracy: 0.8763 - avg categories 0.772
#### 1 dense layer size 30
- mjpk_60 - accuracy: 0.6523 - avg categories 0.497
- mjpk_62 - accuracy: 0.7269 - avg categories 0.612
- mjpk_64 - accuracy: 0.6594 - avg categories 0.526

### 15 features (new system)
#### 2 dense layers size 10
- mjpk_06 - accuracy: 0.8485 - avg categories 0.687
- mjpk_07 - accuracy: 0.8328 - avg categories 0.767
- mjpk_08 - accuracy: 0.8505 - avg categories 0.691
#### 2 dense layers size 20
- mjpk_09 - accuracy: 0.8802 - avg categories 0.749
- mjpk_10 - accuracy: 0.8706 - avg categories 0.718
- mjpk_11 - accuracy: 0.8728 - avg categories 0.731
#### 1 dense layer size 30
- mjpk_54 - accuracy: 0.5831 - avg categories 0.488
- mjpk_55 - accuracy: 0.6152 - avg categories 0.509
- mjpk_57 - accuracy: 0.6240 - avg categories 0.516

### 21 features (new system + 3 middle points)
#### 2 dense layers size 10
- mjpk_12 - accuracy: 0.7685 - avg categories 0.548
- mjpk_13 - accuracy: 0.8409 - avg categories 0.733
- mjpk_14 - accuracy: 0.7502 - avg categories 0.525
- mjpk_18 - accuracy: 0.8198 - avg categories 0.632
- mjpk_19 - accuracy: 0.8514 - avg categories 0.668
#### 2 dense layers size 20
- mjpk_15 - accuracy: 0.8886 - avg categories 0.804
- mjpk_16 - accuracy: 0.9041 - avg categories 0.797
- mjpk_17 - accuracy: 0.9051 - avg categories 0.802
#### 1 dense layer size 30
- mjpk_48 - accuracy: 0.6170 - avg categories 0.549
- mjpk_49 - accuracy: 0.6379 - avg categories 0.568 
- mjpk_51 - accuracy: 0.6479 - avg categories 0.518

## Multiple Beats
### 19 features (multiple beats v1)
#### 2 dense layers size 10
- mjpk_20 - accuracy: 0.7829 - avg categories 0.517
- mjpk_21 - accuracy: 0.7679 - avg categories 0.570
- mjpk_22 - accuracy: 0.7583 - avg categories 0.581
#### 2 dense layers size 20
- mjpk_23 - accuracy: 0.8395 - avg categories 0.614
- mjpk_24 - accuracy: 0.8134 - avg categories 0.616
- mjpk_25 - accuracy: 0.8134 - avg categories 0.616
#### 2 dense layers size 20 - custom weights
- mjpk_26 - accuracy: 0.6039 - avg categories 0.484
- mjpk_27 - accuracy: 0.5162 - avg categories 0.391
- mjpk_28 - accuracy: 0.6068 - avg categories 0.511
#### 1 dense layer size 30
- mjpk_61 - accuracy: 0.7448 - avg categories 0.545
- mjpk_63 - accuracy: 0.7704 - avg categories 0.801
- mjpk_65 - accuracy: 0.7627 - avg categories 0.559

#### All following runs have TF determinism enabled
#### 1 dense layer size 30 - weights Zero() - bias Zero()
- mjpk_72 - accuracy: 0.6806 - avg categories 0.1359
- mjpk_73 - accuracy: 0.6806 - avg categories 0.1359
#### 1 dense layer size 30 - weights Ones() - bias Zero()
- mjpk_74 - accuracy: 0.6806 - avg categories 0.1359
- mjpk_75 - accuracy: 0.6806 - avg categories 0.1359
#### 1 dense layer size 30 - weights GlorotNormal(fixed seed) - bias Zero()
- mjpk_84 - accuracy: 0.7676 - avg categories 0.4946
- mjpk_85 - accuracy: 0.7676 - avg categories 0.4946
#### 1 dense layer size 30 - weights GlorotUniform(fixed seed) - bias Zero() (default)
- mjpk_86 - accuracy: 0.7548 - avg categories 0.5167
- mjpk_87 - accuracy: 0.7548 - avg categories 0.5167


#### 1 dense layer size 30 - weights Zero() - bias Zero() - custom class weights
- mjpk_70 - accuracy: 0.4326 - avg categories 0.1359
- mjpk_71 - accuracy: 0.4326 - avg categories 0.1359
#### 1 dense layer size 30 - weights default
- mjpk_76 - accuracy: 0.7761 - avg categories 0.5835
- mjpk_77 - accuracy: 0.7546 - avg categories 0.7656
- mjpk_78 - accuracy: 0.7351 - avg categories 0.5305
#### 1 dense layer size 30 - weights default - custom class weights
- mjpk_79 - accuracy: 0.5304 - avg categories 0.4072
- mjpk_80 - accuracy: 0.4952 - avg categories 0.3977

### 15 features (multiple beats v2)
#### 2 dense layers size 10
- mjpk_29 - accuracy: 0.7456 - avg categories 0.433
- mjpk_30 - accuracy: 0.7881 - avg categories 0.579
- mjpk_31 - accuracy: 0.7502 - avg categories 0.568
#### 2 dense layers size 20
- mjpk_32 - accuracy: 0.7897 - avg categories 0.743
- mjpk_33 - accuracy: 0.8187 - avg categories 0.593
- mjpk_34 - accuracy: 0.8076 - avg categories 0.609
#### 2 dense layers size 20 - custom weights
- mjpk_35 - accuracy: 0.6793 - avg categories 0.519
- mjpk_36 - accuracy: 0.6848 - avg categories 0.563
- mjpk_37 - accuracy: 0.6951 - avg categories 0.542
#### 1 dense layer size 30 - 
- mjpk_56 - accuracy: 0.7570 - avg categories 0.605
- mjpk_58 - accuracy: 0.7514 - avg categories 0.621
- mjpk_59 - accuracy: 0.7800 - avg categories 0.556
  
### 17 features (multiple beats v3)
#### 2 dense layers size 10
- mjpk_38 - accuracy: 0.7449 - avg categories 0.545
- mjpk_39 - accuracy: 0.7318 - avg categories 0.399
- mjpk_40 - accuracy: 0.7606 - avg categories 0.611
#### 2 dense layers size 20
- mjpk_41 - accuracy: 0.8270 - avg categories 0.749
- mjpk_42 - accuracy: 0.7926 - avg categories 0.611
- mjpk_43 - accuracy: 0.8430 - avg categories 0.759
#### 2 dense layers size 20 - custom weights
- mjpk_44 - accuracy: 0.6955 - avg categories 0.540
- mjpk_45 - accuracy: 0.6695 - avg categories 0.479
- mjpk_46 - accuracy: 0.5611 - avg categories 0.367
#### 1 dense layer size 30 - 
- mjpk_50 - accuracy: 0.8632 - avg categories 0.791
- mjpk_52 - accuracy: 0.7471 - avg categories 0.582
- mjpk_53 - accuracy: 0.7504 - avg categories 0.512



## Summary Table
| Model Name | Features | Classifier | Accuracy | Avg. Categories | Model Init | Notes|
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| mjpk_00 | peak_S0 (12) | MLP (10+10) | / | 0.713 | default |  |
| mjpk_01 | peak_S0 (12) | MLP (10+10) | 0.8525 | 0.601 | default |  |
| mjpk_02 | peak_S0 (12) | MLP (10+10) | 0.7700 | 0.586 | default |  |
| mjpk_03 | peak_S0 (12) | MLP (20+20) | 0.8670 | 0. | default |  |
| mjpk_04 | peak_S0 (12) | MLP (20+20) | 0.8650 | 0. | default |  |
| mjpk_05 | peak_S0 (12) | MLP (20+20) | 0.8763 | 0. | default |  |


## KNN Classification

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

