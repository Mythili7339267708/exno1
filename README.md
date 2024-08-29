 NAME: V MYTHILI
REG NO: 212223040123
DEPT: COMPUTER SCIENCE AND ENGINEERING
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
```
import pandas as pd
df=pd.read_csv('SAMPLEIDS.csv')
df
```

![image](https://github.com/user-attachments/assets/eb7cf3ae-d65f-4854-93c5-d8cb9e8ee498)



```

import pandas as pd
df=pd.read_csv('SAMPLEIDS.csv')
df.shape
```

![image](https://github.com/user-attachments/assets/42f2b0b1-cda9-4f63-9162-572a6172611b)

```
import pandas as pd
df=pd.read_csv('SAMPLEIDS.csv')
df
df.info()
```
![image](https://github.com/user-attachments/assets/e6242f6a-cb2a-4667-8606-0f484ee1a2a1)


```
import pandas as pd
df=pd.read_csv('SAMPLEIDS.csv')
print(df)
print(df.describe())
```

![image](https://github.com/user-attachments/assets/a8822e4a-2c92-47fe-9da7-94789ce03eab)


```
import pandas as pd
df=pd.read_csv('SAMPLEIDS.csv')
df
df.head(5)
```


![image](https://github.com/user-attachments/assets/c000d7ee-c32a-4097-8d3c-1923ff115f7f)


```
import pandas as pd
df=pd.read_csv('SAMPLEIDS.csv')
df
df.tail(5)
```

![image](https://github.com/user-attachments/assets/2462da49-ca5e-4c0b-8a0f-bc31cf0d7448)

```
import pandas as pd
df=pd.read_csv('SAMPLEIDS.csv')
df
df.isnull().sum()#display how many missing values
```

![image](https://github.com/user-attachments/assets/945b2078-3b02-4723-a7a0-f045a0f201d3)

```
import pandas as pd
df=pd.read_csv('SAMPLEIDS.csv')
df.nunique()
```

![image](https://github.com/user-attachments/assets/d6ebe003-e58b-454e-ba30-2c3b24b66fca)

```
import pandas as pd
df=pd.read_csv('SAMPLEIDS.csv')
df['GENDER'].value_counts()
```

![image](https://github.com/user-attachments/assets/f22d805b-a8b2-4747-8407-1ac03687bfc2)

```
import pandas as pd
df=pd.read_csv('SAMPLEIDS.csv')
x=df.dropna(how='any')
print(x)
```

![image](https://github.com/user-attachments/assets/b2767b12-064c-44fb-8762-1b1fc4794b91)

```
import pandas as pd
df=pd.read_csv('SAMPLEIDS.csv')
x2=df.dropna(how='all').shape
df
```

![image](https://github.com/user-attachments/assets/8de88373-2f4d-479d-b97f-d8a93f3f6f05)


```
import pandas as pd
df=pd.read_csv('SAMPLEIDS.csv')
tot=df.dropna(subset=['TOTAL'],how='any')
tot
```
![image](https://github.com/user-attachments/assets/cb430686-3d53-425a-8824-c76e8b05fa1c)

```
import pandas as pd
df=pd.read_csv('SAMPLEIDS.csv')
s=df.fillna(0)
s
```
![image](https://github.com/user-attachments/assets/22c02525-3eaf-4471-a015-f1c563c10959)

```
import pandas as pd
df=pd.read_csv('SAMPLEIDS.csv')
s=df.fillna(method='ffill')
s
```

![image](https://github.com/user-attachments/assets/261dd8c3-e66c-4b2d-8bc0-84cca12bd31c)


```
import pandas as pd
df=pd.read_csv('SAMPLEIDS.csv')
df.isna().sum()
```

![image](https://github.com/user-attachments/assets/61a2e010-f0c1-45d0-b02a-a9dc53581484)

```
import pandas as pd
df=pd.read_csv('SAMPLEIDS.csv')
df['M1']
```

![image](https://github.com/user-attachments/assets/7894fea7-e321-47b0-a2d9-7d2949c7bd60)


```
import pandas as pd
df=pd.read_csv('SAMPLEIDS.csv')
df.isnull()
```

![image](https://github.com/user-attachments/assets/7a680651-20d9-4851-b220-8ac0e743dde5)

```
import pandas as pd
df=pd.read_csv('SAMPLEIDS.csv')
x1=df.dropna(axis=0)
x1
```

![image](https://github.com/user-attachments/assets/5ebc48d6-1828-4cd6-a17f-b22f30297697)


```
import pandas as pd
df=pd.read_csv('SAMPLEIDS.csv')
df.notnull().sum()
```

![image](https://github.com/user-attachments/assets/73bafb89-7333-4b71-b2aa-015a831b358e)

```
import pandas as pd
df=pd.read_csv('SAMPLEIDS.csv')
m=df.drop_duplicates(inplace=False)
m
```

![image](https://github.com/user-attachments/assets/0667a151-0cba-4321-87e5-9128d9ef034b)


```
import pandas as pd
df=pd.read_csv('SAMPLEIDS.csv')
import seaborn as sns
sns.heatmap(df.isnull(),yticklabels=False,annot=True)

```

![image](https://github.com/user-attachments/assets/f3eba1af-371d-4637-9a2e-ffee26cabd4b)

```
import pandas as pd
df=pd.read_csv('SAMPLEIDS.csv')
df.dropna(inplace=True)
sns.heatmap(df.isnull(),yticklabels=False,annot=True)
```

![image](https://github.com/user-attachments/assets/f39ec641-97fb-43a0-b4a9-eb45b1e61f19)


```
import pandas as pd
df=pd.read_csv('SAMPLEIDS.csv')
print(df.loc[0:3])
```

![image](https://github.com/user-attachments/assets/31cd52ab-503e-492c-a53e-81334ae070dd)

```
import pandas as pd
import seaborn as sns
import numpy as np
age=[1,3,28,27,25,92,30,39,40,50,26,24,29,94]
af=pd.DataFrame(age)
af
```

![image](https://github.com/user-attachments/assets/b43fd4e3-ba51-4114-876b-ee49e1f69868)


```
sns.boxplot(data=af)
```

![image](https://github.com/user-attachments/assets/66e0bf5a-b5c9-4687-ab1d-24d6a81fc2bd)


```
sns.boxenplot(data=af)
```

![image](https://github.com/user-attachments/assets/18ae56de-ff38-4227-afee-11d564393e6f)

```

q1=af.quantile(0.25)
q2=af.quantile(0.5)
q3=af.quantile(0.75)
iqr=q3-q1
iqr#inte rcontile reduction
q1=np.percentile(af,25)
q3=np.percentile(af,75)
IQR = q3-q1
IQR
lower_bound = q1 - 1.5 * IQR
lower_bound
upper_bound = q3 + 1.5 *IQR
upper_bound
outliers = [x for x in age if x < lower_bound or x > upper_bound]
outliers

```

![image](https://github.com/user-attachments/assets/eb625697-5315-4532-9a69-80c1951e69c7)


```
af=af[((af>=lower_bound)&(af<=upper_bound))]
af# outliers values are replaced by nan
```


![image](https://github.com/user-attachments/assets/a71c7e76-cf8b-48df-a4bd-b5dd468947a4)

```
sns.boxplot(data=af)
```

![image](https://github.com/user-attachments/assets/492b5370-f91e-409f-b11f-4afb1d4fb1ad)


```
id=pd.read_csv("iris.csv")
id
```

![image](https://github.com/user-attachments/assets/63ef7b47-3e37-4330-b0db-f6eede94974c)


```

sns.boxplot(x='sepal_width',data=id)
```



![image](https://github.com/user-attachments/assets/69be9396-a23c-448a-8ac0-51bcef529b76)

```
c1=id.sepal_width.quantile(0.25)
c3=id.sepal_width.quantile(0.75)
iq=c3-c1
print(c3)

```


![image](https://github.com/user-attachments/assets/113c87cb-0d5e-4509-b4e9-70ed2164e9c2)

```

rid=id[((id.sepal_width<(c1-1.5*iq))|(id.sepal_width>(c3+1.5*iq)))]
rid['sepal_width']
```

![image](https://github.com/user-attachments/assets/b5cfc339-1607-47d9-b74b-07ff03fb2408)

```
delid=id[~((id.sepal_width<(c1-1.5*iq))|(id.sepal_width>(c3+1.5*iq)))]
delid
```


![image](https://github.com/user-attachments/assets/347edbf5-4f76-4e4f-9f43-8ff182994a8f)


```

sns.boxplot(x='sepal_width',data=delid)

```


![image](https://github.com/user-attachments/assets/26149c4f-d82a-4e52-ad51-87dbbb8bae15)

# Result
               Thus we have cleaned the data and removed the outliers by detection using IQR and Z-score method.
