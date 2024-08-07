## Major Peaks
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
|  |  |  |  |  |  |  |
|  |  |  |  |  |  |  |




0.9216320971671162