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
