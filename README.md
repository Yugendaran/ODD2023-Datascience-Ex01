# Ex-01_DS_Data_Cleansing


## AIM
To read the given data and perform data cleaning and save the cleaned data to a file. 

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. 
Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information. 

# ALGORITHM
### STEP 1
Read the given Data
### STEP 2
Get the information about the data
### STEP 3
Remove the null values from the data
### STEP 4
Save the Clean data to the file

# CODE:

**DATA CLEANING HANDLING NULL** **VALUES**

import pandas as pd

df=pd.read_csv('/content/SAMPLEDS.csv')

df

df.shape

df.describe()

df.isnull().sum()

df.dropna(how='any').shape

x=df.dropna(how='any')

x

df.dropna(how='all').shape

tot = df.dropna(subset=['TOTAL'],how='any')

tot

m = df.dropna(subset=['M4'],how='any')

m

tot = df.dropna(subset=['M1','M2','M3','M4'],how='any')

tot

df.fillna(0)

df

df.fillna(method='ffill')

df.fillna(method='bfill')

mn=df.TOTAL.mean()

mn

df.TOTAL.fillna(mn,inplace=True)

df

l=df.M1.interpolate()

l

df.M1.fillna(l,inplace=True)

df

mn=df.TOTAL.median()

mn

df.TOTAL.fillna(mn,inplace=True)

df

l=df.M1.interpolate()

l

df.M1.fillna(l,inplace=True)

df

mn=df.TOTAL.mode()

mn

df.drop_duplicates(inplace=True)

df

df['cd']=pd.to_datetime(df['DOB'])

df

for x in df.index:
  if df.loc[x,"AVG"]>100:
    df.drop(x,inplace=True)
    
df

# Output:
![image](https://github.com/Yugendaran/ODD2023-Datascience-Ex01/assets/128135616/ac34c6d8-e10f-4d6c-8682-0a41642c35a9)

file:///home/sec/Pictures/Screenshot%20from%202023-08-29%2013-14-26.png![Uploading image.png…]()


