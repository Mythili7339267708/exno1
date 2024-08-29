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

















# Result
          <<include your Result here>>
