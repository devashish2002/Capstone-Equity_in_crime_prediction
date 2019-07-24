# Accuracy and Equity in Hot-spot policing
Code for capstone project

Abstract - Several recent studies have demonstrated the efficacy of proactive policing strategies for crime prevention. By predicting emerging geographic hot-spots of violent crime, we can target police patrols and other interventions. However, predictive policing creates moral and ethical concerns, such as fairness and equity, which have been well-documented, yet have not been typically incorporated into the design and evaluation of such systems. In this work we develop machine learning methods to predict hot-spots of crime and present a way to measure equity among those areas. We then adjust the predictions based on the defined equity metric and analyze the trade-offs between accuracy and equity. We also see the performance of the two models based on the racial distribution of the targeted population.

## Model comparison:
<img width="514" alt="modelCF" src="https://user-images.githubusercontent.com/24549241/61807650-f2061600-ae07-11e9-9da6-d22ae8dc7e34.png">

## Predictions without Equity measure

Fitted line
![rf_trend_pred](https://user-images.githubusercontent.com/24549241/61807781-2ed20d00-ae08-11e9-8265-15f472d77a1e.png)

Crimes captured
![rf_curve](https://user-images.githubusercontent.com/24549241/61807809-3ee9ec80-ae08-11e9-8890-44b1ff0618d5.png)

## Predictions with equity measure
 
![pred_op_comparison](https://user-images.githubusercontent.com/24549241/61807894-66d95000-ae08-11e9-8113-293287da6353.png)



## Folder RandomForest
Contains code used to model Random Forests on Census Tracts in NYC

## Folder Chicago
Contains the code for initial exploratory analysis done on crime data of Chicago

## Folder Portland
Contains the code for initial exploratory analysis done on crime data of Portland


