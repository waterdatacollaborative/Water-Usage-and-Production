# Better Data Quality for Better Water Equity

Every year, the State of California gathers data about water usage and production from all of its public water systems via *Electronics Annual Reports* (EARs). For instance, consider Dataset #8 in the Recommended Challenge Datasets: this dataset lists information taken from the EAR for each public water system (PWS) for each month of the year, including water production/delivery, water quality, and rates. In principle, this dataset is a treasure-trove of knowledge for government employees seeking to study, optimize, and understand water distribution in California.

Despite the effort expended to gather this data, it rarely gets used in analyses. Even though the dataset contains valuable insight about water use, its **clunky format** makes even simple analysis questions (e.g. how does water production change in a particular PWS over time?) difficult to ask. Furthermore, the **low data quality** (e.g. missing fields) provides other obstacles. 

This repository includes Jupyter Python notebooks to address both the format and quality problems in the EAR dataset. We intend the users of this repository to be state and local government employees (or perhaps simply interested citizens) who wish to understand how, when, and where water is used in California. 

## Data Transformations

When addressing the problem of the EAR data format, its tempting to take the following simple approach: design the ideal data format, and then transform all of the original EAR raw data permanently into this new and shiny layout. One must recognize however, that the "ideal" data format depends on the questions being asked of the data. In other words, what is important to the user? Water delivery? Water production? What types of water systems (residential, industrial, agricultural, etc.) use the most water, and when?

So, we instead took the approach of writing different data transformation scripts for different output formats. Each script takes as input the raw data, and outputs a combination of rearranged data and calculations into a new format. The two output data formats we chose (along with corresponding dataset number from the Recommended Challenge Datasets) were:

### 1) Water Produced (Dataset #5)

### 2) Water Delivered (Dataset #6)

## Data Hygiene

In addition to transforming the data into a more useful format, there is an included script which converts the original data set into a single dataframe and creates a dictionary that tags each column with keys that identify string and/or number quality. These tags include capitalization errors, consistency in nonalphanumeric notation, misspellings, variance in numerical digits, etc. Suggestion is that these tags be used to model a data cleaning algorithm to take steps toward improving dataset quailty. Another option is to possibly make a histogram of tags (a qualitative index will need to be made as some tags return arrays and others numbers) to visualize data quality. A qualitative view of the tags would assist in identifying high error columns/fields, a potentially useful metric for updating the way in the which the EARs are submitted.  
