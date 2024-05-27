## Obesity Levels Classification 
Obesity is more than a cosmetic concern. The World Health Orgenisation estimates that close to one billion people are obese and along with it comes the risk of many health problems including heart disease, diabetes, and certain cancers. 

This project aims to classify obesity levels using three machine-learning approaches namely Logistic Regression, Random Forest, and KNN and compare the performance of these methods. These computational tools can identify the obesity level of an individual which can be used to further build systems that monitor obesity levels. 


## About Dataset
The data include the estimation of obesity levels in people from the countries of Mexico, Peru and Colombia. They are aged between 14 and 61, with diverse eating habits and physical condition. Data collected obtained 17 attributes and 2111 records.

#### The attributes related with eating habits are: 
* Frequent consumption of high caloric food (FAVC) 
* Frequency of consumption of vegetables (FCVC)
* Number of main meals (NCP)
* Consumption of food between meals (CAEC),
* Consumption of water daily (CH20),
* and Consumption of alcohol (CALC).
#### The attributes related with the physical condition are:
* Calories consumption monitoring (SCC),
* Physical activity frequency (FAF),
* Time using technology devices (TUE),
* Transportation used (MTRANS)

Variables obtained :
Gender, Age, Height and Weight.

The records are labeled with the class variable NObesity (Obesity Level), that allows classification of the data using the values of Insufficient Weight, Normal Weight, Overweight Level I, Overweight Level II, Obesity Type I, Obesity Type II and Obesity Type III. 


The data contains numerical data and continous data, so it can be used for analysis based on algorithms of classification, prediction, segmentation and association. Data is available in CSV format.

## Scope and limitations
The dataset is only limited to Non-Asia Pacific BMI. BMI is the relationship between an individual’s height and weight. Asian BMI, which has a lower cut-off levels, and Polynesian BMI which has a higher cut-off levels are not covered in the dataset.

The World Health Organisation (WHO) Some studies have indicated that individuals of Asian descent may have a higher body fat percentage at a lower BMI compared to other ethnic groups. As a result, some researchers and health organizations have proposed using lower BMI thresholds to define overweight and obesity for Asian populations.

As an example, the International Obesity Task Force (IOTF), which is affiliated with the WHO, has proposed BMI thresholds specific to Asian populations. According to the IOTF criteria, the BMI thresholds for overweight and obesity for Asian adults are:

 + Overweight: BMI ≥ 23 kg/m²
 + Obesity: BMI ≥ 27.5 kg/m²
These thresholds are lower than the standard WHO thresholds, which are:

Overweight: BMI ≥ 25 kg/m²
Obesity: BMI ≥ 30 kg/m²
It's important to note that these BMI thresholds are recommendations and guidelines, and individual health assessments should consider additional factors such as waist circumference, body composition, and overall health status.

Ultimately, while the WHO uses universal BMI thresholds for defining overweight and obesity, healthcare providers and policymakers may consider using population-specific thresholds for certain ethnic groups, including Asians, based on available evidence and guidelines from organizations like the IOTF.

## Visualisations using Python
Visualisations were created using Python libraries such as Pandas, Matplotlib, Seaborn, and Plotly to show the dataset profile.

There are 2111 records with 17 attributes in the dataset which can mainly be grouped into three categories. First, there are almost equal number of males and females. The average age is 24 years old. 170 centimetres and 87 kilograms are the average height and weight, respectively.

![image](https://github.com/JollyCJoseph/project4_group7/assets/152139070/69c73a8d-5b34-4b43-b36a-221f8ce168dd)


The next set of attributes is related to Eating Habits. Most in the dataset eat three meals a day but there’s also a high frequency of consuming high cAloric foods, alcohol, and foods in between meals.

![image](https://github.com/JollyCJoseph/project4_group7/assets/152139070/da979f36-7c8f-44f5-9c66-abc30e35a479)

On the next group of attributes is related to Physical Activities showing more positively skewed distributions which represent the lack of physical activities.

![image](https://github.com/JollyCJoseph/project4_group7/assets/152139070/b25d40b7-a558-4b68-9927-fa98865d8549)

A comparison of the seven Obesity Levels and Family History with Overweight show that being Overweight and/or Obese tends to be hereditary.

![image](https://github.com/JollyCJoseph/project4_group7/assets/152139070/e97b4467-91e3-4199-ab6d-b00157ffa820)


The distribution of Obesity Types of the dataset shows Obesity Type II or Moderate-Risk as the average. The Obesity Type I or  Low-Risk has the maximum number of samples in it and the least are those with Insufficient Weight. In the Machine Learning methods we grouped them into three which Jolly will touch on a bit later. First is Insufficient and Normal Weight, second is Overweight, and last is Obese.

![image](https://github.com/JollyCJoseph/project4_group7/assets/152139070/da57299e-28cf-4a53-8ee5-ec413a1a8519)

## Visualisations using Tableau Public
![image](https://github.com/JollyCJoseph/project4_group7/assets/152139070/2900e9cd-09a8-4ae6-9b6c-4e6033cbe00e)

![image](https://github.com/JollyCJoseph/project4_group7/assets/152139070/1a69932f-e900-4d02-b129-8ae045ef06c9)

![image](https://github.com/JollyCJoseph/project4_group7/assets/152139070/55f3e3bc-047a-4b43-b5e8-721841c501ef)

![image](https://github.com/JollyCJoseph/project4_group7/assets/152139070/471d8bd6-f960-49a4-8d17-00f2e3423303)


## Classification Analysis 
### Linear regression model
![Screenshot 2024-05-23 210930](https://github.com/JollyCJoseph/project4_group7/assets/151517356/2b1a9ba4-5c51-453c-9e48-78a30066c585)
### Random forest
![Screenshot 2024-05-23 211058](https://github.com/JollyCJoseph/project4_group7/assets/151517356/39cac0b3-732d-4b21-8d90-9759511f4060)
### KNN Model
![Screenshot 2024-05-23 211616](https://github.com/JollyCJoseph/project4_group7/assets/151517356/bd4e8da9-cebf-4b3c-85c0-cd13d59a40a8)

All three models predicted well with the highest accuracy of 0.985 with the Logistic Regression Model. For optimising the Logistic Regression Model, we used GridSearchCV for tuning hyperparameters to get the best parameters. After the optimisation, the accuracy increased to 0.99 which is 1.01% more than the pre-tuned model.

## Conclusion

* It was found that Obesity Level III (High-Risk) is more common among females while Obesity Level II (Moderate-Risk) is more common among males.

* Family history with obesity, frequently taking high caloric food, food between meals, etc., are directly related to obesity.

* Insufficient Weight and Overweight Level I are more common among those with no family history of obesity.

* Logistic regression model is best suitable for predicting obesity level in this dataset with an accuracy of 0.99 after hypertuning of parameters using GridSearchCV.


## Reference
 
https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6710633/pdf/main.pdf

https://www.kaggle.com/datasets/aravindpcoder/obesity-or-cvd-risk-classifyregressorcluster

https://www.worldobesity.org/about/about-obesity/obesity-classification

https://apps.who.int/gho/data/node.main-searo.BMIANTHROPOMETRY?lang=en

https://www.mdpi.com/2075-4418/13/18/2949



