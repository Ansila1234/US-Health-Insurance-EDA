# US-Health-Insurance-EDA

This repository contains an exploratory data analysis (EDA) of a dataset related to health insurance in the United States. The goal of this project is to uncover insights about the factors that influence health insurance coverage, cost, and usage.
![health-insurance-img](https://github.com/user-attachments/assets/698bedf7-696b-4c6a-8a1e-34699b06be2b)

# 1. Project Goals
Medical Insurance is a contract that requires an insurer to pay some or all of a person's healthcare costs in exchange for a premium, with the insurance typicallly pays for medical expenses incured by the insured. Insurance cost differs from each individual, certain variable may affect a person insurance cost to be higher or lower.

This project will analyze medical insurance cost in a dataset and exploring variables that may affect it. Further, this project will showcase data analysis skills to provide meaningful insight.

### 1.1 Dataset Overview :
The dataset used in this analysis contains information about health insurance policies, coverage, premiums, and demographic details such as age, income, and region. The dataset was preprocessed and cleaned before performing the analysis.

The dataset is obtained from Kaggle. The dataset consist of 7 columns:

+ **age**: age of primary beneficiary
+ **sex**: insurance contractor gender, male or female
+ **bmi**: body mass index, providing an understanding of body, weights that are relatively high or low relative to height, objective index of body weight  (kg /  m2
 )using the ratio of height to weight
+ **children**: number of children covered by health insurance / number of dependents
+ **smoker**: is the beneficiary smoking? yes or no
+ **region**: the beneficiary's residential area in the US; northeast, southeast, southwest, northwest.
+ **charges**: individual medical costs billed by health insurance, in USD

### 1.2 Tools and Libraries :
The following tools and libraries were used in this project:

+ **Python**
+ **Pandas** for data manipulation
+ **NumPy** for numerical operations
+ **Matplotlib** and **Seaborn** for data visualization
Jupyter Notebook for running the analysis interactively

### 1.3 Objectives :
+ Exploratory Data Analysis and Data Visulaization

### 1.4 Importing the libraries :
![1](https://github.com/user-attachments/assets/8a01dbff-3d88-4536-b932-b3deca406c1b)

# 2. Loading the data :
![2](https://github.com/user-attachments/assets/2fe8f374-827b-49e9-bec3-c2fb986210ee)

![3](https://github.com/user-attachments/assets/203613d2-459f-4033-b98e-03486d654770)

# 3. Exploratory Data Analysis

## 3.1 Shape:
![4](https://github.com/user-attachments/assets/355f36ca-c8ec-46c3-9903-c4cf56e4fa2f)

![5](https://github.com/user-attachments/assets/f63d7927-1291-4aaa-b78f-25202f25d0c2)

## 3.2 Data Types:
![6](https://github.com/user-attachments/assets/fbf6a666-c629-4eef-a61d-9685ecfbc380)

![7](https://github.com/user-attachments/assets/b12a4e12-91aa-404c-a20c-b6896e7f8f31)

![8](https://github.com/user-attachments/assets/60413e49-9784-4185-9e21-ebd5a9e7d9ad)

![9](https://github.com/user-attachments/assets/daf0764f-ac9f-4175-9db0-ab98d7a45033)

![10](https://github.com/user-attachments/assets/021487d6-5795-4467-8b24-2288369d6576)

![11](https://github.com/user-attachments/assets/03d9ded9-5827-4f8c-82b0-9ca6d49523aa)

![12](https://github.com/user-attachments/assets/0c021590-82b7-4958-bd05-b4935a531e73)

![13](https://github.com/user-attachments/assets/0df3044c-a6a0-46c8-89b8-55524720e73d)

![14](https://github.com/user-attachments/assets/31975fb0-b9b6-4cfb-ace0-7eedd527c1e6)

![15](https://github.com/user-attachments/assets/f8152771-e58c-43fc-b272-ae573c217120)

We observe that 'age'(int64), 'bmi'(float64) and 'charges'(float64) are numerical attributes; and 'sex', 'smoker', 'region' and 'children' are categorical attributes.

We observe that the 'children' column is being treated as an integer datatype, even though it contains categorical information.

![16](https://github.com/user-attachments/assets/58e8bd6d-b4e9-4a20-ae68-c53d9263a6a7)

![17](https://github.com/user-attachments/assets/d0217a61-d6f2-4753-aea6-d083bf92c561)

### 3.3 Data Cleaning:
Let's check if the DataFrame contains any missing or null values:

![18](https://github.com/user-attachments/assets/d7b113f6-78d4-4415-a574-415dd2820720)

There are no missing data in the DataFrame.

## 3.4 Summary and Distribution of numerical attributes:
We can get an overview of the important statistics of the data through the describe() method:

![19](https://github.com/user-attachments/assets/fa47c359-6373-4b19-bf18-eb95a497ac6c)

Now let's study the 5-point summary and distribution of the numerical attributes: Age, BMI and Charges.

+ The Density plot gives an intuitive understanding of the underlying distribution of the attribute.
+ The Boxplot (or box-and-whisker plot) shows the distribution of quantitative data in a way that facilitates comparisons between variables or across levels (quantiles) of variable. The box shows the quartiles of the dataset while the whiskers extend to show the rest of the distribution, except for points that are determined to be “outliers” using a method that is a function of the inter-quartile range.
+ Unlike a box plot, in which all of the plot components correspond to actual datapoints, the violin plot features a kernel density estimation of the underlying distribution.
+ The cumulative frequency also corresponds to the density distribution, and indicates the central tendency of the data.

 ![20](https://github.com/user-attachments/assets/60711469-c731-4955-8568-11444379b383)

 ![21](https://github.com/user-attachments/assets/379cc392-cbad-4cbd-9267-8b8304c3c470)

 ## 3.4.1 Age Distribution:

 ![22](https://github.com/user-attachments/assets/36dcb177-0562-462e-a1eb-6d02e6579e9a)

 ![23](https://github.com/user-attachments/assets/4dca729f-1f9f-4062-a6bf-fd2cbb15bb39)

 ![24](https://github.com/user-attachments/assets/6cde56b5-c27f-4b51-a70a-8f0c850132fe)

 ![25](https://github.com/user-attachments/assets/066a6b33-8153-41ff-9be2-5e8fcfbf10ee)

### Observations:
+ The Age of the insured approximately follow a uniform distribution with Mean of 39.2 and Median of 39.0, and with lowest age being 18 and highest being 64.
+ There are no outlier values in the Age distribution in the data.

![26](https://github.com/user-attachments/assets/8934d601-4079-4bf7-892b-d8a5b5e70ea0)






 
































Analysis Objectives
The key objectives of this analysis include:

Understanding the distribution of health insurance coverage across different demographic groups.
Analyzing the factors that influence insurance premiums.
Investigating the relationship between income levels and insurance coverage.
Visualizing trends in health insurance data over time or by region.
Notable Findings
Demographic Analysis: Describe any key insights from your demographic analysis, such as which age group or income bracket tends to have higher insurance premiums.
Premium Trends: Summarize the findings on premium costs and the factors that most significantly affect them.
Coverage Insights: Include any insights on the level of coverage across different regions or other variables.
Visualizations
Here are some visualizations included in this analysis:

Heatmap: A correlation heatmap showing relationships between different variables.
Bar Charts: Representing the distribution of insurance policies across different age groups.
Boxplots: Analyzing the spread of insurance premiums across income groups.


