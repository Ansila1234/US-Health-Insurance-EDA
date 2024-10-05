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

## 3.4.2 BMI Distribution

![27](https://github.com/user-attachments/assets/9b598a33-c547-4143-ab0b-6394ab11b14d)

![28](https://github.com/user-attachments/assets/d93d0de1-767b-458f-8c84-4b5d42fd8df6)

![29](https://github.com/user-attachments/assets/20242f33-b567-4302-ab57-e5424b59d575)

![30](https://github.com/user-attachments/assets/24a02eef-0543-4d9d-9d26-ddb2484de7c2)

![31](https://github.com/user-attachments/assets/099a97ec-4c16-438a-a98e-35702d03dbc5)

![32](https://github.com/user-attachments/assets/64fbb29e-3d52-45be-8df8-cb2975ed791c)

### Observations:

+ The BMI distribution of the Insured approximately follows a normal distribution with a Mean of 30.66 and Median of 30.4.
+ There are a total of 9 outlier values in the BMI distribution, all in the higher side. The highest BMI observed is 53.13.
+ The person with the highest BMI (least healthy, based on available data) is also one of the youngest (male, 18, non-smoker.) He is paying less premium than the mean, but significantly more than the median charges. This is in line with our basic understanding of underwriting rules.

## 3.4.3 Charges Distribution:

![33](https://github.com/user-attachments/assets/58745ba8-cd69-453a-9a16-7eea2e7d2e4b)

![34](https://github.com/user-attachments/assets/d9570c2b-1e8c-4e7f-bc1f-b910e9a1e3ed)

![35](https://github.com/user-attachments/assets/afd5a45c-25c2-46fc-a196-4e222e6edbff)

![36](https://github.com/user-attachments/assets/e13eb543-c1e3-4ed5-aced-11faaac9fc78)

![37](https://github.com/user-attachments/assets/9624bdd1-b9c2-4deb-87df-4365ddd6370d)

![38](https://github.com/user-attachments/assets/7c3ca2fc-f267-49a8-b703-5a8366affd52)

![39](https://github.com/user-attachments/assets/8dc7f7d3-f2be-4c18-93db-5a68aa920903)

### Observations:

+ The Charges distribution of the Insured is heavily skewed to the left (median < mean) with a Mean of 13270.4223 and Median of 9382.033. The lowest charged amount is 1121.8739 and the highest charged amount is 63770.42801.
+ Out of a total of 1338 data points, there are a total of 139 outlier values in the distribution of charges, all in the higher side. The highest charges paid is 63770.42801.
+ The insured chared with highest premium is a 54 years old female smoker with relatively high BMI (indicating obesity).
+ The person with the highest BMI (obese, or least healthy, based on available data) is also one of the youngest (male, 18, non-smoker.) He is paying less premium charges than the mean(which, we note, is affected by extreme outlier values of charges like the person above), but significantly more than the median. This is in line with our basic understanding of underwriting rules.

## 3.5 Summary and Distribution of categorical attributes:

Let's explore the distribution of categorical variables:'sex','smoker','region' and 'children'.

![40](https://github.com/user-attachments/assets/82fc73eb-da13-4a35-afe5-78f0bfb5f75a)

## 3.5.1 Sex:

![41](https://github.com/user-attachments/assets/b72cc301-9d93-4f50-92aa-d5d2acc937f1)

![42](https://github.com/user-attachments/assets/254d5415-8338-46c3-8539-8f2bd203dd50)

### Observations:
The dataset is almost evenly distributed among genders, with 676 Males (50.5%) and 662 Fenales (49.5%).

### 3.5.2 Smoker

![43](https://github.com/user-attachments/assets/219b9a04-4b5d-4336-aa83-f3e8f594d0a6)

![44](https://github.com/user-attachments/assets/59ef830e-d0d3-436c-99da-0fb332c15cc0)

![45](https://github.com/user-attachments/assets/9f3e8dbf-0a8c-4719-854b-ee21c7a36284)

![46](https://github.com/user-attachments/assets/7cd94bab-fee0-4efe-823a-f52f0a5654ab)

![47](https://github.com/user-attachments/assets/3e846651-1ea2-4ee3-b951-cc36569993f0)

![48](https://github.com/user-attachments/assets/61fa51c8-5cf5-4d32-940b-274f1ecf603d)

![49](https://github.com/user-attachments/assets/8ddf578f-2250-4138-ae1f-6056e4264b50)

### Observations:
+ Of the total 1338 insured, 274 (20.5%) are smokers and the rest are non-smokers.
+ Among 274 smokers, proportion of males (159) are higher than females (115).
+ The average insurance premium for smokers are significantly higher than non-smokers.

## 3.5.3 Regions

![50](https://github.com/user-attachments/assets/4fb8da86-a234-4de7-ac25-fa8cb8c25d5b)

![51](https://github.com/user-attachments/assets/7b3f52ed-16d4-4b62-95cb-ee7d63fe13ff)

### Observations:
+ All four regions are represented approximately evenly in the dataset.

## Number of children

![52](https://github.com/user-attachments/assets/505a8d55-ea58-4a1e-8672-54bf1ac6a6cb)

![53](https://github.com/user-attachments/assets/bb14ccfe-e6d8-4bc3-ad52-3447dd79b0bb)

![54](https://github.com/user-attachments/assets/bd3f734f-5bca-4126-b180-cb27f3c4bc76)

### Observation:
+ In the dataset,approximately 85% (1138/1338) of the insured have less than 3 children.

## Pairplot
Let's plot pairwise relationships in our dataset through a pairplot. In order to show all columns in our pairplot, first let's convert all categorical attributes to their category codes. First we set the datatypes of all the categorical variables as category:

![55](https://github.com/user-attachments/assets/ecf85de2-748b-4ca1-a455-2dafb36aa9e2)

![56](https://github.com/user-attachments/assets/22483e2c-a15f-4e1b-9368-19de03b75e71)

![57](https://github.com/user-attachments/assets/9c9e7e6e-be9a-4fb0-8af2-ed85bdb40c64)

![58](https://github.com/user-attachments/assets/b6053d5b-8316-4968-bc51-8b4f4077b03a)

![59](https://github.com/user-attachments/assets/fa868558-4501-46ed-b48f-392900607d99)

![60](https://github.com/user-attachments/assets/8f687f6f-33b2-4a3b-8d90-ef174ea834f0)

A particularly interesting relationship between insurance premium charges, BMI and smoking status(Smoker/Non-smoker) can be seen in this graph:

![61](https://github.com/user-attachments/assets/10b67f3f-5182-4a28-971e-3ee447534332)

![62](https://github.com/user-attachments/assets/458c34a2-08ee-4ba8-ae1d-efbcff2038b6)

## 3.7 Correlation:
Let's study the correlation between different attributes in our dataset.

![63](https://github.com/user-attachments/assets/a9648de3-bfb7-4cff-92a7-018d7a655aa6)

### Observations:
From the correlation heatmap, we can conclude that the premium charges show a weak positive correlation with Age and BMI of the insured, and a strong positive correlation with smoking habit.







