
# Predicting medical expenses using Linear Regression

- Any insurance Company offers affordable health insurance to thousands of customer all over the United States. 
- As the a data scientist we're tasked with creating an automated system to estimate the annual medical expenditure for new customers, using information such as:
`age`, `sex`, `BMI`, `children`, smoking habits(`smoker`) and `region` of residence

## Libraries Used 
- pandas 
- numpy as np
- plotly.express as px 
- matplotlib.pyplot as plt  
- seaborn as sns 
- from urllib.request -->  urlretrieve 
- sklearn 

### Steps
1. let's download the data using the urlretrieve function from urllib.request.
2. check the data type for each column. using `.info() ` and `.describe()`
3. We'll explore the data by visualizing the distribution of values in some columns of the dataset, and the relationships between "charges" and other columns.
4. We'll use libraries Matplotlib, Seaborn and Plotly for visualization.
- Throughout EDA we will use following plots:
    - px.histogram
    - px.box
    - px.scatter
    - px.violin
4. We Encode the data as sex and smoker are binary columns, we use simple binary Encoding.
5. The "region" column contains 4 values, so we Used hot encoding and create a new column for each region.

## Observation after EDA
1. `age`, `bmi` and `smoker` are three most influencing columns for our target variable `charges`.
2. We used `.corr` method to determine the Correlation between columns.


##### We design 3  Linear Regression models using various methods
- We maintain a dictionary `rmse_dict` to get 3 rmse errors to compare.
- For first model we use `train_test_split` from sklearn.
- For 2nd Model we used Scaling method and scaled the data.
- For 3rd model we used only orignal numerical columns `age` `bmi` and `children`.
- and then compared all three rmse.

`{'1st': 6065.341008508664,'2nd': 6043.542556795788, 
'3rd': 11355.317901125973}`# Predicting_medical_charges
