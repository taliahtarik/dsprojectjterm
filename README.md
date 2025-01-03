# Healthcare Readmission Data Analysis  

### By Group 1: Taliah, Aysha, and Joe  

---

## **Project Objective**  
Our goal is to create visualizations that display hospital readmission rates across various regions of the United States (Northeast, Southeast, Southwest, Midwest, West). From these visualizations, we aim to answer the following key questions:  

1. **What patterns can be identified in readmission rates across different regions in the U.S.?**  
2. **Which diseases are most commonly contributing to hospital readmissions in different regions?**  
3. **Are there any regional variations in readmission rates for specific diseases?**  
4. **Can geographic factors explain variations in hospital readmission rates?**  

---

## **Data Overview**  

### **Source**  
- [CMS Healthcare Provider Data](https://data.cms.gov/provider-data/dataset/9n3s-kdb3#data-table)  

The dataset tracks **readmission rates** across healthcare facilities in different states, providing insights into healthcare equity and hospital-level performance.  

---

## **Dataset Contains**  
1. **Hospital-Level Information**  
   - Metrics on readmission rates.  

2. **Healthcare Equity Data**  
   - Indicators of equity in care delivery.  

3. **Condition-Specific Metrics**  
   - Data on the following conditions:  
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

## **Research Question**

*What patterns exist regarding hospital readmission rates within various regions in the United States, and what are the diseases most commonly contributing to these readmissions?*

---

## **Similar Research Projects**
*Add research here...*

--- 

## 
///python
import pandas as pd
from google.colab import files
import seaborn as sns
uploaded = files.upload()
file = "FY_2024_Hospital_Readmissions_Reduction_Program_Hospital.csv"
data = pd.read_csv(file)
data.head()
