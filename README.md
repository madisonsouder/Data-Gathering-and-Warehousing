# Data Gathering and Warehousing
## Source
The data was published by the Centers for Disease Control and Prevention (CDC). It was collected by the Division of Population Health and the National Center for Chronic Disease Prevention and Health Promotion. Collect of the data started in 2015 and ended in 2022. The data was accessed and downloaded as a .csv file on Feburary 6th 2025.

Centers for Disease Control and Prevention. (2023). *U.S. Chronic Disease Indicators* [Data Set]. Centers for Disease Control and Prevention.\
https://data.cdc.gov/d/hksd-2xuw
#### Collection
The data was collected by the Division of Population Health through a number of surveys and provided by various health foundations and organizations.
- American Community Survey
- Arthritis National Research Foundation
- Behavioral Risk Factor Surveillance System
- Centers for Medicare & Medicaid Services - Part a Claims Data
- Food Security Supplement Current Population Survey
- National Immunization Survey
- National Survey of Children's Health
- National Vital Statistics System
- Pregnancy Risk Assessment Monitoring System
- US Cancer DTV
- United States Renal Data System
- Women, Infants, and Children (WIC) Participant and Program Characteristics
- Youth Risk Behavior Surveillance
#### Extraction
The data was downloaded from the Centers for Disease Control and Prevention website as a .csv file. This was a one time extraction with no updates.
## Data Cleaning
#### Progam
The data wsa cleaned and examined using python through jupyter notebook.
#### Cleaning
1. All column names were changed to lowercase and underscores were used in place of spaces between words.
2. Ten columns were removed because they only contained NaN values. These included:
   - Response
   - stratification Category 2
   - Stratification 2
   - Stratification Category 3
   - Stratification 3
   - Response ID
   - Stratification Category ID 2
   - Stratification ID 2
   - Stratification Category ID 3
   - Stratification ID 3
3. Rows that had NaN values for the data entry column were removed. This was 100,019 entries out of an intial 309,215 entries.
4. Two typos were found in the Question column. Both typos were: "among adults 18â€“64". This was changed to "among adults 18-64".
5. The stratification cateogory ID 1 column was removed because it was a redundancy of the stratification category column.
6. The data value alt column was removed becuase it was identical to the data value column.\
All data cleaning and reasoning was logged as comments in python.
## Data Nuances
#### Numerical Data
There are two columns in the data set that contain information about the numerical data units and their type.\
Data Value Unit and Data Value Type:
- Adjusted rate by age, sex, race and ethnicity - Cases per 1,000,00
- Age-adjusted Mean - Number and depends on the question for that entry
- Age-adjusted Prevalence - Percent
- Age-adjusted Rate - Cases per 1,000 or cases per 100,000 or per 100,000
- Crude 75th percentile - Number
- Crude Mean - Number
- Crude Median - Number
- Crude Prevalence - Percent
- Crude Rate - Cases oer 1,000 or cases per 100,000
- Number - Number
- Per capita alcohol consumption gallons - Gallons
- Proportion - Percent
#### Formulas
No additonal columns were created and thus no formulas were used.
#### Column Names
- year_start - The year the data collect was started
- year_end - The year the data collect ended
- location_abbr - The abbrievation for the state, region, district or territorty the data was collected from
- location_desc - The full names of the state, region, district or territorty the data was collected from
- data_source - How the data was collected or where it was obtained from
- topic - The health concern the data collected falls under
- question - The specific research question that was asked when collecting the data
- data_value_unit - The unit of the data
- data_value_type - The type of data recorded
- data_value - The value recorded
- data_value_footnote_symbol - Indication that a footnote is present for this data entry
- data_value_footnote - Additional information about the collect of the data
- low_confidence_limit - The minimun value of the confidence interval 
- high_confidence_limit - The maximum value of the confidence interval
- stratification_category_1 - The board category in which the population was divided (Age, gender, race)
- stratification_1 - The specific category (male or female)
- geo_location - The location coordinates
- location_id - The number assigned to each unique location
- topic_id - An abbreviation assigned to each unique topic
- question_id - The topic abbrevation and the question number
- data_value_type_id - An abbreviation assigned to each unique data value type
- stratification_id_1 - An abbreviation assigned to each unique statification
## Regulations
This dataset is for public use and does not include sensitive and private information. It is under an  Open Data Commons Open Database License.
