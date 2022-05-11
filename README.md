## CMS Readmission Rates
DATA602 Final Project

Student: Hala Algrain

[Presentation Video](https://youtu.be/1DGCAwDgovc)

## Overview

The Readmissions Reduction Program (HRRP) uses the Excess Readmission Ratio (ERR) to assess a hospital's performance for 6 conditions: pneumonia, acute myocardial infarction, heart failure, chronic obstructive pulmondary disease, coronary artery bypass graft, and total knee and hip arthroplastry.

## Dataset Description
The dataset sources:

1. ERRs from CMS' [HRRP Program](https://www.cms.gov/Medicare/Medicare-Fee-for-Service-Payment/AcuteInpatientPPS/Readmissions-Reduction-Program)
2. Demographic information from [Census Bureau’s Geocoder API](https://geocoding.geo.census.gov/)
3. Medicaid expansion status from [Kaiser Family Foundation](https://www.kff.org/medicaid/issue-brief/status-of-state-medicaid-expansion-decisions-interactive-map/)

## Problem Statement
Reporting quality measures is very costly with an annual cost of over $15 billion. While the HRRP has successfully reduced readmissions, these reductions are variable acroos hospital and patient population groups; hospitals serving the most vulnerable patients often are penalized the most and have the least amount of improvement. There is also evidence that the HRRP program is associated with increased mortality for heart failure and pneumonia.

Pneumonia in particular is a broad diagnostic label that can encompass a variety of acute and chronic causes e.g. bacterial infection versus post covid-19 pneumonia. Further bringing into question the utlity of how well hospitals can influence change in response to their performance metrics.

## Exploratory Analysis Findings
There is a strong correlation between socioeconomic and racial characteristics of census tracts. CMS ERR calculations ensure they have a mean of zero and standard deviation of 0.08.

## Classification Results
The best model was logistic regression. We admit this dataset is small. Further analysis with a larger sample size is needed to improve generalizability of the results.

## Predictions Using this Dataset
The final model is able to predict estimated readmission ratios for pneumonia that are above 1.0 with 67% accuracy on a test dataset. There was a modest benefit to adding Principal Component Analysis to preprocess the data.

## Potential Next Steps and Follow-ups
To improve upon this preliminary analysis: (1)remove medicaid expansion as a feature and include hospitals in the remaining states, (2) use random forests for feature engineering, (3) conduct a panel analysis with more years.

