# INFO7374 Data Analysis Using Python - Final Project
## Homicide Data Analysis (Final)
## Data Used:

- For this analysis used Homicide dataset in .CSV format as main dataset you can see the files [here](Final/data) Filename Database and database1 are main dataset files 

- Also used Weapons Registration dataset for analysis 1 statewise you can find the data [Here](Final/data). Weapons data i have got from [National Instant Criminal Background Check System (NICS)](https://www.fbi.gov/services/cjis/nics)

- For analysis 4 used wheather dataset to combine with homicide dataset to see how homicide rate gets effected with change of wheather you can find wheather data [Here](Final/data). Wheather and temparature data was downloaded from <https://www.ncdc.noaa.gov/>

- For analysis 3 used population data statewise to combine with homicide data you can find population data [here](Final/data). Population data is fetched from <https://catalog.data.gov/dataset?res_format=CSV>

### Purpose for doing analysis on homicide: 
- Nowadays homicide crimes in USA has increased. Wanted to find out factors that contribute in those crimes. 

## Analysis Performed: 
# Analysis 1 : 

## Preferred weapon for homicide and genderwise weapon of choice. Why that weapon is used statewise breakdown 

### Steps: 
- The data files containing homicide and Weapons Registration data is read in to a dataframe
- Filter the date get only entries where crime is solved. So that we know which weapon is used. Also filter wntries where gender is UNKNOWN
- For each weapon count the number of incidents and plot the grapth . 
- Split the data based on gender and count the number of incidents group by Weapon for male and female separately ans plot the grapth 
- From second dataset get Avg number of Handgun and LongGun Issued by each state . Because those are the 2 most used weapon for crime. 
- Plot the graph of count of gun lisence issued by each state. The data is present for 20 years 
- From main dataset plot the heatmap for statewise weapon used.

### Output: 
CSV Files:[]()
png Files: []()
