# Python API Challenge
---
### PURPOSE

The purpose of this repository is to store weather analyses for the world using data from a custom list of  approximately 1000 cities extracted from openweathermap.org and using visualizations from Google Maps
#

### ANALYTICAL TOOL CHOICE RATIONALE

The tools chosen for this analysis include Python and several associsted libraries including Pnadas, MatPlotLib, SciPy.  Additionally Jupyter Notebooks was userd as repository for the analysis.  

They were chosen for the following reasons:
1.  Python provides a powerful and flexible code platform for developing data analyses. Additionally, the associtated libraries provide broad predefined functionality to facilitate all of the activities from data acquisition and formatiing, to calculations, and visualization.  
2.  Jupyter Notebook provides unique functionality for 2 important elements:
    (a)  Code and test discrete portions of code in real time in one location
    (b)  House all code as well as data and visual ouputs in one package. 
#

### APPROACH

#### WeatherPy
-Created a custom data set of over 1000 cities world wide
-Put the cities into a list and ran looped calls to openweathermap api to ensure that the cities exisyted in their database.  The handful that did not were removed resulting in the final list of cities of ~ 1000 cities that were used for the analysis. Note: The code for creation of the final list of cities and their associated data is not in scope for the required analysis documentation and, thus, is not included. The Notebook begins with and only includes the required analyses.
-Saved the resulting data set to a csv file
-Imported the csv file into pandas as a dataframe for the analysis
-Performed a series of api calls to openweather to extract the required waether data points for each of the cities in the list to create the final data set to be used for all of the analyses. Interestingly, though I could not find documentation during a cursory on the open weather site of the time volume limits of api calls allowed , the number was exceeded by this dataset and the api key was locked to further calls for 24 hours.  Thus, the analyses required multiple days to complete.    
-Created the required scatter plots of latitude vs temperature, humidity, cloudiness, and wind speed and ouput images of the charts to the notebook directory 
-Performed linear regression analyses to determine the correlation of the aforementioned weather factors by hemisphere and plotted the results on scatter plots and ouput images of the charts to the notebook directory
-Recorded observations from the analyses in the notebook.  

#### VacationPy
-Imported the final csv data from WeatherPy analysis into new notebook
-Created a heatmap with in Google Maps displaying the relative humidity in all of the cities from the world city data set
-Segregated the city weather data by temperatures between 69 and 85 fahrenheit, very low cloudiness and wind speeds, and moderate humidity and saved the results of the segregated data to a new dataframe of these "ideal vacation cities" 
-Made calls to google places api to find hotels in those cities and created a new dataframe containing the city weather data for the vacation cities as well as the newly acquired hotel names in those cities
-Plotted markers on the orginal humidity heatmap with pop-up labels that tell the name of the hotel, city , and country.   
#

### INCLUDED ITEMS
The repository contains two folders: WeatherPy and VacationPy that contain each contain the respctive files for those analyses.

WeatherPy contains:
1. weatherpy.ipynb - the Jupyter Notebook file containing all of the code, analysis and charts for this portion of the project
2. config.py - a dummy py file that would contain the API key for use in the notebook code but is empty in this respository - as the file is called by the code in the notebook an API key would hhave to be included and saved in the file to run the code
3. NOTE_config File Empty.txt - an empty text file included with the title as a reminder that the config.py file in the folder is empty  
4. 3 Observable Trends from the Extracted Weather Data.docx - a Word document containing the required 3 obervations from the WeatherPy analysis
5. weatherpy.html - an html copy of the jupyter notebook file that provides the ability to see the code and results without having to run Jupyter Notebooks and having the additional benefit of having code formatted in color.   
6. Cities by Lat Long Final CSV.csv - the custom file containing data that was specifically created for the study of nearly 1000 cities worldwide to provide a good breadth and depth of geography to ensure quality results from the study.  
7. worldcity_data.csv - the data file produced as a output product of the python program containing all of the original city data plus the weather data aquired for those locations.  
8. Numerous png files produced as outputs of the python code that are images of the charts produced by the analysis and providing visualization of those analyses. 

VacationPy contains:
1. vacationpy.ipynb - the Jupyter Notebook file containing all of the code, analysis, and charts for this portion of the project
2. mapconfig.py - a dummy py file that would contain the API key for use in the notebook code but is empty in this respository - as the file is called by the code in the notebook an API key would hhave to be included and saved in the file to run the code
3. NOTE_mapconfig File Empty.txt - an empty text file included with the title as a reminder that the config.py file in the folder is empty 
4. weatherpy.html - an html copy of the jupyter notebook file that provides the ability to see the code and results without having to run Jupyter Notebooks and having the additional benefit of having code formatted in color. 
5. World City Humdity HeatMap Capture.JPG and World City Humdity HeatMap Capture LRG.JPG - screen captues of the Goggle Maps maps created by the program to display the relative humidity of all of the world cities included in the study.  Both of the files contain captures of the same map but the LRG file is zoomed in to show a different amount of detail whereas the other files gives a much broader overall view.  
6.  Vacation Hotel Location LRG.JPG - a screen capture of markers that were layered onto the world humidity heatmap containing the locations of the hotels for the cities identified by aforementioned criteria to be possible vacation spots. The image shows all of the information pop ups that appear as a result of clicking on the respective markers.  The pop ups contain the name of the hotel, as well as the city and country where they are located.  
#
