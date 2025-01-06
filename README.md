# Healthcare Readmission Data Analysis  

### By Group 1: Taliah, Aysha, and Joe  

---

## **Project Objective**  

Our goal is to create visualizations that highlight patterns in hospital readmission rates across U.S. regions (Northeast, Southeast, Southwest, Midwest, West). Specifically, we aim to:  

- Identify regional trends in hospital readmission rates.  
- Determine which diseases most commonly contribute to these readmissions.  

---

# **Research Question**

## *What patterns exist regarding hospital readmission rates within various regions in the United States, and what are the diseases most commonly contributing to these readmissions?*

---

## **Similar Research Projects**

Source: [Forecasting Hospital Readmissions with Machine Learning](https://pmc.ncbi.nlm.nih.gov/articles/PMC9222500/)

Summary: This study focuses on using machine learning techniques to predict hospital readmissions based on real-world inpatient data. It highlights the importance of predicting readmissions as a key strategy for improving patient care and reducing hospital costs. 

It uses similar variables like discharge data, patient demographics, and readmission rates to build predictive models. The findings show that machine learning models allow for better early intervention strategies to reduce unnecessary readmissions. 

---

## **Data Overview**  

### **Source**  
- [CMS Healthcare Provider Data](https://data.cms.gov/provider-data/dataset/9n3s-kdb3#data-table)  

The dataset tracks **readmission rates** across healthcare facilities in different states, providing insights into healthcare equity and hospital-level performance. It contains metrics on readmission rates, and data on on the following conditions:  
     - **PN** (Pneumonia)  
     - **HF** (Heart Failure)  
     - **MI** (Myocardial Infarction)  
     - **COPD** (Chronic Obstructive Pulmonary Disease)  
     - **HKR** (Hip/Knee Replacement)  
     - **CABG** (Coronary Artery Bypass Grafting)  

---

## **Key Variables in the Dataset**  
- **Facility ID**: The unique identifier for each facility or hospital.  
- **State**: The U.S. state where the facility is located.  
- **Measure Name**: The specific medical condition or procedure being measured (e.g., Heart failure, hip replacement). The dataset includes six unique conditions.  
- **Predicted Readmission Rate**: The hospital-specific likelihood of patient readmission.  
- **Expected Readmission Rate**: The national average readmission rate for comparison.  
- **Excess Readmission Ratio**: The ratio comparing predicted (per hospital) to expected (national average) rates of readmission.  
- **Number of Readmissions**: The actual observed number of patients readmitted.  
- **Start and End Date**: The date range of the data collection period.

--- 

## Hospital Readmissions Analysis
### How do the variables correlate? What is the most common readmission condition across all states?

Our pre analysis correlation heatmap revealed a moderate correlation between predicted readmission rates and actual readmissions, serving as a foundational layer to answering the discrepancy between the two. 

<iframe src="https://taliahtarik.github.io/dsprojectjterm/hospitalreadmissions.html" width="100%" height="600px"></iframe>

---

## Excess Readmission Ratio by State 
### How do hospital readmission rates vary, and what patterns can be identified in regional disparities?

This choropleth map provides an interactive overview of hospital readmission trends across the United States, showcasing state-level performance and identifying areas of high risk and effective care management through Excess Readmission Ratios (ERR) across six medical conditions.

<iframe src="https://taliahtarik.github.io/dsprojectjterm/finalday2pt2.html" width="100%" height="600px"></iframe>

<iframe src="https://taliahtarik.github.io/dsprojectjterm/ERRVis.html" width="100%" height="600px"></iframe>

---

## Machine Learning Models 
### How does health equity influence hospital readmission rates, and to what extent can health equity scores predict disparities in readmission outcomes across different regions?
This analysis explores the connection between health equity and hospital readmission rates, which ties directly to our research question.

<iframe src="https://taliahtarik.github.io/dsprojectjterm/HELinReg.html" width="100%" height="600px"></iframe>

![Feature Importances](https://github.com/taliahtarik/dsprojectjterm/raw/main/feature_importances.png)

[View Logistic Regression Interactive Graph](https://github.com/taliahtarik/dsprojectjterm/raw/main/logistic_regression.html)

---

## Limitations
Reducing health equity scores into a binary category may have oversimplified the effects of equity on readmission.

---

## Key Takeaways

1. **Heart Failure**  
   - A leading cause of readmissions nationwide (except pneumonia in two states).

2. **Variation in Readmission Rates**  
   - CABG Surgery: Highest variability.  
   - COPD: Lowest variability (indicates uniform management).  

3. **Excess Readmission Ratios (ERRs)**  
   - Variations highlight opportunities to replicate successful practices or target interventions.

4. **Prediction vs. Reality**  
   - Stacked bar charts show close alignment between hospital predictions and national benchmarks.  
   - Northeast: Minor variations suggest potential areas for fine-tuning prediction models.

---
