Explore US Bike Share Dataset


Introduction:
In this project, I will make to explore data related to bikeshare systems for three major bikeshare systems in the United States. I will perform data wrangling to unify the format of data from the three systems and write code to compute descriptive statistics. I will also make use of a package that is not part of the standard Python library to help you visualize the data.*


Data Collection and Wrangling. 

Datasets:
NYC-CitiBike-2016.csv:
This dataset is for Newyork bikeshare systems.
describe at https://www.citibikenyc.com/system-data

Chicago-Divvy-2016.csv:
This dataset is for Chicago bikeshare systems.
describe at https://www.divvybikes.com/system-data

Washington-CapitalBikeshare-2016.csv:
This dataset is for Washington bikeshare systems.
describe at https://www.capitalbikeshare.com/system-data

Notice:
If you visit these pages, you will notice that each city has a different way of delivering its data. Chicago updates with new data twice a year, Washington DC is quarterly, and New York City is monthly. However, you do not need to download the data yourself. The data has already been collected for you in the /data/ folder of the project files. While the original data for 2016 is spread among multiple files for each city, the files in the /data/ folder collect all of the trip data for the year into one file per city. Some data wrangling of inconsistencies in timestamp format within each city has already been performed for you. In addition, a random 2% sample of the original data is taken to make the exploration more manageable.**

Libraries:
- csv.
- datetime.
- pprint.
- dateutil.
- operator.
- matplotlib.pyplot.
- numpy.
- subprocess.

The functions I have created:

- print_first_point: This function prints and returns the first row from the csv file.

-convert_Washington_du_to_float: 
Tackes a dictionary as input containing info about a single trip (datum) and then it does a convert the value of trip duration to float for Washington city.

convert_others_city_duration_to_float:
Takes a dictionary as input containing info about a single trip (datum) and then it does convert the value of trip duration to float for other countreis.

duration_in_mins:
Takes a dictionary as input containing info about a single trip (datum) and its origin city (city) and returns the trip duration in units of minutes.

parse_dates_semple:
Takes a dictionary as input containing info about a single trip (datum), transfer the string of date to date

parse_dates:
Takes a dictionary as input containing info about a single trip (datum), for Washington dataset and extact transfare the string of date to date.

time_of_trip:
Takes a dictionary as input containing info about a single trip (datum) and its origin city (city) and returns the month, hour, and day of the week inwhich the trip was made.

change_values:
This function is for changing the value of usertype column in Washington city it is take dictionry and return new column.

type_of_user:
Takes a dictionary as input containing info about a single trip (datum) and its origin city (city) and returns the type of system user that made the trip.

condense_data:
This function takes full data from the specified input file and writes the condensed data to a specified output file.


Exploratory Data Analysis:

number_of_trips:
This function reads in a file with trip data and reports the number of trips made by subscribers, stomers, and total overall.

avg_duration:
This function to find the average of duration for a spicific city.



Visualizations:

create_list:
This function is for extract the duration of trip column and save data in a list with delete the column name it is return a list.

convert_to_float:
This function tackes a list and convert it data type to float.

classify:
This function is for classify the type of users to Subscribers and Customers depending on duration of trip and return two lists.

counter_days:
This function is for classify the type of users to Subscribers and Customers depending on duration of trip and return two lists.


The Questions I have answered in this analysis:

- What is the average trip length for each city?
- Which city has the highest number of trips?
- Which city has the highest proportion of trips made by subscribers? 
- Which city has the highest proportion of trips made by short-term customers?
- What is the average trip length for each city? 
- What proportion of rides made in each city are longer than 30 minutes?
- Which type of user takes longer rides on average: Subscribers or Customers?
- For each group, where is the peak of each distribution? 
- How would you describe the shape of each distribution?


Source:
* https://classroom.udacity.com/nanodegrees/nd002-mena-connect/parts/df47a726-8f27-48f5-90b2-ac1037ab4b94/modules/8a1784ab-aa4a-4df8-8d89-a331b31dbfed/lessons/e07a8fd7-ba87-44c5-98ac-65d9440fa310/concepts/628c5ac1-a424-418c-ba2f-e344ec0fa067

** https://github.com/mohammed-otaibi/Explore-US-BikeShare-Data/blob/master/Bike_Share_Analysis.ipynb