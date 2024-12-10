# Peak Valley + MLP

### Background
The complete waveform of the ECG is cut to single heartbeats, identified thanks to the R-wave. The peak-valley algorithm is run on each heartbeat to identify the important points which are then used as inputs to the MLP model.
The R-wave is the highest peak of the heartbeat and it is considered as its center. The lenght of the heartbeat is the parameter HEARTBEAT_LENGTH, half of the points are before the R-wave and half after so that all heartbeats have the same lenght and no filler data.

### Algorithm description
The algorithm considers 3 consecutive points at a time and finds a local maximum or minimum if the middle one is higher or lower than the other two. A local max or min is kept only if its amplitude with respect to the previous point is over a threshold (DELTA_PEAK). If no peaks are selected for at least a time DELTA_TIME, then the threshold condition is ignored.

### Data conversion
The data type of the original dataset is float, but its precision can be lowered to match the one of a 16bit or 8bit integer. The actual values must remain in float notation for model training. Points can also be converted from absolute amplitudes to difference amplitudes, by dubtracting to each point's amplitude the amplitude of the previous point.

### MLP training
From the resulting peaks only a number equal to POINTS_LENGTH of points is considered for training. The points are selected randomly. The chosen points are fed to the MLP network.

## Some results


