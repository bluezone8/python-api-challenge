tools
Python and associated libraries Pandas Matplotlib SciPy 
Jupyter notebook
Python provides a powerful and flexible code platform for developing data analyses. Additionally, the associtated libraries provide braod predefined functionality to faciliatte all of the activities from data acquaition and formatiing, to calculations, and visualization.  jupyetr notebooks provides unique functionality for 2 important elements: 1.code and testdiscrete portions of code in real time in one lkocation and 2. house all code as well as data and visual ouputs in one package.  

Approach 
weather py
-created a custom data set of over 1000 cities world wide
-put the cities into a list and ran looped calls to openweather api to ensure that the cities exisyted in their database.  The handful that did not were removed resulting in the final list of cities of ~ 1000 cities that were used for the analysis. Note: The code for creation of the final list of cities and their associated data is not in scope for the required analysis documentation and, thus, is not included. The Notebook begins with and only includes the required analyses.
-saved the resulting data set to a csv file
-Imported the csv file into pandas as a dataframe for the analysis
-Perfomred a series of api calls to openweather to extract the required waether data points for each of the cities in the list to create the final data set to be used for all of the analyses. Interestingly, though I could not find documentation during a cursory on the open weather site of the time volume limits of api calls allowed , the number was exceeded by this dataset and the api key was locked to further calls for 24 hours.  Thus, the analyses required multiple days to complete.    
-Created the required scatter plots of latitude vs temperature, humidity, cloudiness, and wind speed and ouput images of the charts to the notebook directory 
-performed linear regression analyses to determine the correlation of the aforementioned weather factors by hemisphere and plotted the results on scatter plots and ouput images of the charts to the notebook directory
-Recorded observations from the analyses in the notebook.  

vacation py
-imported the final csv data from weatherpy analyssis into new notebook
-created a heatmap with a call to Google Maps API map indicating humidity in all of the cities from the world city data set humidity
-segregated the city weather data by temperatures between 69 and 85 fahrenheit, very low cloudiness and wind speeds, and moderate humidity.  
-saved the results of the segregated data to a new dataframe of these "ideal vacation cities" 
-made calls to google places api to find hotels in those cities and -created a new dataframe containing the city wetaher data for the vacation cities and including the hotel names
-plotted markers on the orginal humidity heatmap with popup labels that tell the name of the hotel, city , and country.  

included items
1. Code 
  