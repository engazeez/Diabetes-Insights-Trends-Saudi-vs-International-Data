# Diabetes Insights & Trends (Saudi vs International Data)

---
## Problem Statement

In 2019 alone, 1.5 million people have died due to diabetes and estimates indicate that 463 million people are living with diabetes all over the world3. According to The World Health Organization, Saudi Arabia has the second highest rate of diabetes in the Middle East, and is seventh in the world for the rate of diabetes. Recent estimates indicate around 7 million of the Saudi population are diabetic and around 3 million have pre-diabetes.In Saudi Arabia, diabetes is one of the most prevalent diseases impacting the quality of life of many individuals and causing an immeasurable health and financial burden on the country’s economy


## Objectives

Here, we explore the prevalence of diabetes, examine the comorbidities and predictive factors of diabetes among the Saudi population.
- Our goal is to improve the quality of life by utilizing the power of artificial intelligence.
- Our objective is to build a machine learning model that identifies undiagnosed diabetic individuals in Saudi Arabia.



## Data Source and requirements
The data was provided by Lean Business Services, a well-known health service provider with immense impact on health data within the kingdom.
Hence, the content, formats, and data representations were therefore prepared in accordance with Lean requirements. Domain knowledge experts were consulted as needed.

---
### Local Data Dictionary

| Column               |Type                  |Mening                     |
|:-------------------|:------------------:|:--------------------:|
|PatientID                 |*int* |*A unique number for each patient* |
|U_Encounter_ID_x                 |*object* |*The patient's visit number* |
|Service Type                 |*object* |*The service that was provided to the patient* |
|Service_Code                 |*object* |*The code is for the service that was provided to the patient* |
|Service Name                 |*object* |*The name of the service that was provided to the patient* |
|U_Encounter_ID_y                 |*object* |*The patient's visit number* |
|Gender                 |*object* |*Male or Female* |
|YearOfBirth                 |*object* |*The year of birth of each patient* |
|Provider Name                 |*object* |*The name of the hospital that provided the service* |
|Discharge Date/Time                 |*object* |*Discharge Date of the patient* |
|Admission Date/Time                 |*object* |*Admission Date of the patient* |
|Encounter_Type                |*object* |*Hospital departement visited by patient* |
|Duration of leave                 |*int* |*The number of days the patient stays in the hospital* |
|Nationality                 |*object* |*Admission Date of the patient* |
|Discharge Mode                 |*object* |*The method upon whitch the patient was discharged  from hospital/clinic* |
|Clinic                 |*object* |*The name of the clinic that received the patient* |
|MaritalStatus                 |*float64* |*The patient's marital status* |
|Diagnosis Description                 |*object* |*Diagnosis Description of the patient* |
|Diagnosis Code                 |*object* |*Diagnosis Code of the patient* |
|Diagnosis Type                 |*object* |*Principal Diagnosis\؟* |
|height                 |*float64* |*Patient height* |
|weight                 |*float64* |*The patient's weight* |
|gender                 |*object* |*Another column to clarify the patient's gender* |
|has_diabetes                 |*bool* |*1 means that the patient has diabetes* |
|has_hypertension                 |*object* |*1 means that the patient has hypertension* |

---
### International Data Dictionary (Without Lab Result)

| Column               |Type                  |Mening                     |
|:-------------------|:------------------:|:--------------------:|
|PatientID                 |*int* |*A unique number for each patient* |
|Benign_essential_hypertension                 |*int* |*1 means that the patient has benign hypertension* |
|Lumbago                 |*int* |*1 means that the patient has low back pain (LBP) or lumbago is a common disorder involving the muscles, nerves, and bones of the back.* |
|Mixed_hyperlipidemia                 |*int* |* Mixed hyperlipidemia is a genetic disorder passed down through family members. 1 means that the patient have this disease, and have higher-than-normal levels of cholesterol, triglycerides, and other lipids in your blood. * |
|Routine_general_medical_examination_at_a_health_care_facility                 |*int* |*1 means that the patient visits the hospital continuously for checks* |
|DMIndicator                 |*int* |*1 means that the patient have diabetes* |
|Gender                 |*object* |*Male or Female* |
|YearOfBirth                 |*int* |*The year of birth of each patient* |
|Location                 |*object* |*The city of every patient* |
|Smoking Status Indicator                 |*int* |*We don't know what he's referring to* |
|Lipitor Atorvastatin                 |*int* |*Atorvastatin (Lipitor) is a medication prescribed by a doctor to lower cholesterol in people who have been diagnosed with high cholesterol (high levels of cholesterol in the blood). 1 means that the patient is taking this medicine* |
|Lisinopril                 |*int* |*Lisinopril is used to treat high blood pressure. 1 means that the patient is taking this medicine* |
|Simvastatin                 |*int* |*medicine used to lower cholesterol. 1 means that the patient is taking this medicine* |


