# OSIC-Pulmonary-Fibrosis-Progression

The aim of this Notebook is to predict a patient’s severity of decline in lung function based on a CT scan of their lungs. Lung function is assessed based on output from a spirometer, which measures the forced vital capacity (FVC), i.e. the volume of air exhaled.

In the dataset, you are provided with a baseline chest CT scan and associated clinical information for a set of patients. A patient has an image acquired at time Week = 0 and has numerous follow up visits over the course of approximately 1-2 years, at which time their FVC is measured.

In the training set, you are provided with an anonymized, baseline CT scan and the entire history of FVC measurements.
In the test set, you are provided with a baseline CT scan and only the initial FVC measurement. You are asked to predict the final three FVC measurements for each patient, as well as a confidence value in your prediction.
There are around 200 cases in the public & private test sets, combined. This is split roughly 15-85 between public-private.

Since this is real medical data, you will notice the relative timing of FVC measurements varies widely. The timing of the initial measurement relative to the CT scan and the duration to the forecasted time points may be different for each patient. This is considered part of the challenge of the competition. To avoid potential leakage in the timing of follow up visits, you are asked to predict every patient's FVC measurement for every possible week. Those weeks which are not in the final three visits are ignored in scoring.
</br>

Source : Kaggle challenge</br>

## Columns
train.csv and test.csv </br>
Patient- a unique Id for each patient (also the name of the patient's DICOM folder)</br>
Weeks- the relative number of weeks pre/post the baseline CT (may be negative)</br>
FVC - the recorded lung capacity in ml</br>
Percent- a computed field which approximates the patient's FVC as a percent of the typical FVC for a person of similar characteristics</br>
Age</br>
Sex</br>
SmokingStatus</br>
