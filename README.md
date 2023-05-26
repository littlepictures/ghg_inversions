# CLIP - GHG Inversion vs National Inventories

## Background on this CLIP
[SHORT DESCRIPTION ON WHAT THE CLIP SHOWS AND WHY IT MATTERS IN TERMS OF CLIMATE DATAVIZ (500-600 CHARACTERS)]

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam at vestibulum nulla, ac tincidunt sem. Morbi in nisl at nisl feugiat faucibus sed eu neque. In fringilla, odio eu porttitor condimentum, tortor leo congue justo, id venenatis metus lectus sed libero. Mauris id arcu eros. Sed orci mauris, tincidunt nec ex non, eleifend pellentesque dolor. Mauris tellus ligula, tincidunt accumsan sapien accumsan, pellentesque rhoncus ex. Phasellus sollicitudin dolor eget porttitor gravida. Integer malesuada vehicula ante, ac interdum felis congue nec. Mauris in sagittis felis. 


## Data Sources
[LIST OF ALL DATASOURCES AND SPECIFIC DATASETS USED IN THE CREATION OF THE CLIP]

The CLIP uses the following datasets:
- [ESA Open Data website](https://climate.esa.int/de/odp/#/dashboard)

## Data Preparation
The notebook imports necessary libraries such as os and zipfile for handling file operations.
It defines file paths for the zip file containing the data and the extraction path.
Data Preparation

The notebook extracts climate inversion data from the provided zip file.
It loads this data into dataframes for further processing, as indicated by calling the head() function on inventory_df and co2_inversion_df.
It defines a list of specific countries (e.g., CHN, USA, EUR) for subsequent analysis.
It copies relevant columns from the land_flux_df dataframe into a new dataframe df_viz and computes a 'difference' column as the difference between inversion_median and national_inventory.
It converts the 'party' column in the df_viz dataframe to string data type.

## Creating Visualizations
The notebook uses the Altair library to create visualizations of the processed data.
It creates an area chart using the mark_area method on the df_viz dataframe, with the year as the X-axis.
It also creates a bar chart using the mark_bar method.
It reproduces charts from a referenced paper and creates an abstraction that shows only the difference between reported and measured data.

## CREDITS & LICENSE
- Idea by: [Ubilabs](https://www.ubilabs.com/)
- Processing Scripts by: [Ubilabs](https://www.ubilabs.com/)
- Visualization by: [Ubilabs](https://www.ubilabs.com/)

The code in this repository is published under [CC BY-SA 4.0 license](https://creativecommons.org/licenses/by-sa/4.0/)
