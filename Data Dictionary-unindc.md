## *Uni*que *N*ational *D*rug *C*ode  crosswalk file

This is a Stata format file that contains national drug codes (NDCs) and the World Health Organization Anatomical Therapeutic Chemical Classification (WHO ATC) system classes.

### Meta-data    

    -----------------------------------------------------------------------------------------------------------------
                  storage   display    value
    variable name   type    format     label      variable label
    -----------------------------------------------------------------------------------------------------------------
    ndc             str11   %11s                  NDC
    drug            str256  %256s                 SOURCE_CODE_DESCRIPTION
    rxncui          long    %12.0g                RXNORM_INGREDIENT
    concept_name    str102  %102s                 CONCEPT_NAME
    cscode          str7    %9s                   CLASS_CONCEPT_CODE
    drug_class      str50   %50s                  DRUG_CLASS
    sgthr           str50   %50s                  
    sgphr           str50   %50s                  
    sgchem          str50   %50s                  
    -----------------------------------------------------------------------------------------------------------------

### Variable Descriptions

| Variable     | Description                                                         | Example values                                                        | Notes                                                                                                                                      |   |
|--------------|---------------------------------------------------------------------|-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|---|
| ndc          | 11-digit National Drug Code identifier for prescription medications | 00536381301, 33261008810                                              | This variable should always be maintained as a string/character variable                                                                   |   |
| drug         | Drug name including dosage and/or strength                          | Bumetanide 2 Mg Oral Tablet,  Erythromycin Stearate 250 Mg Oral Tablet |                                                                                                                                            |   |
| rxncui       | Identifier for corresponding concept in the RxNorm database         | 161, 5640                                                             |                                                                                                                                            |   |
| concept_name | Generic Drug name. Does not include dosage or strength              | Cefadroxil, Fentanyl                                                  |                                                                                                                                            |   |
| cscode       | ATC code of the drug                                                | B03BA01, D04AA32                                                      |                                                                                                                                            |   |
| drug_class   | Broad drug class                                                    | Cimetidine, Glipizide                                                 | This is a very broad drug classification and for most intents shohuld be avoided. This is very closely related to `concept_name` variable. |   |
| sgthr        | **Th**e**r**apeutic **s**ub**g**roup                                | Antibacterials For Systemic Use, Antiseptics And Disinfectants        | See http://apps.who.int/medicinedocs/en/d/Js4876e/6.2.html#Js4876e.6.2 for more details                                                    |   |
| sgphr        | **Ph**a**r**macological **s**ub**g**roup                            | Antiepileptics, Anxiolytics                                           | See http://apps.who.int/medicinedocs/en/d/Js4876e/6.2.html#Js4876e.6.2 for more details                                                    |   |
| sgchem       | **Chem**ical **s**ub**g**roup                                       | Azaspirodecanedione Derivatives, Enzyme Preparations                  | See http://apps.who.int/medicinedocs/en/d/Js4876e/6.2.html#Js4876e.6.2 for more details                                                    |   |
