### **Uni**que **N**ational **D**rug **C**ode  crosswalk file

This is a Stata format file that contains national drug codes (NDCs) and the World Health Organization Anatomical Therapeutic Chemical Classification (WHO ATC) system classes.

## Meta-data    

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
