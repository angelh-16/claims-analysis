# HHA507 Assignment 5: Healthcare Claims Data Analysis
## Overview
This assignment simulates the analysis that healthcare data analysts, medical billing specialists, and health informaticians perform on a daily basis. Acting as a data analyst at Stony Brook University Hospital, the goal is to analyze billing patterns, identify the most common diagnoses and procedures, and understand payer mix to support operational decision-making based on the sample of prospective claims data from May 2024, provided by the compliance and revenue cycle teams.

This assignment required working with three interconnected claims files to answer questions about provider billing patterns, common diagnoses, procedures, and payer relationships, focusing on relational data analysis using Python and pandas.


## Data source information
### 1. HEADER File (`STONYBRK_20240531_HEADER.csv`)
Contains one row per claim with high-level information:
- **ProspectiveClaimId**: Unique claim identifier
- **Provider NPIs**: Billing, Attending, Rendering, Referring, Operating providers
- **ServiceFromDate/ServiceToDate**: Service dates
- **PrimaryPayerName/PrimaryPayerCode**: Primary insurance payer
- **PlaceOfService**: Where services were rendered
- **WorkQueName**: Audit/review queue assignment

### 2. LINE File (`STONYBRK_20240531_LINE.csv`)
Contains one row per service line (procedures/services):
- **ProspectiveClaimId**: Links to HEADER file
- **LinePos**: Line number on the claim
- **HCPCS**: CPT/HCPCS procedure code
- **Modifier1-4**: Procedure modifiers
- **DxMapDelim**: Shows which diagnosis codes justify this procedure
- **Charges**: Dollar amount billed for this line
- **Units**: Quantity of service

### 3. CODE File (`STONYBRK_20240531_CODE.csv`)
Contains diagnosis codes (ICD-10):
- **ProspectiveClaimId**: Links to HEADER file
- **CodePos**: Position/order of diagnosis on claim
- **CodeValue**: ICD-10 diagnosis code
- **CodeQualifier**: Code type (ABF, ABK, etc.)

## Data Location
The data files are located in:
```
Module6_claims/clean/example_2/
    STONYBRK_20240531_HEADER.csv
    STONYBRK_20240531_LINE.csv
    STONYBRK_20240531_CODE.csv
```

## How to run notebook
1. dowload all the csv files in the data folder of this repo
2. click into the folder `notebooks` in this repo 
3. click into `claims_analysis.ipynb`
4. click on Open in Colab at the top
5. in collab, click the files icon on the left side
6. create a folder named data and upload the files you downloaded in to the folder
7. Run the code by clicking Run all or click theplay button next to each section of a code to run it one by one

## Summary of key findings
* 
* 
* 
* 
* 

## Required libraries
**requirements.txt** with necessary Python packages:
   ```
   pandas>=1.3.0
   matplotlib>=3.4.0
   seaborn>=0.11.0
   ```