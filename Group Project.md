# DSCI100-Project
url <- "https://archive.ics.uci.edu/ml/machine-learning-databases/heart-disease/cleve.mod"
download.file (url,"cleve.mod" )
colnames <-c("Age","Sex","Chest Pain Type","Resting Blood Pressure", "Cholesteral", "Fasting Blood Sugar","Resting Ecg","Max Heart Rate","Exercise Induced Angina", "Oldpeak","Slope ","Number of Vessels Colored","Thal","Healthy or Sick","Health")
clev_data <-read_delim("cleve.mod",skip=20,delim="   ",col_names=colnames)
clev_data
