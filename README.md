# little picture - ghg inversions
## Background on this little picture
_satellite observations can improve national greenhouse gas reporting Nations around the world are making efforts to reduce emissions of climate warming gases._

To track action, countries report their greenhouse gas emissions to the UNFCCC. Researchers have developed a framework using Earth observation satellite data to independently check, and help improve, national inventory greenhouse gas reports that show progress towards Paris Agreement objectives. This bar chart contrasts reported versus space-derived CO 2 in Brazil.

https://climate.esa.int/en/little-pictures-gallery/ghg-inversions/

## Data Sources
The CLIP uses the following datasets:
- Paper source: https://essd.copernicus.org/articles/14/1639/2022/ 
- Data Source: https://zenodo.org/record/5089799#.ZGTewexByAl (data compressed into a single zip file)

## Data Preparation
- The notebook imports necessary libraries such as os and zipfile for handling file operations.
- It defines file paths for the zip file containing the data and the extraction path.
- The notebook extracts climate inversion data from the provided zip file.
- It loads this data into dataframes for further processing, as indicated by calling the head() function on inventory_df and co2_inversion_df.
- It defines a list of specific countries (e.g., CHN, USA, EUR) for subsequent analysis.
- It copies relevant columns from the land_flux_df dataframe into a new dataframe df_viz and computes a 'difference' column as the difference between inversion_median and national_inventory.
- It converts the 'party' column in the df_viz dataframe to string data type.

## Creating Visualisations
- The notebook uses the Altair library to create visualizations of the processed data.
- It creates an area chart using the mark_area method on the df_viz dataframe, with the year as the X-axis.
- It also creates a bar chart using the mark_bar method.
- It reproduces charts from a referenced paper and creates an abstraction that shows only the difference between reported and measured data.

## CREDITS & LICENSE
- Idea by: [Ubilabs](https://www.ubilabs.com/)
- Processing Scripts by: [Ubilabs](https://www.ubilabs.com/)
- Visualisation by: [Ubilabs](https://www.ubilabs.com/)

The code in this repository is published under [CC BY-SA 4.0 license](https://creativecommons.org/licenses/by-sa/4.0/)
