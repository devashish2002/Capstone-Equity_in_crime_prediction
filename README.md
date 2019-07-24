# Accuracy and Equity in Hot-spot policing

### Overview
Several recent studies have demonstrated the efficacy of proactive policing strategies for crime prevention. By predicting emerging geographic hot-spots of violent crime, we can target police patrols and other interventions. However, predictive policing creates moral and ethical concerns, such as fairness and equity, which have been well-documented, yet have not been typically incorporated into the design and evaluation of such systems. In this work we develop machine learning methods to predict hot-spots of crime and present a way to measure equity among those areas. We then adjust the predictions based on the defined equity metric and analyze the trade-offs between accuracy and equity. We also see the performance of the two models based on the racial distribution of the targeted population.

### Why bother?

Past studies indicate possible bias against certain groups and demographics due to a variety of reasons ranging from past prevalence of crimes in a location to feedback loops arising from continuous intevention in a geography and ignoring other areas.

<img width="937" alt="Screen Shot 2019-07-24 at 11 51 46 AM" src="https://user-images.githubusercontent.com/24549241/61808474-74dba080-ae09-11e9-92cf-79cf96e4c264.png">

The work presented focus on the following key areas:(1) Accuracy of predictive hot-spot methods and <br/>
(2) Methods to bring about more equity into predictive models.

Some of the key questions answered are the following:<br/>
What are the best evaluation metrics for measuring accuracy and equity in predictive policing? <br/>
Can simple equitymetrics, measuring to what extent patrols are concentrated or dispersed across a city, be improved to account forneighborhood demographics, socio-economics, and crime victimization/underlying need for policing? <br/>
Are there trade-offs between policing accuracy and equity, or is it possible to maximize both criteria simultaneously?<br/>

### Machine Learning models used:

Long Short Term Memory (LSTM) neural networks
Gaussian Processes (GP)
Random Forests (RF)

<img width="514" alt="modelCF" src="https://user-images.githubusercontent.com/24549241/61807650-f2061600-ae07-11e9-9da6-d22ae8dc7e34.png">

### Defining equity

We have defined the metric as a proportion of estimated need of policing to the actual deployment on ground. Both these metrics cannot be directly measured but can be indirectly assessed through proxy measures. As a proxy for demand for policing, we consider the metric "Level of disorder" in neighborhoods measured by Vacant Buildings/Plots, 311 complaints, Garbage disposal problems etc. But from further discussions we decided to measure the Part 1 Violent Crimes as a proxy for policing demand with the assumption that all violent crimes are captured by the police department and gets reflected in the crime data. To assess the actual deployment of police forces we considered using drug/narcotics related crimes but historical data suggests that some locations might be more prone to drug related crimes. Instead we chose total number of arrests within a census tract as proxy considering that most of these instances happen during police patrolling.

<img width="510" alt="Screen Shot 2019-07-24 at 12 04 56 PM" src="https://user-images.githubusercontent.com/24549241/61809426-46f75b80-ae0b-11e9-8342-862d56b029b5.png">

### Predictions without Equity measure

Fitted line
![rf_trend_pred](https://user-images.githubusercontent.com/24549241/61807781-2ed20d00-ae08-11e9-8265-15f472d77a1e.png)

Crimes captured
![rf_curve](https://user-images.githubusercontent.com/24549241/61807809-3ee9ec80-ae08-11e9-8890-44b1ff0618d5.png)

### Predictions with equity measure
 
![pred_op_comparison](https://user-images.githubusercontent.com/24549241/61807894-66d95000-ae08-11e9-8113-293287da6353.png)

### Spatial distribution

<img width="1358" alt="Screen Shot 2019-07-24 at 11 48 22 AM" src="https://user-images.githubusercontent.com/24549241/61808205-f54dd180-ae08-11e9-851f-f36ee813062e.png">

### Racial distribution of targeted population

<img width="1110" alt="Screen Shot 2019-07-24 at 11 49 14 AM" src="https://user-images.githubusercontent.com/24549241/61808270-144c6380-ae09-11e9-9183-d5b7e7378934.png">


#### Folder RandomForest
Contains code used to model Random Forests on Census Tracts in NYC

#### Folder Chicago
Contains the code for initial exploratory analysis done on crime data of Chicago

#### Folder Portland
Contains the code for initial exploratory analysis done on crime data of Portland


