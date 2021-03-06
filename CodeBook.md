# Code Book

## Raw data information

The following data set information was obtained from http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data. 

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain.

For each record in the dataset it is provided: 
- Triaxial acceleration from the accelerometer (total acceleration) and the estimated body acceleration.
- Triaxial Angular velocity from the gyroscope. 
- A 561-feature vector with time and frequency domain variables. 
- Its activity label. 
- An identifier of the subject who carried out the experiment.

### Data collection
Data was obtained from the UCI Machine Learning repository:
http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

## Data transformation
A tidy summary dataset was generated from the raw data using the script run_analysis.R

1. The training and test data were merged into a single dataset

2. The means and standard deviations were extracted for all features

3. Activities were recoded to have meaningful names

4. Variables were given more descriptive names

5. The summary data set was created by taking the means of features by activity and subject

6. Columns of the summary dataset were split to create a more readable table

## Tidy summary data set
The summary set contains the means of features by activity and subject

### Rows
* The first row is a header containing the names of variables
* Each additional row contains a single feature

### Columns
* Subject - A numeric ID representing a participant
* Activity - The type of activity being performed (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING)
* Domain - Whether the feature is a measurement of time or frequency (Time or Frequency)
* Signal - Whether the signal is from body or gravity (Body or Gravity)
* Instrument - Measurement instrument (Accelerometer or Gyroscope)
* Variable - (Mean or Standard.Deviation)
* Magnitude - Whether the measurement is of magnitude (TRUE or FALSE)
* Jerk - Whether the measurement is of jerk (TRUE or FALSE)
* Direction - The axis along which the feature is meansured (X, Y, Z, or NA)
* Average - Feature mean computed by activity and subject

