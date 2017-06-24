# DATA ANALYSIS OF CRIMINAL ACTIVITY IN CHICAGO
![alt text](https://github.com/swarupmishal/mishal_swarup_spring2017/blob/master/final/extra/6A231614-652B-4334-852C-54261F4B13BD.png)

## What exactly the Data is?
This dataset reflects reported incidents of crime (with the exception of murders where data exists for each victim) that occurred in the City of Chicago from 2001 to present, minus the most recent seven days. Data is extracted from the Chicago Police Department's CLEAR (Citizen Law Enforcement Analysis and Reporting) system. In order to protect the privacy of crime victims, addresses are shown at the block level only and specific locations are not identified. The Data is already Processed. The data consists of 22 columns and 6.31 Million rows. Each row is a Reported Crime. The entire description for the dataset can be found out at this link,
https://data.cityofchicago.org/Public-Safety/Crimes-2001-to-present/ijzp-q8t2


## How can one obtain the Data and run the .ipynb files?
The data is huge of 1.4 gb. Takes around 5 minutes to download the data, depending on the internet connectivity. There are 2 links for downloading the data.

Link 1:

https://data.cityofchicago.org/api/views/ijzp-q8t2/rows.csv?accessType=DOWNLOAD

Steps:
- Just Copy and Paste the link mentioned above and it will automatically start download
- Store the downloaded csv file at the folder location final/data/raw_data and then run the .ipynb files

Link 2 (If Link 1 doesn't work):

https://data.cityofchicago.org/Public-Safety/Crimes-2001-to-present/ijzp-q8t2/data

Steps:
- Copy and paste the link mentioned above
- Click Export tab
- Click Download and click then Download As CSV 
- Store the downloaded csv file at the folder location final/data/raw_data and then run the .ipynb files

## How is the Data stored?
The Data is stored as CSV file. The downloaded file should be stored inside the folder raw_data which we can find under data folder. The  downloaded file is read using Python

## Individual Analysis and its Inference
## Analysis 1
### Analyzing Pattern of Crime over the years since 2001
> Input: 
Primary Type, Year

> Steps:
- Read the input file
- Make a dataframe total crimes
- Group it by Primary type and then Sort it
- Plot a graph to display Overall Crimes since 2001
- Make a dataframe to sum Crimes based on Year
- Plot a graph to display the pattern of Crimes over the years

> Output:
###### Count of Crime by Primary Type Classification.csv
[View the csv file here](https://github.com/swarupmishal/mishal_swarup_spring2017/blob/master/final/analysis/ana_1/Count%20of%20Crime%20by%20Primary%20Type%20Classification.csv)
###### Count of Crime by Primary Type Classification
![alt text](https://github.com/swarupmishal/mishal_swarup_spring2017/blob/master/final/analysis/ana_1/Count%20of%20Crime%20by%20Primary%20Type%20Classification.png)
###### Change in Count of Crime by Year.csv
[View the csv file here](https://github.com/swarupmishal/mishal_swarup_spring2017/blob/master/final/analysis/ana_1/Change%20in%20Count%20of%20Crime%20by%20Year.csv)
###### Change in Count of Crime by Year
![alt text](https://github.com/swarupmishal/mishal_swarup_spring2017/blob/master/final/analysis/ana_1/Change%20in%20Count%20of%20Crime%20by%20Year.png)

> Inference:
- We can see that Theft is the most common crime that takes place in Chicago.
- If we observe the second graph, we can analyze that the rate of crime in Chicago is showing decreasing trend over the years since 2001, thus slowly Chicago is becoming a better and safe place to live.
- There is a sudden fall of crime in the year 2017, because of the obvious lack of full year's worth of data.
------------------------------------
## Analysis 2
### Analyzing Crime Activity vs Arrest Activity for the past 5 years
> Input: 
Arrest, Year

> Steps:
- Read the input file
- Limit data for last 5 years
- Make a dataframe total crimes
- Group it by Year and then Sort it
- Make a dataframe total crimes where actually someone was arrested
- Group it by Year and then Sort it
- Plot a graph to display Crime Activity vs Arrest Activity from 2012 to 2017

> Output:
###### Count of Criminal Activity of Last 5 Years.csv
[View the csv file here](https://github.com/swarupmishal/mishal_swarup_spring2017/blob/master/final/analysis/ana_2/Count%20of%20Criminal%20Activity%20in%20last%205%20years.csv)
###### Count of Arrest Activity of Last 5 Years.csv
[View the csv file here](https://github.com/swarupmishal/mishal_swarup_spring2017/blob/master/final/analysis/ana_2/Count%20of%20Arrest%20Activity%20in%20last%205%20years.csv)
###### Crime Activity vs Arrest Activity for Last 5 years
![alt text](https://github.com/swarupmishal/mishal_swarup_spring2017/blob/master/final/analysis/ana_2/Crime%20Activity%20VS%20Arrests%20from%202012%20-%202017.png)

> Inference:
- So from the line plot above, truly there has been a decrease in criminal activity over the last five years which has lead to fewer arrests.
- Also there is a wide gap between arrests and crime activity, of about 250,000 difference in crime activity and arrests, except for the year 2017 for obvious reasons of not having data for entire year.
--------------------------------
## Analysis 3
### Lets try to analyze Car Theft in Chicago in Last 5 years
> Input: 
Area Name, Year

> Steps:
- Read the input file
- Limit data for last 5 years
- Add Area Name as an extra column for better analysis.
- Limit data where Car was stolen
- Plot a graph to display Overall Trend of Car Theft in last 5 years
- Group by the data by Year and Area Name
- Plot a graph to display the Count of Car Theft by Community Area
> Output:
###### Count of Car Theft by Community Area.csv
[View the csv file here](https://github.com/swarupmishal/mishal_swarup_spring2017/blob/master/final/analysis/ana_3/Count%20of%20Car%20Theft%20by%20Community%20Area.csv)
###### Car Theft in Chicago, 2012-2017
![alt text](https://github.com/swarupmishal/mishal_swarup_spring2017/blob/master/final/analysis/ana_3/Car%20Theft%20in%20Chicago%2C%202012-2017.png)
###### Count of Car Theft by Community Area
![alt text](https://github.com/swarupmishal/mishal_swarup_spring2017/blob/master/final/analysis/ana_3/Count%20of%20Car%20Theft%20by%20Community%20Area.png)

> Inference:
- The rate of Car theft was observed maximum in the year 2012.
- The rate of car theft seems to be falling in Chicago, since 2012.
- We can see that out of the 77 Community Areas, Austin is the worst Community Are to park a car, followed by West Town and Humboldt Park.
--------------------------------
## Analysis 4
### Analyzing Monthly Domestic Violence in last 5 years
> Input: 
Domestic, Year

> Steps:
- Read the input file
- Limit data for last 5 years
- Make a dataframe total crimes
- Group it by Domestic, Year and then Sort it
- Plot a graph to display Monthly domestic violence for last 5 years

> Output:
###### Monthly domestic violence
![alt text](https://github.com/swarupmishal/mishal_swarup_spring2017/blob/master/final/analysis/ana_4/Monthly%20domestic%20violence.png)

> Inference:
- We can observe a higher rates of Crime in the mid year of each year.
- The higher rate of crime activity during April-August, might be due to the fact that it's the summer period where people are always outside and more vulnerable to attacks from perps.
--------------------------------
## Analysis 5
### Analyzing Map of Chicago with maximum Crime Occurrences in past 2 Years
> Input: 
Latitude, Longitude, Year

> Steps:
- Read the input file
- Make a dataframe total crimes
- Limit the data for last 2 years
- Plot a graph to display Map of Chicago with maximum Crime Occurrences

> Output:
###### Map of Chicago with maximum Crime Occurrences
![alt text](https://github.com/swarupmishal/mishal_swarup_spring2017/blob/master/final/analysis/ana_5/Chicago%20Crime%20Heat%20Map%20in%20Last%202%20Years.png)


> Inference:
- The Bright spots show more criminal activity and light spots show less criminal activity in past 2 years.
- Brighter the spot, more is it unsafe to stay in that locality.
- If someone is considering moving to Chicago, they should try to live near places with light spots so as to avoid Criminal activity.
--------------------------------
