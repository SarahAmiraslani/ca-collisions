# San Diego County Collisions Exploratory Analysis

## Overview
Using geospatial data, we explore whether the location of popular clubs and bars in San Diego County is related to traffic collisions reported between 2015 and 2019. We define traffic collisions to broadly encompass any traffic violation that is reported and documented in the county's publicly available dataset. Note that these collisions involve events as serious as DUIs to minor breaches such as tailgating related collisions. In addition to analyzing the proximity of traffic collisions to San Diego nightlife, we explore whether car accidents are significantly more likely to occur at certain times of the day (e.g., midnight) or certain days of the week (e.g., Saturdays). Lastly, we explore whether there exists any police biases that lead certain groups of people to be stopped and questioned by the police for significantly longer periods of time.

## Group members
- **Sarah Amiraslani**, GitHub ID: SarahAmiraslani
- **Paul Chu**, GitHub ID: paulchu54
- **Catherine Eng**, GitHub ID: ceeng
- **Jose Jimenez**, GitHub ID: JoseJimenezJr019
- **Erin Park**, GitHub ID: eyp012
- **Alysa Quijada**, GitHub ID: alysa-quijada

## Research Questions
1. What types of traffic collisions are most common within San Diego county (e.g., DUIs, hit-and-runs, driving on the wrong side of the road, speeding)?
2. Is there a relationship between distance to high bar density areas such as gaslamp quarters, north park, east village, little Italy, pacific beach, hillcrest, and traffic collisions?
3. Which police beats and geographic divisions within San Diego county attend to the most severe accidents (i.e., those with the highest injuries and fatalities)?
4. Can we identify any police biases in the demographics of people who are stopped and questioned on the road?

## Hypothesis
1. In response to research question 1: We predict that minor, non-fatal accidents and crashes will be the most prevalent. We expect that most people are following traffic laws and trying not to get into accidents when driving on a normal day. This would then suggest that most accidents would be minor accidents as people are not deliberately trying to get into big accidents and being conscious. Null hypothesis: There is no difference in the prevalence of traffic collision types in San Diego County.

2. In response to research question 2: We predict that more collisions will occur in locations where nightlife is common (e.g., Pacific Beach and Gaslamp) rather than the suburbs. Part of most nightlife activities, such as bars and clubs, involves drinking and staying up late through the night. With late nights and alcohol influence, we predict more traffic collisions in those areas. Null hypothesis: There is no effect of traffic collisions in relation to high bar density areas.

3. In response to research question 3: We predict that regions with lower-income neighborhoods would have more severe accidents. Low-income neighborhoods may be slower to fix problematic infrastructures, such as damaged roads, causing more collisions. The higher number of collisions also might make police responses slower in these areas. Null hypothesis: There is no effect of geographic divisions and police beats in relation to more severe accidents.

4. In response to research question 4: We predict that people of a younger age get stopped and questioned on the road more often. Driving has a lot to do with experience, and those who have been driving longer tend to be better. From this, we expect that those with less experience overall are more likely to be stopped and questioned. Null hypothesis: There are no biases in the demographics of people who are stopped and questioned on the road.

## Background
San Diego County is the second-largest population in California, meaning that there is a higher rate of car accidents in San Diego County just by the sheer number of people. In San Diego, more people die from car accidents than being murdered (Bowen, 2017). The rate of car accidents continues to increase while also being reported that these traffic collisions are happening more in low-income neighborhoods. In addition, the leading cause of car accidents in San Diego County is driving under the influence.

Through this project, we hope to inform the San Diego public about locations and times where collisions most occur to help people make more informed decisions. Specifically, in areas where drunk driving accidents are more prevalent, we want to encourage the use of rideshare apps to promote road safety. By pulling the results directly from data relevant to San Diego, we hope to bring more awareness to residents and responding officer’s patrol beats about the trends we see happening.

Note: To understand our data cleaning steps and analyses, you must understand that police officers are assigned regions of the county to patrol, and these regions are called police beats. San Diego county is divided into 140 Police Beats that make up nine geographic divisions that are referenced in our analyses: Northern, Northeastern, Eastern, Southeastern, Central, Western, Southern, Mid City, and Northwestern San Diego. Below is a map of the beats and geographic divisions in San Diego county. For a better quality image, click the link below the map.

For more information on San Diego beats see: https://www.sandiego.gov/police/services/divisions

## Datasets
**Traffic collisions dataset**
- Data from 2015 to 2019
- source:https://data.sandiego.gov/datasets/police-collisions/
- Number of observations: 28122
- This dataset includes information about reported collisions between the years of 2015 to 2019 in San Diego County. Data contains variables such as the date and time that the collision occurred, the police beat number corresponding to the location of the accident, the address of the accident, the violation type, a description of the charge, the number of people injured, the number of people killed, and severity level of the offense (e.g., misdemeanor or felony).

**Police stops dataset**
- Data from 2018 to 2019
- Source: https://data.sandiego.gov/datasets/police-ripa-stops/
- Number of observations:179725
- This dataset includes information on police stops between 2018 and 2019 in San Diego County. Data contains variables such as the date of the stop, the duration of the stop, whether the stop was in response to a call for service, the officer's assignment, the address of the stop, the police beat corresponding to the stop location, the gender, age, and sexual preferences of the person stopped.

