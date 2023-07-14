# ndc-fda-drug
This application is built in Jupyter Notebook, the file `novo_nordisk_qaiser.ipynb` generates different CSV files as output for the following requirements:

    1) How many unique persons have been prescribed a medication containing the active ingredient “insulin”?

    2) How many of the NDC packages can't be found in FDA database?

    3) From the NDC packages found in the FDA database, which ten active ingredients are prescribed to most persons and how many persons have been prescribed each of them?

    4) Which ten drugs that are not found in FDA's database are prescribed to highest number of persons, and how many persons have been prescribed each of them?


# Data
   - CSV file `DE1_0_2008_to_2010_Prescription_Drug_Events_Sample_10.csv` can be downloaded from [CMS](https://www.cms.gov/research-statistics-data-and-systems/downloadable-public-use-files/synpufs/desample10)

   - JSON data `drug-ndc-0001-of-0001.json` can be downloaded from [FDA](https://open.fda.gov/apis/drug/ndc/download/) site. 

## Datasets linking
The two datasets can be linked via the NDCs, after some transformations. First, the 11-digit NDC code (PROD_SRVC_ID) from csv file must be reverted back to a 10-digit code. Sequentially, the labeler and the product code part from the 10-digit NDC will form the drug product NDC (product_ndc) that can be searched with JSON-file. 