### International Data Dictionary (With Lab Result)

| Column               |Type                  |Mening                     |
|:-------------------|:------------------:|:--------------------:|
|PatientID                 |*int* |*A unique number for each patient* |
|Benign_essential_hypertension                 |*int* |*1 means that the patient has benign hypertension* |
|Lumbago                 |*int* |*1 means that the patient has low back pain (LBP) or lumbago is a common disorder involving the muscles, nerves, and bones of the back.* |
|Mixed_hyperlipidemia                 |*int* |Mixed hyperlipidemia is a genetic disorder passed down through family members. 1 means that the patient have this disease, and have higher-than-normal levels of cholesterol, triglycerides, and other lipids in your blood.|
|Routine_general_medical_examination_at_a_health_care_facility                 |*int* |*1 means that the patient visits the hospital continuously for checks* |
|DMIndicator                 |*int* |*1 means that the patient have diabetes* |
|Gender                 |*object* |*Male or Female* |
|YearOfBirth                 |*int* |*The year of birth of each patient* |
|Location                 |*object* |*The city of every patient* |
|Smoking Status Indicator                 |*int* |*We don't know what he's referring to* |
|Lipitor Atorvastatin                 |*int* |*Atorvastatin (Lipitor) is a medication prescribed by a doctor to lower cholesterol in people who have been diagnosed with high cholesterol (high levels of cholesterol in the blood). 1 means that the patient is taking this medicine* |
|Lisinopril                 |*int* |*Lisinopril is used to treat high blood pressure. 1 means that the patient is taking this medicine* |
|Simvastatin                 |*int* |*medicine used to lower cholesterol. 1 means that the patient is taking this medicine* |
|ReportYear                 |*int64* |*Year of issuance of the report* |
|PanelName                 |*object* |*Individual laboratory tests * |
|ObservationYear                 |*object* |*Observation year* |
|Status                 |*object* |*patient file status* |
|HL7Identifier                 |*object* |*an identifier used by an organization to ID the pt across the various healthcare setting* |
|HL7Text                 |*object* |*The name of the identifier* |
|ObservationValue                 |*float64* |*The test result* |
|Units                 |*object* |*The test unit* |
|ReferenceRange                 |*object* |*Reference range for the test * |
|ResultStatus                 |*object* |*Final\Corrected* |
|AbnormalFlags                 |*object* |*The condition of the patient's test result is abnormal* |
|ObservationYear:1                 |*int64* |*Observation year* |
|IsAbnormalValue                 |*int64* |*1 If you are an abnormal patient test result* |
---

## Folders
**Source:** contains two jupyter notebooks with details of code for both International and local data
**Report:** Contain the technical report file in .doc and .pdf formats.


## Build Requirement

- Python 3.8.5
- Anaconda 3
- Mac OS 11.1
- Microsoft Windows 10
- Ubuntu 20.04.2 LTS
- RAM capacity 8GB or over

---
## CONTRIBUTORS
- Abdulaziz Alsulami | engaziz02@gmail.com 
- Najwa Alsaeedi | najwasaeed44@gmail.com
- Amjaad Alsubaie | amjaad_636@hotmail.com
- Ahmed Adam | am4ma@hotmail.com
---
## Acknowledgements
- Special thanks to MISK academy & MCIT for kindly sponsership our Bootcamp at General Assembly. This capstone would not have been without your generousity and mentorship

- Special gratitude for Lean Business Services for kindly providing us with valuable local & international metadata. It is thorugh leaders like you we march forward into a brighter future.

Sincerely, Green Elbow Feb, 2021
