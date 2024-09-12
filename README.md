# VA Home Loan Volume by County: Longitudinal Dataset

## Overview
This repository contains a longitudinal dataset detailing veteran home loan volumes by county in the United States, derived from the VA Home Loan Volume reports. The dataset consolidates annual data from multiple years (2015–2022) into a machine-readable format, allowing for comprehensive analysis of veteran loan activity across different regions and over time.

The data source is the VA Home Loan Volume by County reports, available at [this website](https://www.benefits.va.gov/HOMELOANS/lender_county_volume.asp). These reports document the total number of veteran home loans, including purchases, Interest Rate Reduction Refinance Loans (IRRRLs), and cash-out refinances, by county and county equivalents across the U.S. 

## Data Cleaning Process
The original data contained inconsistencies, including errors in county names and the assignment of counties to incorrect states. These errors were cleaned and corrected to ensure the accuracy of the dataset. In addition, we used MABLE GeoCorr at the Missouri Census Data Center to add metropolitan, micropolitan, and nonmetropolitan status to each county (based on the 2010 delineations). 

## Dataset Description
This dataset includes several key variables, making it useful for analyzing veteran home loan purchases in relation to regional population sizes and urbanization levels. The dataset contains the following columns:
- **fips**: Numeric representation of the FIPS (Federal Information Processing Standards) code, which uniquely identifies U.S. counties.
- **fips_char**: Character version of the FIPS code.
- **cbsa13**: Core-Based Statistical Area (CBSA) code identifying metropolitan or micropolitan areas.
- **cbsatype13**: The type of CBSA, which is either "Metro" (metropolitan area) or "Nonmetro" (non-metropolitan area).
- **cbsaname**: The name of the CBSA, including the area type (Metro/Nonmetro).
- **pop10**: Population as of the 2010 U.S. Census.
- **purchase2015** to **purchase2022**: Number of veteran home loan purchases for each year from 2015 to 2022.
- **rolling_average**: A rolling average of loan purchases across the observed years, providing a smoothed trend of home loan activity.
- **proportion1000**: The proportion of loan purchases per 1,000 residents, allowing for comparisons of loan activity across regions with differing population sizes.

## Usage
The dataset can be used for a variety of research and analytical purposes, including:
- Examining trends in veteran home loan activity over time.
- Comparing loan volumes between metropolitan and non-metropolitan areas.
- Analyzing regional disparities in veteran access to home loans.
- Investigating the relationship between population size and loan activity.

## Data Sources
The dataset was compiled from the following annual VA Home Loan Volume by County reports:
- [FY 2015 Report (PDF)](https://www.benefits.va.gov/homeloans/documents/docs/fy2015_all_counties.pdf)
- [FY 2016 Report (PDF)](https://www.benefits.va.gov/homeloans/documents/docs/fy2016_all_counties.pdf)
- [FY 2017 Report (PDF)](https://www.benefits.va.gov/homeloans/documents/docs/fy2017_all_counties.pdf)
- [FY 2018 Report (PDF)](https://www.benefits.va.gov/homeloans/documents/docs/fy2018_all_counties.pdf)
- [FY 2019 Report (PDF)](https://www.benefits.va.gov/HOMELOANS/documents/docs/fy2019_all_counties.pdf)
- [FY 2020 Report (PDF)](https://www.benefits.va.gov/HOMELOANS/documents/docs/fy2020_all_counties.pdf)
- [FY 2021 Report (XLSX)](https://www.benefits.va.gov/HOMELOANS/documents/docs/fy2021_all_counties.xlsx)
- [FY 2022 Report (XLSX)](https://www.benefits.va.gov/HOMELOANS/documents/docs/fy2022_all_counties.xlsx)
- [FY 2023 Report (XLSX)](https://www.benefits.va.gov/HOMELOANS/documents/lender-statistics/fy23-counties-total.xlsx)

## Citation
If you use this dataset in your research, please cite as follows:
> Michael Lotspeich-Yadao, VA Home Loan Volume by County: Longitudinal Dataset, [https://github.com/mlots2-illinois/VA_Lending].

Additionally, you may acknowledge the original data source:
> U.S. Department of Veterans Affairs, VA Home Loan Volume by County Reports. Available at [https://www.benefits.va.gov/HOMELOANS/lender_county_volume.asp](https://www.benefits.va.gov/HOMELOANS/lender_county_volume.asp).

## License
This dataset is provided under the CC0-1.0 license license. Please refer to the LICENSE file for more details.
