Predictive Maintenance for NASA Turbofan Engines

Problem Overview
In aviation, engine reliability is critical. Maintenance is typically done in two ways:

Reactive maintenance: Fixing components after failure, which can be risky and expensive Scheduled maintenance: Replacing parts at fixed intervals, even if they are still usable

A more efficient approach is to use sensor data to estimate when an engine is likely to fail. This allows maintenance to be performed only when needed.

Objective: Estimate the Remaining Useful Life (RUL) of turbofan engines using sensor data.

Dataset (NASA CMAPSS – FD001) Input: Time-series data from 21 sensors (e.g., temperature, pressure, speed) Scenario: Engines operate normally at first, then gradually degrade until failure Target: Remaining Useful Life (RUL), measured in cycles
Methodology A. Data Cleaning and Feature Selection


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


