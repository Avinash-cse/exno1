# Exno:1
Data Cleaning Process

# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# Algorithm
STEP 1: Read the given Data

STEP 2: Get the information about the data

STEP 3: Remove the null values from the data

STEP 4: Save the Clean data to the file

STEP 5: Remove outliers using IQR

STEP 6: Use zscore of to remove outliers

# Coding and Output
import pandas as pd

df=pd.read_csv("SAMPLEIDS.csv")

print(df)

<img width="842" height="492" alt="Screenshot 2026-07-27 200857" src="https://github.com/user-attachments/assets/ab6f2025-c5c9-4fb8-b42a-9a1a0c5850bd" />
<img width="320" height="482" alt="Screenshot 2026-07-27 200904" src="https://github.com/user-attachments/assets/dd2f513b-b842-4a9d-a2e4-8380700d34c5" />

df.shape

<img width="165" height="35" alt="Screenshot 2026-07-27 200910" src="https://github.com/user-attachments/assets/8541bac7-e24b-480e-9ee6-fb2c6078a7ac" />
df.head()
<img width="955" height="222" alt="Screenshot 2026-07-27 200917" src="https://github.com/user-attachments/assets/fe4a3361-017e-4afd-a029-10b1df11fc83" />
df.tail()
<img width="993" height="217" alt="Screenshot 2026-07-27 200937" src="https://github.com/user-attachments/assets/ebe07e9e-5020-4d7e-b52d-ce8bccfbadef" />
df.info()
<img width="450" height="413" alt="Screenshot 2026-07-27 200951" src="https://github.com/user-attachments/assets/40cbcd11-5e6f-4a5a-bb27-2c6ec75030f4" />
df.describe()
<img width="937" height="310" alt="Screenshot 2026-07-27 200957" src="https://github.com/user-attachments/assets/b1c1296f-b3c0-419c-83d3-7ccddfe5afb1" />
df.isnull()
<img width="887" height="736" alt="Screenshot 2026-07-27 201005" src="https://github.com/user-attachments/assets/6d513200-8564-4b7a-b069-ffcf8f0625f8" />
df.notnull()
<img width="897" height="738" alt="Screenshot 2026-07-27 201013" src="https://github.com/user-attachments/assets/ea60fa2d-4d62-47c0-a66e-d12b48b68670" />
df.isnull().sum()
<img width="242" height="295" alt="Screenshot 2026-07-27 201019" src="https://github.com/user-attachments/assets/4f35688c-d661-46d0-81c5-9b4f8c355243" />
df.isnull().any()
<img width="283" height="292" alt="Screenshot 2026-07-27 201024" src="https://github.com/user-attachments/assets/cf2077ea-5a2d-4432-830c-b9daf5736784" />
df.dropna()
<img width="1052" height="491" alt="Screenshot 2026-07-27 201029" src="https://github.com/user-attachments/assets/1da604cb-e9b2-4ba2-94a5-f770a80049c2" />
df.dropna(axis=1)
<img width="491" height="415" alt="Screenshot 2026-07-27 201041" src="https://github.com/user-attachments/assets/b0c1ab08-48a1-4972-a7c3-82b2bad5e615" />
df.fillna(method='ffill')
<img width="1020" height="740" alt="Screenshot 2026-07-27 201059" src="https://github.com/user-attachments/assets/bf7c6aad-a582-44a6-a05f-9544ec9eba48" />
df.fillna(method='bfill')
<img width="1032" height="727" alt="Screenshot 2026-07-27 201106" src="https://github.com/user-attachments/assets/a8a2da50-b04d-43cc-bc48-7557a20e604e" />
df.fillna({'GENDER':'MALE','NAME':'SRI','M1':'150'})
<img width="1035" height="736" alt="Screenshot 2026-07-27 201114" src="https://github.com/user-attachments/assets/3d76ced8-87a4-45d7-955c-0c473be2a54a" />
ir=pd.read_csv("iris.csv")
print(ir)
<img width="713" height="312" alt="Screenshot 2026-07-27 201120" src="https://github.com/user-attachments/assets/9a90de38-3aea-44be-a2ef-6e261010e1a3" />
ir.shape
<img width="217" height="40" alt="Screenshot 2026-07-27 201124" src="https://github.com/user-attachments/assets/8795b007-b4aa-455f-8f74-34b1eb748554" />
ir.head()
<img width="642" height="220" alt="Screenshot 2026-07-27 201129" src="https://github.com/user-attachments/assets/645f9e0e-37e6-4b28-8e88-9e11d591d6d4" />
ir.tail()
<img width="717" height="227" alt="Screenshot 2026-07-27 201133" src="https://github.com/user-attachments/assets/b340beb4-6185-4307-941b-80dd7b1727ef" />
ir.isnull()
<img width="736" height="422" alt="Screenshot 2026-07-27 201141" src="https://github.com/user-attachments/assets/2b04a3ef-d6f9-44d6-9b2b-70dedf542549" />
ir.isnull().sum()
<img width="327" height="145" alt="Screenshot 2026-07-27 201146" src="https://github.com/user-attachments/assets/fcbbe5f6-d12c-4fd8-ba00-46125beacf47" />
ir.describe()
<img width="592" height="312" alt="Screenshot 2026-07-27 201151" src="https://github.com/user-attachments/assets/433d9aff-4488-4ee6-a95b-080ce67bc239" />
import seaborn as sns
sns.boxplot(x='sepal_width',data=ir)
<img width="917" height="427" alt="Screenshot 2026-07-27 201217" src="https://github.com/user-attachments/assets/9e5323f9-72c0-4be3-b2c5-f112f13b4ff9" />
sns.boxplot(x='sepal_length',data=ir)
<img width="887" height="583" alt="Screenshot 2026-07-27 201225" src="https://github.com/user-attachments/assets/9cada6a1-e8bd-4819-b598-388d77bd5bd6" />
sns.boxplot(x='petal_length',data=ir)
<img width="808" height="590" alt="Screenshot 2026-07-27 201230" src="https://github.com/user-attachments/assets/bc6884f7-742f-4c97-bce7-e96186b2d439" />
sns.boxplot(x='petal_width',data=ir)
<img width="878" height="581" alt="Screenshot 2026-07-27 204147" src="https://github.com/user-attachments/assets/75acf689-13f6-4816-b532-8ce377e9493f" />
Q1=ir.sepal_width.quantile(0.25) 
Q3=ir.sepal_width.quantile(0.75) 
(IQR)=Q3-Q1 
print(IQR)
<img width="83" height="40" alt="Screenshot 2026-07-27 204152" src="https://github.com/user-attachments/assets/9f00432e-f50f-477e-8317-c66ead71df54" />
ran=ir[((ir.sepal_width<(Q1-1.5*IQR))|(ir.sepal_width>(Q3+1.5*IQR)))] 
ran['sepal_width']
<img width="451" height="117" alt="Screenshot 2026-07-27 204155" src="https://github.com/user-attachments/assets/8b2aac3f-fea0-4ee8-8866-72178c1cd986" />
ran=ir[~((ir.sepal_width<(Q1-1.5*IQR))|(ir.sepal_width>(Q3+1.5*IQR)))] 
ran['sepal_width']
<img width="568" height="268" alt="Screenshot 2026-07-27 204202" src="https://github.com/user-attachments/assets/1a298144-75b7-4e3e-8e5f-d375dd428da7" />
sns.boxplot(x='sepal_width',data=ran)
<img width="837" height="587" alt="Screenshot 2026-07-27 204208" src="https://github.com/user-attachments/assets/79ef5f16-f8fb-4c03-a2ad-0474856c1daf" />
import numpy as np
import scipy.stats as stats 
z=np.abs(stats.zscore(ir['petal_length'])) 
print(z)
<img width="522" height="277" alt="Screenshot 2026-07-27 204212" src="https://github.com/user-attachments/assets/881ed77c-ba7c-4a6e-a1ab-7e8f9e6bbfd8" />
ir1=ir[z<3] 
print(ir1)
<img width="743" height="317" alt="Screenshot 2026-07-27 204216" src="https://github.com/user-attachments/assets/e48e2396-f1a8-45fe-9c23-3df1eb8baa14" />
# Result
The given data is read and data cleaning is successfully performed and saved the cleaned data in a file. Outliers detection using IQR and Z score methods are successfully performed.
