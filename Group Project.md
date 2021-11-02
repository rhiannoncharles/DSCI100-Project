# DSCI100-Project
library(tidyverse)
colnames <-c("Age","Sex","Chest Pain Type","Resting Blood Pressure", "Cholesteral", "Fasting Blood Sugar","Resting Ecg","Max Heart Rate","Exercise Induced Angina", "Oldpeak","Slope ","Number of Vessels Colored","Thal","Healthy or Sick","Health")
clev_data <-read_delim("DATASCI Group Project 39/cleve.mod",skip=20,delim="   ",col_names=colnames)
clev_data
