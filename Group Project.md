# DSCI100-Project
#Downloading the neccessary packages.
library(tidyverse)
library(tidymodels)

#Setting the seed.
set.seed(1234)

#Dowloading the data from the web and reading it in R.
url <- "https://archive.ics.uci.edu/ml/machine-learning-databases/heart-disease/cleve.mod"
download.file (url,"cleve.mod" )
colnames <-c("Age","Sex","Chest_PainType","Rest_Blood_Press", "Cholesterol", "Fast_Blood_Sug","Rest_Ecg","Max_Heart_Rate","Exercise_Induced_Angina", "Oldpeak","Slope ","Nmbr_of_Vessels_Col","Thal","Buff_or_Sick","Health")
clev_data <-read_delim("cleve.mod", skip=20, delim="   ", col_names=colnames)%>%
    mutate(Buff_or_Sick = as_factor(Buff_or_Sick))%>%
    mutate(Max_Heart_Rate = as.numeric(Max_Heart_Rate))%>%
    mutate(Nmbr_of_Vessels_Col = as.numeric(Nmbr_of_Vessels_Col))%>%
    filter(Buff_or_Sick == "buff" | Buff_or_Sick == "sick")

#Splitting the data into a training and a testing set.
#75% of the data will be randomly taken as training data.
clev_split <- initial_split(clev_data, prop = 0.75, strata = Buff_or_Sick)  
clev_train <- training(clev_split)   
clev_test <- testing(clev_split)
head(clev_train)

#Selecting predictor variables and visualizing the summary of the predictor variables.
data_selected <- clev_train %>%
    select(Cholesterol, Max_Heart_Rate, Nmbr_of_Vessels_Col )
summary(data_selected)


#Visualizing the distribution of two predictor variables with training data.
plot_1 <- clev_train %>%
    ggplot(aes(x=Cholesterol, y=Max_Heart_Rate, color=Buff_or_Sick))+
    geom_point()+
    labs(x="Cholesterol", y="Max Heart Rate", color="Health Status")+
    ggtitle("Cholesterol vs Max Heart Rate")
plot_1