**Yelp bars dataset**
- Source: Yelp API
- link: https://drive.google.com/a/ucsd.edu/file/d/11QL6OqdMeBze3QHyMnBN2CFRUKtTPdmt/view?usp=sharing
- Number of observations: 50
- This dataset includes Yelp data of bars in San Diego county. The data contain variables such as the name of the bar, the bar's ratings on yelp, the number of ratings the bar has, the URL to the bar's website, and the longitude and latitude coordinates corresponding to its location.

**Yelp clubs dataset**
- Source: Yelp API
- link:https://drive.google.com/a/ucsd.edu/file/d/1sIjYBX4jSsTmKgmt2BnUeWT1W_xLaxow/view?usp=sharing
- Number of observations: 49
- This dataset includes Yelp data of night clubs in San Diego county. The data contain variables such as the name of the club, the club's ratings on yelp, the number of ratings the club has, the URL to the club's website, and the longitude and latitude coordinates corresponding to its location.

We work on each of the datasets independently and did not need to combine datasets into a single dataframe. The yelp datasets allow us to see if any correlation lies within the location of these nightlife locations and vehicle collisions.

## Results
![alt text](https://github.com/SarahAmiraslani/SD_collisions/blob/master/map.png)

## Ethics & Privacy
Despite pulling data from publically available datasets, insensitive analyses and false conclusions could affect the beliefs and well-being of San Diego residents. Thus, we have taken precautions to input data that respects the privacy of individuals whose information are in the dataset using the Safe Harbour protocol, as well as carefully considering our conclusions. Specifically, the information of any individual over the age of 90 was removed. Moreover, though we found more collisions in lower-income areas with a higher population of people of color, we took care to mention the crucial factors that likely effect this result such as neglected traffic lights, worn-out cars leading to car malfunctions, and damaged roads.

## Conclusion & Discussion
Taking into account the different aspects of this question, as well as the results we found, we can conclude that certain aspects of our hypotheses were correct, while others were a bit misguided. For example, the type of traffic violations that are most common within San Diego county were violating traffic signals and signs. This varies only slightly from our original hypothesis, in that minor collisions are not among the most prevalent, but rather general traffic violations occur at a much higher rate. Still, it is important to note that these seemingly small violations could very easily lead to much larger and more serious collisions and injuries, so it would be wise to figure out why exactly these things are happening to perhaps prevent any major collisions in the future.

Our group was interested in determining whether or not more collisions occur in communities with higher nightlife activity. It was expected that police beats that patrol communities with high nightlife activity, which include Pacific Beach, Hillcrest, Gaslamp Quarters, and North Park, would have higher frequency of collisions. The data shows that Pacific Beach had the highest frequency of collisions with almost 1500 collisions. Kearny Mesa, North Park, Mira Mesa, and La Jolla were the next cities with the highest number of collisions within San Diego county. Although La Jolla does not have high nightlife activity, the high number of collisions can be due to other factors such as age distribution. Since La Jolla is well-known as a city where people come to retire, the population of the city consists of a lot more older individuals. For most driver’s licenses, people are required to renew their license after the age of 65 because driving competency begins to decline at that age. Although the Central Division of San Diego County had the highest nightlife activity, the data did not show the Central Division to be an area with high collision frequency. As for the question of which geographic region of San Diego is host to the highest volume of severe accidents (totaled cars, injuries, deaths, etc.), we found that police beat 122, Pacific Beach, had the highest number of traffic collisions, Northwestern San Diego had the highest average amount of injuries, and Southern San Diego had the highest average number of fatalities. Pacific Beach is a San Diego neighborhood well known for its active nightlife, which may be a contributor to the amount of traffic collisions that occur.

Lastly, we investigated whether there were any biases in police in the demographics of the people who were stopped and questioned. We predicted that younger people would get stopped more than people of older age. In our data, we found that younger people were stopped more often with longer duration, which aligned with our hypothesis. Along with reasons stated in our hypothesis, younger people might be getting stopped with longer durations because officers might be taking more time to explain the procedures and traffic laws.

## Limitations
Some of the limitations we faced were in the datasets we used. One limitation was that we weren’t able to access data for every single bar in San Diego, which affects the visualization of the data and the statistics. The Yelp datasets only gave us the most popular bars that were localized more in downtown San Diego and not getting much from bars more North. This meant we were not getting all of San Diego County. Another limitation in our dataset was that some of the data overlapped in the violations sections, which means some of the data for one violation were duplicated in other violation sections. We also did not consider all violation codes. We also found that the nine regions that we used to split up San Diego County were not truly representative. Each of the nine regions have different cities and each city has a varying density of nightlife activity. Based on each respective region, the data of the cities with different densities were combined into that region. It would have been better to separate regions of San Diego County by police beats for analysis and representation of nightlife activity, but there are 140 police beats. Though it may have been better to separate the regions by the smaller police beat areas, 140 different regions may have over complicated the analysis.

## Affiliation
This was a class project done for [COGS 1O8: Data Science in Practice](https://github.com/COGS108)at the University of California, San Diego. 
