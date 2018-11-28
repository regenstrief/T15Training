# Type-2 Diabetes Data Dictionary


The Type-2 Diabetes or T2D dataset includes data extracted from the Indiana Network of Patient Care for patients presenting with Diabetes. The dataset consists of 5 tables: 
1. Patients table (patients.csv)
2. Prescription medication table (medication.csv)
3. Encounters table (encounter.csv)
4. Diagnoses and visit types table (diagnosis.csv)
5. Clinical variables (e.g. tests, measurements etc.) table (clinical_vars.csv)

## Patients table  
This is the master patient index of all patients in the registry. All rows are unique and identify a distinct patient with T2D.

### Meta-data
Number of observations: 77,908
Number of variables: 14

    --------------------------------------------------------------------
                   storage   display    value
    variable name   type    format     label      variable label
    --------------------------------------------------------------------
    studyid         long    %12.0g                STUDYID
    index_year      int     %8.0g                 INDEX_YEAR
    index_age       byte    %8.0g                 INDEX_AGE
    gender          str1    %9s                   GENDER
    race            str42   %42s                  RACE
    t2d_status      str13   %13s                  T2D_STATUS
    cardiovascular  str2    %9s                   CARDIOVASCULAR
    nephropathy     str2    %9s                   NEPHROPATHY
    liver           str2    %9s                   LIVER
    enc_12m_bf      int     %8.0g                 ENC_12M_BF
    enc_12m_af      int     %8.0g                 ENC_12M_AF
    enc_yrs_bf      byte    %8.0g                 ENC_YRS_BF
    enc_yrs_af      byte    %8.0g                 ENC_YRS_AF
    biobank         str2    %9s                   BIOBANK
    --------------------------------------------------------------------
