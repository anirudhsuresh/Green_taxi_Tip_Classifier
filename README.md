# Green Taxi Tip Classifier Model : Project Overview :
* Created a tool based on a classifer model which could predict if a taxi ride in NYC would be able to secure tips based on a number of factors 
* Used [Data](https://s3.amazonaws.com/nyc-tlc/trip+data/green_tripdata_2019-01.csv) from January 2019 from NYC open data
* Also added [taxi zones](https://s3.amazonaws.com/nyc-tlc/misc/taxi+_zone_lookup.csv) data , in order to be able to get the borough where the taxi operated
* Engineered Features from the data : speed of taxi , distance travelled ,pick up /drop off hours , location of pickup /drop
* Used random forest model to classify if tips were secured 


## Code and Packages Used 
* *R Version :* 4.0.5 
* *Packages:* mlbench,tidyverse,ggplot2,caret,lubridate,olsrr,randomForest,cowplot,tidymodels,parsnip,reshape,pROC,ggeasy

## Data Cleaning 
After getting the data from the webisite and merging the two data sets , I made the following changes and created the following variables :
* Removed negative values of all distances of trip , trip cost,fare ,etc
* Limited passgeners to 6
* Removed two columns eHail and store and forward flags since they had over 99% Null enteries
* Created variables :
    * pick up hour
    * drop off hour 
    * pick up borough(s)
    * drop off borough(s)
* Transformed all variables to the right data types 


## EDA 
