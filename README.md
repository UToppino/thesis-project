# Hardware acceleration of machine learning algorithms for extreme edge computing
### Master's Thesis Project - Computer Engineering (Embedded Systems) @ Politecnico di Torino

## Background

#### ***TODO***: spiegare la struttura del battito cardiaco, le varie onde PQRST, le aritimie da classificare.

## Summary
### Progression of tests:
- **Normalized dataset:**
   - **CNN + MLP**: Classic structure of convolution layers to extract features and MLP classification.
   - **Peak/Valley (or Picchi/Valli) + MLP**: The signal is analyzed, and peaks and valleys are extracted depending on the signal shape. The MLP classifier uses the peaks and valleys as inputs.

- **Original dataset:**
  - **Peak/Valley (or Picchi/Valli) + MLP**: As before.
  - **Major Peaks + MLP**: The important waves of the ECG signal are identified (P-Q-R-S-T waves), the peak amplitude of each wave is extracted, and these points are used as inputs to the MLP classifier.
  - **Major Peaks + KNN**: Same as above, but the classification is done using the KNN algorithm. This test is intended to compare the KNN and MLP classification methods.

- **Original dataset - single heartbeats:** (heartbeat is centered around the R-wave and cut to a fixed length)
  - **Whole beat + MLP**: The whole beat of length N is used for classification. This is not feasible on final hardware due to memory constraints.
  - **Random points + MLP**: A set of random points with a set distribution is extracted and used for classification.
  - **Peak/Valley (or Picchi/Valli) + MLP**: Points are extracted with the same algorithm as before. A set number of points is considered, the points are symmetrical with respect to the center of the beat (R-wave).


## Tests on normalized dataset

#### CNN + MLP

#### Peak/Valley + MLP

## Tests on original dataset

#### Peak/Valley + MLP

#### Major Peaks + MLP / KNN
Different selections of points are tested:
- Single Beat v1 : 12 features
- Single Beat v2 : 15 features
- Single Beat v3 : 21 features (same as v2 + 3 middle points)
- Multiple Beats v1 : 19 features
- Multiple Beats v2 : 15 features
- Multiple Beats v3 : 17 features

Detailed selection of points for all versions at [Major Peaks + MLP](/docs/major_peaks_mlp.md)

The extracted features are used as input for the classifier, either MLP or KNN