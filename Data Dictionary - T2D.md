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
### Meta-data

## Encounters table
### Meta-data

## Diagnosis table
This contains the diagnosis list for all patients in the registry. Rows are **NOT** unique, i.e. there are multiple rows for a given patient. The total number of unique patients may not necessarily be equal to the MPI.

### Meta-data
Number of observations: 9,195,539                          
Number of variables: 3                          

    --------------------------------------------------------------------
                  storage   display    value
    variable name   type    format     label      variable label
    --------------------------------------------------------------------
    studyid         long    %8.0g                 STUDYID
    days_dx_index   float   %9.0g                 DAYS_DX_INDEX
    dx_code         str8    %9s                   DX_CODE
    --------------------------------------------------------------------


## Clinical variables table
### Meta-data
