### Problem Statement
* Predict Length of Stay (LOS) based on Clinical signs found in text and considering structured information such as Age, Gender and major ICD Diagnoses

### Introduction
According to an annual survey conducted by the American Hospital Association, there are a total of 6,093 hospitals in the US which house 920,531 staffed beds. Out of these, 70,098 are adult ICU beds which are predicted to have a 60% occupancy in March 2023, according to the Institute for Health Metrics and Evaluation Covid-19 projections provided 60% of all adult ICU beds are taken by non-Covid patients. 

Secondly, the hospital stays in US costed the health system at least $377.5 billion per year as of 2016, according to an article published by HealthCatalyst and these costs have increased since. Also, the Medical Legislation standardizes payments for all procedures performed on a patient, regardless of the length of stay of the patient.

These numbers provide a tangible ground to analyze and study the average Length of Stay (LOS) in the intensive care unit (ICU) to minimize LoS and lower the chances of getting a hospital-acquired condition such as staph infection. Another benefit is that hospital resources and services can be planned and allocated with maximum efficacy. One approach to predicting LOS is to use a combination of clinical signs found in text and structured information such as age, gender, and major ICD diagnosis.

* **Keywords:** Feed Forward Neural Network, Fully Convolutional Network, ICD Diagnosis, Regression, Gradient Boost 

### Data Collection
* Source(url): https://physionet.org/content/mimiciii/1.4/
* Short Description : MIMIC-III is a large, freely-available database comprising deidentified health-related data associated with over forty thousand patients who stayed in critical care units of the Beth Israel Deaconess Medical Center between 2001 and 2012. The database includes information such as demographics, vital sign measurements made at the bedside (~1 data point per hour), laboratory test results, procedures, medications, caregiver notes, imaging reports, and mortality (including post-hospital discharge).
MIMIC supports a diverse range of analytic studies spanning epidemiology, clinical decision-rule improvement, and electronic tool development. It is notable for three factors: it is freely available to researchers worldwide; it encompasses a diverse and very large population of ICU patients; and it contains highly granular data, including vital signs, laboratory results, and medications.

* **Keywords:** Feed Forward Neural Network, Fully Convolutional Network, ICD Diagnosis, Regression, Gradient Boost

### Methodology
1. We have built 2 types of Neural Network Architectures.

2. The following are the 2 types of architectures we have used - 
 * Feed Forward Neural Network
    * A Feed Forward Neural Network is an artificial neural network in which the connections between nodes does not form a cycle. The feed forward model is the simplest form of neural network as information is only processed in one direction. While the data may pass through multiple hidden nodes, it always moves in one direction and never backwards.
 
 * Fully Convolutional Neural Network
    * A Fully Convolutional Neural Network (FCN) for 1-dimensional data is a type of neural network architecture that consists entirely of convolutional layers, without any fully connected layers. FCNs for 1D data are powerful models that can automatically learn features from raw signals, without the need for manual feature engineering.
 
3. Keywords: Feed Forward Neural Network, Fully Convolutional Network, ICD Diagnosis, Regression, Gradient Boost

4. Models were compiled and fit as inspired by the following github repositories - 
  * Feed Forward Neural Networks
    * MLH Repo - https://github.com/sdasara95/Machine-Learning-in-Healthcare
    * usama Repo - https://github.com/usama6679/LENGTH-OF-STAY-PREDICTION-AT-TIME-OF-AhhDMISSION
  * Fully Convolutional Neural Networks
    * NICU Repo - https://github.com/bt-s/NICU-length-of-stay-prediction

  These models will be further tuned with the helped of the Keras Tuner.

5. Model Evaluation
  * The models will be evaluated with the help of the following performance metrics - 
    * Mean Squared Error - This would help us in understanding the best models for minimizing the prediction errors
    * Mean Absolute Error - This would help us understand the best models with the smallest average deviation from the actual values
    * R-Squared Value - This will help us explain the largest proportion of variance in the data

### How to run the code - 
* Prerequisites - Ability to run .ipynb files in either Jupyter Notebook or Google Colaboratory, Access to the MIMIC-III dataset from PhysioNet
* Open the .ipynb file on your environment. The file path for the .csv files downloaded from the MIMIC-III dataset needs to be updated on the code for it to import the data.
* All the code cells are ready to run sequentially. 
* The Google Drive mount is not required if the files are not imported from Google Drive.