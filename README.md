# Ex-01_DS_Data_Cleansing
# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# ALGORITHM
## STEP 1
Read the given Data

## STEP 2
Get the information about the data

## STEP 3
Remove the null values from the data

## STEP 4
Save the Clean data to the file

# CODE
#data_set
```
import pandas as pd
df = pd.read_csv("/content/Data_set.csv")
df.head(5)
df.info()
df.isnull().sum()
#MODE:
df['show_name'] = df['show_name'].fillna(df['show_name']).mode()[0]
df['aired_on'] = df['aired_on'].fillna(df['aired_on']).mode()[0]
df['original_network'] = df['original_network'].fillna(df['original_network']).mode()[0]
#MEAN:
df['rating'] = df['rating'].fillna(df['rating']).mean()
df['current_overall_rank'] = df['current_overall_rank'].fillna(df['current_overall_rank']).mean()
#FORWARD METHOD:
df['watchers'] = df['watchers'].fillna(method='ffill')
df.isnull().sum()
```
```
#loan_data
import pandas as pd
df = pd.read_csv("/content/Loan_data.csv")
df.head(5)
df.info()
df.isnull().sum()
#MODE:
df['Gender'] = df['Gender'].fillna(df['Gender'].mode()[0])
df['Self_Employed'] = df['Self_Employed'].fillna(df['Self_Employed'].mode()[0])
df['Dependents'] = df['Dependents'].fillna(df['Dependents'].mode()[0])
#MEAN and MEDIAN:
df['LoanAmount'] = df['LoanAmount'].fillna(df['LoanAmount'].median())
df['Loan_Amount_Term']=df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].mean())
df['Credit_History']=df['Credit_History'].fillna(df['Credit_History'].mean())
df.isnull().sum()
```
# OUPUT
First File:

Data_Set.csv FILE

![first_file](https://user-images.githubusercontent.com/120232371/226583239-a9311a6d-0913-412e-bcab-90617ad8d9b6.png)

INFO

![first_file](https://user-images.githubusercontent.com/120232371/226583465-ed36c85d-0f91-4a88-b428-aeb568ce60fd.png)

Isnull.().sum() before cleaning

![mean](https://user-images.githubusercontent.com/120232371/226583961-b1b87123-0266-4fb4-a6b0-8582eb4762a2.png)

MODE,MEAN and FORWARD METHOD

![mode](https://user-images.githubusercontent.com/120232371/226584368-85644a07-d3e9-4246-b851-ef640338f995.png)

isnull().sum() after cleaning

![median](https://user-images.githubusercontent.com/120232371/226584566-de75010a-30c4-470b-aa29-0e91881fa4b2.png)

Second File:

Loan_Data.csv FILE

![INFO2](https://user-images.githubusercontent.com/120232371/226584903-b0babf5e-0571-4ab9-be3d-2b7e4bf634ee.png)

INFO

![IFO3](https://user-images.githubusercontent.com/120232371/226585167-35651463-7bf2-4503-8401-4eb97272c9f4.png)

Isnull.().sum() before cleaning

![IFO](https://user-images.githubusercontent.com/120232371/226585389-d51bf412-28c0-4207-96bd-cae85b69669b.png)

MODE,MEAN and MEDIAN

![IFO1](https://user-images.githubusercontent.com/120232371/226585673-5e57ab79-fe82-4ca7-8156-3368d6ebd357.png)

snull().sum() after cleaning

![LAST](https://user-images.githubusercontent.com/120232371/226585937-b92cd15d-d160-4e12-bb4c-600abbef7957.png)









