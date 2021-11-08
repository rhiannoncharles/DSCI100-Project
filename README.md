# DSCI100-Project
Title: Predicting Heart Disease 

Introduction
Heart disease is currently the leading cause of death from a non-transmissible source with 8.9 million people dying from it annually (Filate et al. 2003; Health Agency of Canada 2018). This is mainly due to a growing aging population making it so a larger portion of people are more prone to cardiovascular diseases (Health Agency of Canada 2018; Statista 2021). However, the disease takes years to develop and is very easily preventable by monitoring or reducing risk factors through various lifestyle changes such as eating a healthy diet, increasing physical activity, and limiting smoking and alcohol consumption (Statista 2021; Government of Canada, 2017). Therefore, early detection of risk factors can help prevent heart disease from developing, or can help prevent the progression of the disease. 

Hence, our research question is:
How can age, blood pressure, cholesterol, heart rate, and number of major blood vessels predict heart disease?

For this analysis we will be using the modified Cleveland dataset from the Heart Disease Data Set from the UCI Machine Learning Repository. The dataset consists of 15 different attributes as follows:
"age","sex","cp_type","rest_bp", "chol", 
             "fbs","restecg","max_hr","eir", 
             "op","slope","num_bv","thal","class","health"

age: Age of person in years
sex: (1 = male, 0 = female)
cp_type: The types of chest pain experienced (Value 1: typical angina, Value 2: atypical angina, Value 3: non-anginal pain, Value 4: asymptomatic)
rest_bp: Resting blood pressure (mm Hg on admission to the hospital)
chol: serum cholesterol in mg/dl
fbs: Fasting blood sugar (if > 120 mg/dl, 1 = true; 0 = false)
restecg: Resting electrocardiographic measurement (0 = normal, 1 = having ST-T wave abnormality, 2 = showing probable or definite left ventricular hypertrophy by Estes’ criteria)
max_hr: Maximum heart rate achieved
eia: Exercise induced angina (1 = yes; 0 = no)
op: ST depression induced by exercise relative to rest (‘ST’ relates to positions on the ECG plot)
slope: the slope of the peak exercise ST segment (Value 1: upsloping, Value 2: flat, Value 3: downsloping)
num_bv: The number of major vessels (0–3)
thal: A blood disorder called thalassemia (1 = normal; 2 = fixed defect; 3 = reversible defect)
class: With or without heart disease (buff = healthy, sick = heart disease)
health: Heart disease (0 = no, 1, 2, 3, 4 = yes)
To create our model we will be selecting age, resting blood pressure, max heart rate, cholesterol, and the number of major vessels for our predictors. Then we will be using the class as our predicted attribute. 



Methods:
We will do a classification to predict if the individual has heart disease or not. We plan on using all the variables so we can make an #accurate prediction. One way we will visualize our results is with a scatterplot that shows the likelihood of heart disease based on #certain predictors. We hope to find certain predictors that better show the likelihood of heart disease which can help to make it easier #to predict it in patients. Further questions that could come from this are what combinations of two or three predictors show the highest #likelihood of heart disease or what combinations are the least accurate. 

Sources

Filate, Woganee A., Helen L. Johansen, Courtney C. Kennedy, and Jack V. Tu. 2003. “Regional Variations in Cardiovascualr Mortality in Canada.” Canadian Journal of Cardiology 11 (19): 1241.
Government of Canada. 2017. “Heart Disease in Canada.” Canada.ca. https://www.canada.ca/en/public-health/services/publications/diseases-conditions/heart-disease-canada.html.
Health Agency of Canada. 2018. “Report from the Canadian Chronic Disease Surveillance System: Heart Disease in Canada.” Canadian Electronic Library/desLibris. https://go.exlibris.link/CPyKsFFV.
Statista. 2021. “Death rate for major cardiovascular diseases in Canada from 2000 to 2019.” https://www.statista.com/statistics/434439/death-rate-for-major-cardiovascular-diseases-in-canada/.



