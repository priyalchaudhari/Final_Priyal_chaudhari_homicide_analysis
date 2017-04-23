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

### Plots: 
![weaponused](https://cloud.githubusercontent.com/assets/25044602/25302541/6fef44de-270e-11e7-8224-0ee26e89ad16.png)


![male female distribution with weapon](https://cloud.githubusercontent.com/assets/25044602/25302545/9179151c-270e-11e7-9d70-78230c861440.png)

![gunlicenceperstate](https://cloud.githubusercontent.com/assets/25044602/25302548/9a6881f8-270e-11e7-838b-480473ca27e7.png)


![statewiseheatmap](https://cloud.githubusercontent.com/assets/25044602/25302562/a33420da-270e-11e7-8227-9505e6aca683.png)


### conclusion:
- That Higher Rates of Gun Ownership Lead to Higher Rates of Violent Crime Rifle Association and other gun-rights proponents, who have steadfastly pushed the idea that a society with more guns leads to less crime, and that “the only way to stop a bad guy with a gun is a good guy with a gun.”
- shows that gun ownership is more often a catalyst than a deterrent to crime.
- As seen in graphs California, Texas issues most license and the murder count in those states are more
- More number of registration issued the crime is increasing. So with that I can conclude that the gun which is given for the safety and self defence is being used for commiting crimes.

# Analysis 2:

## Factors Affecting solving murder crimes. 

### Steps: 
- The data files containing homicide and Weapons Registration data is read in to a dataframe
- get the unique value in perpatrator column 
- Count the number of cases solved for each race known and count the number of cases unsolved
- Count the number of cases solved and unsolved if the race is UNKNOWN 
- plot the graph for Perpatrator race vs number of cases 
- Follow same procedure for Victim sex and Relationship 
- Plot the graphs for both 
- Used random forest algorithm to check wheather the factors I am getting with graph match with feature ranking of algorithm

### output:

### Plot
![race vs crimesolved](https://cloud.githubusercontent.com/assets/25044602/25303292/afbee42a-271d-11e7-924f-b8d84e2325cc.png)


![victim race vs crimesolved](https://cloud.githubusercontent.com/assets/25044602/25303294/b83e27b4-271d-11e7-8e8d-4ebf5b925ea5.png)

![relationship vs crimesolved](https://cloud.githubusercontent.com/assets/25044602/25303298/c13908de-271d-11e7-99b2-81b4085b34e1.png)

### Algorithm Result:
 
![captureqw](https://cloud.githubusercontent.com/assets/25044602/25303391/12622900-2720-11e7-99b5-63813a529cec.PNG)


![wq](https://cloud.githubusercontent.com/assets/25044602/25303396/1dca632a-2720-11e7-8f5f-813a8c326c6c.PNG)

### Conclusion: 
- Based on the result in the graph Most valuable features above 15%: Perpetrator Sex, Perpetrator Age, Perpetrator Race,Relationship
- I have also plotted the the gapth for victim race but that factor is not making significance difference. Even if the victim race is known there are several cases that has gone unsolved 
- With perpatrator race known most of the cases are solved in that case 
- With relationship is also same sinario . Most of cases go unsolved if relationship between victim and perpatrator is unknown 
- With this analysis I conclude that Perpatrator race, Relation are two most important factors to solve the case. 
- Even with relationship if the relationship is stranger then also cases are solved but if its unknown then the rate of solving decreases 
- The results that I am getting from random forest are same that I have got in the graph . 


# Analysis 3:
## most safe and Unsafe state in united states based on rate of homicide.
## conclusion based on (Number of crimes per 10,000 people for each state)

### Steps:
- First downloaded and cleaned data for population for each state and calculate avg of population for each state 
- Read the data from both the dataset. 1) Homocide dataset and 2) Population Dataset
- Calculate the number of cases grouped by state 
- Then calculate the ave population per state 
- sorth the dataframe to get top and bottom values 
- combine both dataset in to single frame and plot the graph 

### Output

### Plot

![result](https://cloud.githubusercontent.com/assets/25044602/25308456/b51746c8-2782-11e7-9fad-c56e21280c3a.png)

![result_safe](https://cloud.githubusercontent.com/assets/25044602/25308460/c8d35756-2782-11e7-9cc4-bc4522215e16.png)


### Conclusion: 
- Two of most unsafe states where crime rates are high are D.C. and Louisiana
- North Dakota and New Hampshire are the 2 safe states according to crime rate
- -The FBI's crime report for 2012 found nearly 68% of all homicides in America involved a firearm, and Louisiana fiercely protects the right to bear arms. The state passed an amendment in November making gun ownership a "fundamental right" like free speech and making it extremely difficult to pass laws that step on that right. Louisiana also passed a law recently that lets its citizens apply for concealed carry handgun permits that last their entire lifetimes. Louisianans who want to walk around and openly carry their guns don't need a permit at all under the state's open carry law. 
- This is the link for above statastics <http://www.businessinsider.com/why-is-the-murder-rate-high-in-louisiana-2013-9>
- Hence because of the very low regulation the homicide rate is high in Louisiana. 

# Analysis 4 : 
## Crime rate with change of wheather.
## How whather is affecting crime in United States
## Combined Wheather data with Homicide data to see the pattern and also Used state abbrivation data to match the statenames
### Steps:
- First collected the data for wheather for the link mentioned above 
- In that data the teparature for state is given monthwise 
- Converted the interger number month column in to word format 
- The state names mentioned are in abbrivated format in temp data 
- downloaded and used a US STATE and there abbrivation CSV file to merge with temparature data so that I have statename in full format now 
- calculated the avg temp for each state the temparature is splited monthwise because we wanted to see the pattern when wheather changes 
- The calculate the number of incidents for each state monthwise 
- For that counted the incidents grouped by month and state 
- Merged both data based on state and month . Statenames ar matched using the abbrivation file used 
- Then splitted the data in separate datafrome statewise 
- Each state will have 12 months of data in a dataframe 
- plotted a line chart for each state to see the progression in number of crimes with change in wheather 

### Output 

### Plots: 
![california](https://cloud.githubusercontent.com/assets/25044602/25309199/63377d02-2794-11e7-8c82-df07d8e8be9a.png)

![new york](https://cloud.githubusercontent.com/assets/25044602/25309202/70bd7120-2794-11e7-8b8a-a4e3d864bb4f.png)

![texas](https://cloud.githubusercontent.com/assets/25044602/25309204/729e0aa4-2794-11e7-928e-0f788f56cdf2.png)

![louisiana](https://cloud.githubusercontent.com/assets/25044602/25309201/6ca29d40-2794-11e7-8ef2-5f67ec71dd1d.png)

### conclusion:
- As seen in the plots with california,Texas,New york all show increase in crime rate with increase in temparature 
- Louisiana which has hieghest crime rate in US (According to findings in previous analysis) surprisingly dosent show any pattern. 
- hot temperatures increase irritability, which in turn increases aggressive behavior, including violent crime.
- "More people out - more crime, less people out - less crime."

# Analysis 5:
## Homicide distribution according to relationship in USA
## Age distribution of each relationship category 

### Steps: 
- First read the data from CSV file in to a dataframe 
- read all the relationship betweent victim and perpatrator 
- categorize the relationship in criterial like male oartner, parents, childrens 
- create a new column in dataframe and all the relationship category values in to that column 
- Count the number of incidents for each category 
- get the total incidents from data frame 
- calculate the pecentage for each category 
- plot the pei chart for percentage 
- then get the age group involved in each category 
- plot a scotter plot to show density of age group. 

### Output:

### plots:

![piechart for percentage](https://cloud.githubusercontent.com/assets/25044602/25309447/6c939d3e-279b-11e7-98ff-82f6e5915783.png)


![piechartanotherversion](https://cloud.githubusercontent.com/assets/25044602/25309445/6c9259a6-279b-11e7-9b93-25105c29519f.png)


![scatterplot](https://cloud.githubusercontent.com/assets/25044602/25309446/6c9312ec-279b-11e7-8552-d33f0c148e4c.png)

### conclusion: 
- AS seen in the pie chart most of the relationships almost half are strangers 
- 2nd most troubled group of relationship is Aquaitence 
- Most of homicide crimes are must be serial killers or gang wars hence relation category is stranger 
- By above graph it is also observed that homicide crimes based on some motive like most of partner or parent category crimes have motive or personal agenda . These crimes are less as compaired to other categories. 
- Scatter plot shows the age group involved in each categoty
- There is a pattern for each category like in neighbour category there is no significant grouping. Whereas in sibling category we will find that maximum grouping is around age 20yrs to 40 yrs  


