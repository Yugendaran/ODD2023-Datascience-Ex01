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

![image](https://github.com/Yugendaran/ODD2023-Datascience-Ex01/assets/128135616/9e734620-fc40-49aa-99f5-e6acdc9c442e)

![image](https://github.com/Yugendaran/ODD2023-Datascience-Ex01/assets/128135616/d73918e1-5a68-4c17-aada-418bb9e5ac62)

![image](https://github.com/Yugendaran/ODD2023-Datascience-Ex01/assets/128135616/2be1d6f2-a960-4c99-8ab3-a874e507899c)

![image](https://github.com/Yugendaran/ODD2023-Datascience-Ex01/assets/128135616/4d47fd85-5f53-4b33-8cd1-c8d37db44081)

![image](https://github.com/Yugendaran/ODD2023-Datascience-Ex01/assets/128135616/1c49a726-4aa4-4d82-ac37-c61ebba3e3ef)

![image](https://github.com/Yugendaran/ODD2023-Datascience-Ex01/assets/128135616/e5883e91-2459-4030-997c-d50de198e2b4)

![image](https://github.com/Yugendaran/ODD2023-Datascience-Ex01/assets/128135616/57c325df-5ad0-4641-951d-ab6285043e51)

![image](https://github.com/Yugendaran/ODD2023-Datascience-Ex01/assets/128135616/e2e8d3e6-9d0a-4b58-a726-159ca46cd91b)

![image](https://github.com/Yugendaran/ODD2023-Datascience-Ex01/assets/128135616/14efba85-ca11-4e70-8766-7e1bc366b1cd)

![image](https://github.com/Yugendaran/ODD2023-Datascience-Ex01/assets/128135616/c264bcbf-1365-42b6-96e4-0d11670e9824)

![image](https://github.com/Yugendaran/ODD2023-Datascience-Ex01/assets/128135616/255fb8bd-50a0-4f62-97b1-7d605c1b58e0)







