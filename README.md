# Better Data Pipelines, For Better Water Pipelines

Every year, the State of California gathers data about water usage and production from all of its public water systems via *Electronics Annual Reports* (EARs). For instance, consider Dataset #8 in the Recommended Challenge Datasets: this dataset lists information taken from the EAR for each public water system (PWS) for each month of the year, including water production/delivery, water quality, and rates. In principle, this dataset is a treasure-trove of knowledge for government employees seeking to study, optimize, and understand water distribution in California.

Despite the effort expended to gather this data, it rarely gets used in analyses. Even though the dataset contains valuable insight about water use, its **clunky format** makes even simple analysis questions (e.g. how does water production change in a particular PWS over time?) difficult to ask. Furthermore, the **low data quality** (e.g. missing fields) provides other obstacles. 

This repository includes Jupyter Python notebooks to address both the format and quality problems in the EAR dataset. We intend the users of this repository to be state and local government employees (or perhaps simply interested citizens) who wish to understand how, when, and where water is used in California. 

## Data Transformations

When addressing the problem of the EAR data format, its tempting to take the following simple approach: design the ideal data format, and then transform all of the original EAR raw data permanently into this new and shiny layout. One must recognize however, that the "ideal" data format depends on the questions being asked of the data. In other words, what is important to the user? Water delivery? Water production? What types of water systems (residential, industrial, agricultural, etc.) use the most water, and when?

So, we instead took the approach of writing different data transformation scripts for different output formats. Each script takes as input the raw data, and outputs a combination of rearranged data and calculations into a new format. 

LIST OF DIFFERENT FORMATS/CORRESPONDING OUTPUTS

## Data Hygiene

In addition to transforming the data into a more useful format, we also provide 

PUT SOME STUFF HERE
