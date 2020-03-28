# AustinPopulationData

The purpose of this repository is to analyze the population and economic growth of the city of Austin, TX between 2010-2020 and how the trends fit in the broader context of the U.S.
It seeks to address the following questions:

- What demographic and geographic changes have taken place?
- How has the population grown?
- How has growth impacted wealth and income equity?
- What industries have grown the most over time? 

The repository is divided into the following sections:
- **01_API_and_Data_Collection**: This folder contains a Jupyter Notebook that pulls data from the US Census website (Census.gov) via API. The notebook pulls data regarding population, poverty, housing, and education by zipcode for all zipcodes in the United States for a given year. Due to data size, four separate API calls are performed, one for each data topic. It then filters out the data for Austin zipcodes and exports that data to CSV format in the Appendix_A_Resources. To gather data for a different year, simply set the year variable in the first cell to the year desired; the program will run for years 2011-2018. An API key to call data from Census.gov is included in the repository.
- **02_Data_Cleaning**: This folder contains a Jupyter Notebook that merges the Census data pulled in the 01_API_and_Data_Collection folder. It will join data by topic (i.e. population, poverty, housing, and education) into a dataframe for all years collected, and then merge all 4 topics into a single dataframe. The notebook will then export all dataframes into CSV format, saved in the Appendix_A_Resources folder, to be used by code in the 03_Visualization_Code folder.
- **03_Visualization_Code**: This folder contains several Jupyter Notebooks that generate data plots, graphs, and heatmaps based on demographics and industry data located in the Appendix_A_Resources folder. A subfolder called Additional_Visualization_Code contains several Jupyter Notebooks used to write functions, which are called in the Income_Demographic_Trends.ipynb to generate plots. If the code is run again, it will export plots in PNG format to the Appendix_B_Output_Data folder. Note: A Google Maps API key is required to generate the heatmaps.
- **04_Presentation**: This folder contains the slide presentation showing findings on Austin growth data.
- **Appendix_A_Resources**: This folder contains the data analyzed in CSV format, along with a list of resources cited.
- **Appendix_B_Output_Data**: This folder contains the images and plots generated in the notebooks in the 03_Visualization_Code folder.
