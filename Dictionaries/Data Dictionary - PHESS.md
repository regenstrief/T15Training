# PHESS Data Dictionary

This deidentified data was derived from the Indiana State Department of Health's (ISDH) Public Health Emergency Surveillance (PHESS) system. Emergency
departments across Indiana send raw HL7 data to ISDH to be used for early detection of public health emergencies. The variables in this data were derived by parsing various HL7 segments into a delimited text file.

The following links may provide more information:

1. [PHESS](https://www.in.gov/isdh/18085.htm)
2. [List of HL7 fields shared by PHESS](https://eportal.isdh.in.gov/MeaningfulUse/Documents/ISDH_PHESS_Messaging_Feedback_Template_01-12-2018.pdf)
3. [Wikipedia entry for HL7](https://en.wikipedia.org/wiki/Health_Level_7)

 
## Meta-Data  
Number of observations: 100,000  
Number of variables: 45  

| **Variable**            | **Variable description**                                                                   |
|-----------------------|-----------------------------------------------------------------------------------|
| INTERNAL_PAT_ID       | Unique patient identifier                                                         |
| SENDING_APP           | Sending application                                                               |
| SENDING_FAC           | Sending facility                                                                  |
| AGE                   | Years between August 2018 and patient date of birth                               |
| GENDER                | Patient gender(Male/Female)                                                    |
| RACE                  | Race as mapped                                                      |
| ETHNICITY             | Ethnicity                                                 |
| ADMIT_REASON          | Admit reason                                                                      |
| ADMIT_REASON_CLEAN    | Cleaned admit reason                                                              |
| CHIEF_COMPLAINT       | Chief complaint                                                                   |
| DISCHARGE_DISPOSITION | Type of discharge (Routine, Transfer, Admit to inpatient etc.)                    |
| DX_TYPE               | Type of diagnosis (Admit, Discharge, etc.)                                        |
| DX_CODE               | Diagnosis code                                                                    |
| DX_TEXT               | Diagnosis code description text                                                   |
| DX_CODE_SYSTEM        | Diagnosis code system (ICD9, ICD10, etc.)                                         |
| ZIP_GROUP             | Three digit zip code group                                                        |
| ZIP_TOTAL_POPULATION  | Total population of three digit zip code group                                    |
| FLAG_ABDOMINAL        | Flag for one of the top 20 admit reasons                                          |
| FLAG_RASH             | Flag for one of the top 20 admit reasons                                          |
| FLAG_SEPSIS           | Flag for one of the top 20 admit reasons                                          |
| FLAG_CHEST            | Flag for one of the top 20 admit reasons                                          |
| FLAG_COUGH            | Flag for one of the top 20 admit reasons                                          |
| FLAG_SOB              | Flag for one of the top 20 admit reasons                                          |
| FLAG_DIZZINESS        | Flag for one of the top 20 admit reasons                                          |
| FLAG_FEVER            | Flag for one of the top 20 admit reasons                                          |
| FLAG_VOMITING         | Flag for one of the top 20 admit reasons                                          |
| FLAG_WOUND            | Flag for one of the top 20 admit reasons                                          |
| FLAG_BACK_PAIN        | Flag for one of the top 20 admit reasons                                          |
| FLAG_ALLERGY          | Flag for one of the top 20 admit reasons                                          |
| FLAG_CONGESTION       | Flag for one of the top 20 admit reasons                                          |
| FLAG_VEHICLE          | Flag for one of the top 20 admit reasons                                          |
| FLAG_HEADACHE         | Flag for one of the top 20 admit reasons                                          |
| FLAG_PAIN             | Flag for one of the top 20 admit reasons                                          |
| FLAG_PREGNANCY        | Flag for one of the top 20 admit reasons                                          |
| FLAG_STABBING         | Flag for one of the top 20 admit reasons                                          |
| FLAG_STI              | Flag for one of the top 20 admit reasons                                          |
| FLAG_SORE_THROAT      | Flag for one of the top 20 admit reasons                                          |
| FLAG_SWELLING         | Flag for one of the top 20 admit reasons                                          |
| FLAG_SINUS            | Flag for one of the top 20 admit reasons                                          |
| FLAG_FALL             | Flag for one of the top 20 admit reasons                                          |
| WEEKDAY               | Day of week (Monday - Sunday)                                                     |
| AGE_GROUP             | Age groups bins, will indicate if a patient is over 90                            |
| TRANSACTION_DAY       | Negative numbers indicates days before a gap, positive number indicate days after |
| TRANSACTION_TIME      | Transaction time                                                                  |
| ZIP_IS_INDIANA        | Flag indicating if 3 digit zip group is in Indiana                                |
