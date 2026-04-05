Data Set: FD001
Train trjectories: 100
Test trajectories: 100
Conditions: ONE (Sea Level)
Fault Modes: ONE (HPC Degradation)


Experimental Scenario

The dataset is composed of multiple multivariate time series, each representing a different engine from a fleet of identical units. Every dataset is split into training and testing subsets. Each engine begins operation with unknown levels of initial wear and manufacturing variability; however, these differences are considered normal and not indicative of faults.

Three operational settings that significantly influence engine performance are included in the data, which also contains sensor noise.

At the beginning of each time series, the engine operates under normal conditions. Over time, a fault develops. In the training set, this fault progressively increases until complete system failure occurs. In contrast, the test set ends before failure happens.

The goal is to predict the Remaining Useful Life (RUL) for each engine in the test set, defined as the number of operational cycles remaining after the final recorded cycle. A vector containing the true RUL values for the test data is also provided.

The data is supplied as text files with 26 space-separated columns. Each row corresponds to a single operational cycle, and each column represents a different variable. The columns correspond to:

1)	unit number
2)	time, in cycles
3)	operational setting 1
4)	operational setting 2
5)	operational setting 3
6)	sensor measurement  1
7)	sensor measurement  2
...
26)	sensor measurement  26


