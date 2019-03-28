# Type-2 Diabetes Data Dictionary


The Type-2 Diabetes or T2D dataset includes data extracted from the Indiana Network of Patient Care for patients presenting with Diabetes. The dataset consists of 5 tables: 
1. Patients table (patients.csv)
2. Prescription medication table (medication.csv)
3. Encounters table (encounter.csv)
4. Diagnoses and visit types table (diagnosis.csv)
5. Clinical variables (e.g. tests, measurements etc.) table (clinical_vars.csv)

## Patients table  
This is the master patient index (MPI) of all patients in the registry. All rows are unique and identify a distinct patient with T2D.

### Meta-data
Number of observations: 77,908
Number of variables: 14

| **Variable**       | **Variable Description**                                                                                                                                                                        |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| studyid        | Patient identifier                                                                                                                                                                          |
| index_year     | Year of Diabetes Diagnosis                                                                                                                                                                  |
| index_age      | Age at Diagnosis                                                                                                                                                                            |
| gender         | Gender                                                                                                                                                                                      |
| race           | Race                                                                                                                                                                                        |
| t2d_status     |  Describes how the patient was identified as a T2D patient. This could be one of following methods  1. ICD diagnosis alone 2. HbA1C alone 3. Meds alone 4. Combination of any of the above. |
| cardiovascular | Cardiovascular disease status: Yes/No                                                                                                                                                       |
| nephropathy    | Nephropathy status: Yes/No                                                                                                                                                                  |
| liver          | Liver disease status: Yes/No                                                                                                                                                                |
| enc_12m_bf     | Encounters in 12 month period before index event                                                                                                                                            |
| enc_12m_af     | Encounters in 12 month period before index event                                                                                                                                            |
| enc_yrs_bf     | Number of years of encounter data before the index event                                                                                                                                    |
| enc_yrs_af     | Number of years of encounter data after the index event                                                                                                                                     |
| biobank        | Availability of biobank data for patient: Yes/No                                                                                                                                            |

## Medications table
Number of observations: 709,744
Number of variables: 7

### Meta-data
This contains prescription data for all patients in the registry. Rows are **NOT** unique, i.e. there are multiple rows for a given patient. The total number of unique patients may not necessarily be equal to the MPI.


| **Variables**         | **Variable description**                                       |
|-----------------------|----------------------------------------------------------------|
| studyid               | Patient identifier                                             |
| drug_name             | Name of the drug                                               |
| strength              | Strength (e.g. 20mg, 500 mg etc)                               |
| number_of_days_supply | Total number of days supplied                                  |
| days_med_index        | Day medication was prescribed in terms of days from/to the index event a given medication was prescribed |
| ndc_code              | 11-digit national drug  code                                   |
| dispense_amount       | Number of pills/units dispensed                                |

## Encounters table
Number of observations: 7,891,799 
Number of variables: 4

### Meta-data
This contains the encounter type for patient encounters in the registry. Rows are **NOT** unique, i.e. there are multiple rows for a given patient. The total number of unique patients may not necessarily be equal to the MPI.

| **Variables**          | **Variable description**                            |
|------------------------|-----------------------------------------------------|
| studyid                | Patient identifier                                  |
| days_enc_index         | Encounter day in terms of days from/to index event  |
| care_setting_name      | Care setting (e.g. Outpatient, Inpatient etc.)      |
| location_point_of_care | Actual location ( e.g. X hospital, Y Pharmacy etc.) |

## Diagnosis table
This contains the diagnosis list for all patients in the registry. Rows are **NOT** unique, i.e. there are multiple rows for a given patient. The total number of unique patients may not necessarily be equal to the MPI.

### Meta-data
Number of observations: 9,195,539                          
Number of variables: 3                          

| **Variables**     | **Variable Description**               |
|---------------|------------------------------------|
| studyid      | Patient identifier                 |
| days_dx_index | Number of days from/to index event |
| dx_code       | ICD9 diagnosis code                |


## Clinical variables table
Number of observations: 27,776,723
Number of variables: 7

### Meta-data

| **Variables**  | **Variable description**                                                                                                                                                                                                                                                                                                            |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| studyid        | Patient identifier                                                                                                                                                                                                                                                                                                                  |
| type           |  Description of type of `obs` variable.   (e.g. Phenotypes for `obs` values that describe the phenotype such as Weight, BP etc., Medication if `obs` value is a drug name etc.)                                                                                                                                                     |
| coded_code     | Code for observation. This may contain CPT, HCPCS or organization level codes                                                                                                                                                                                                                                                       |
| days_vis_index | Day on which a given observation, test, medication etc. was orderd in terms of days from/to the index event                                                                                                                                                                                                                         |
| obs            | Actual name of the type of observation (e.g. Weight, Order, Pulse, Medication name in case of medications etc.)                                                                                                                                                                                                                     |
| obsvalue       | Values of observation types in `obs` variable for quantitative clinical vars (i.e. tests where results are numbers)                                                                                                                                                                                                                 |
| code_name      |  Values of observation types in `obs` variable for qualitative clinical vars (i.e. tests with results of positive/negative for instance) e.g. if `obs` has value of "ABO Grouping", `code_name` may have a value of "group O" (actual  blood group), if `obs` has "Weight (lbs)" `code_name` may have "140 lbs" (weight value) etc. |
