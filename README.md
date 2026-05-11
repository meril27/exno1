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
data=pd.read_csv("/content/SAMPLEIDS.csv")
data
```
<img width="907" height="712" alt="image" src="https://github.com/user-attachments/assets/485ea524-fd65-4bcf-8013-65c9e562f91e" />
<br>

```
data.info()
```
<img width="892" height="462" alt="image" src="https://github.com/user-attachments/assets/fd61472a-67b2-4318-8d23-39e4aeaa8998" />
<br>

```
data.describe()
```
<img width="982" height="351" alt="image" src="https://github.com/user-attachments/assets/d67859e5-7ce3-4a7e-8d65-4433033dc6de" />
<br>

```
data.isnull()
```
<img width="1025" height="766" alt="image" src="https://github.com/user-attachments/assets/cb3f6e81-02ea-426f-bb65-56b2adc8cc94" />
<br>

```
data.isnull().sum()
```
<img width="882" height="342" alt="image" src="https://github.com/user-attachments/assets/d638ad81-ca13-43c9-ba1c-29094d86125d" />
<br>

```
data.notnull()
```
<img width="1123" height="652" alt="image" src="https://github.com/user-attachments/assets/9ed84972-ad18-49ad-9298-39aee2300bda" />
<br>

```
data.notnull().sum()
```
<img width="581" height="628" alt="image" src="https://github.com/user-attachments/assets/c20da81a-3a03-4e5f-aad1-3339c440517d" />
<br>

```
data.dropna()
```
<img width="1380" height="621" alt="image" src="https://github.com/user-attachments/assets/8b3810b7-f8dd-4506-83e8-c62b45496b04" />
<br>

```
data.dropna(axis=1)
```
<img width="730" height="701" alt="image" src="https://github.com/user-attachments/assets/5aa0d052-b934-4ec1-9d65-3f8a1ea164d2" />
<br>

```
data
```
<img width="1212" height="695" alt="image" src="https://github.com/user-attachments/assets/3285fa4c-a6f7-4d13-be06-3f13875f698c" />
<br>

```
data.dropna(inplace=True)
data
```
<img width="1136" height="612" alt="image" src="https://github.com/user-attachments/assets/88157584-c81e-4d34-b9bc-b9b22f6d0bbc" />
<br>

```
import pandas as pd
data1=pd.read_csv("/content/Loan_data.csv")
data1
```
<img width="1747" height="582" alt="image" src="https://github.com/user-attachments/assets/a3781fbc-4e3c-4a0e-a517-eab12a8ef631" />
<br>

```
data.isnull()
```
<img width="1003" height="560" alt="image" src="https://github.com/user-attachments/assets/619307f5-49a3-4b51-a79c-f47e59df3cf3" />
<br>

```
data.isnull().sum()
```
<img width="821" height="561" alt="image" src="https://github.com/user-attachments/assets/3e828e35-5c6f-4e0e-9297-e08b65e724ee" />
<br>

```
data.fillna("Datascience")
```
<img width="1346" height="561" alt="image" src="https://github.com/user-attachments/assets/7d156da0-40aa-4d0d-b9b2-7f8b6ec7c41f" />
<br>

```
data
```
<img width="1215" height="571" alt="image" src="https://github.com/user-attachments/assets/78fdcf44-4f3c-4b79-8073-e16fd70f0838" />
<br>

```
data.ffill()
```
<img width="1156" height="551" alt="image" src="https://github.com/user-attachments/assets/ceab7d92-0452-45e5-bd7e-b034bf2f4e16" />
<br>

```
data=pd.read_csv("/content/SAMPLEIDS.csv")
data
```
<img width="1090" height="703" alt="image" src="https://github.com/user-attachments/assets/74c46ca8-9335-4681-ad8e-73b41ed75d0d" />
<br>

```
data.ffill()
```
<img width="1110" height="707" alt="image" src="https://github.com/user-attachments/assets/a85d2c8c-277f-4813-b8bf-cf6952261c90" />
<br>

```
data.bfill()
```
<img width="965" height="702" alt="image" src="https://github.com/user-attachments/assets/2c3c5eaf-e8f0-41e5-8695-d24f1f6f1578" />
<br>

```
data['TOTAL'].fillna(method='bfill',inplace=True)
```
<img width="1788" height="306" alt="image" src="https://github.com/user-attachments/assets/9d276efb-5547-4718-917f-6b641086fa51" />
<br>

```
data
```
<img width="1210" height="705" alt="image" src="https://github.com/user-attachments/assets/4880c270-aa4a-4a53-b0b2-b014b54b635e" />
<br>

```
data['M4'].fillna(value=data['M4'].mean(),inplace=True)
```
<img width="1791" height="246" alt="image" src="https://github.com/user-attachments/assets/305436d6-4c7d-4b3d-a0c1-cb14ce71d93b" />
<br>

```
data
```
<img width="1196" height="707" alt="image" src="https://github.com/user-attachments/assets/b5a1b087-ce8f-488f-8ff5-d7d5baa05b09" />
<br>

```
data['M4'].fillna(value=data['M4'].median(),inplace=True)
```
<img width="1802" height="248" alt="image" src="https://github.com/user-attachments/assets/8bcc9b39-eda3-4d93-bdb6-88799c7b6039" />
<br>

```
data
```
<img width="1133" height="717" alt="image" src="https://github.com/user-attachments/assets/30a07686-552b-47ce-b142-3677cc6af122" />
<br>

```
data['M4'].fillna(value=data['M4'].mode(),inplace=True)
```
<img width="1771" height="225" alt="image" src="https://github.com/user-attachments/assets/e5d2cfcd-1534-486e-bddd-f900adc1074b" />
<br>

```
data
```
<img width="1127" height="711" alt="image" src="https://github.com/user-attachments/assets/34562354-2df4-4cd9-88c9-343902b647cb" />

## IQR Method:

```
import pandas as pd
ir=pd.read_csv("iris.csv")
ir
```
<img width="596" height="437" alt="image" src="https://github.com/user-attachments/assets/e1f272a3-c007-461b-806c-932a19e82b3d" />
<br>

```
ir.describe()
```
<img width="492" height="297" alt="image" src="https://github.com/user-attachments/assets/42b6875c-f9f2-45e5-907d-0028e2827040" />
<br>

```
ir.shape
```
```
(150, 5)
```
```
ir.info()
```
<img width="458" height="257" alt="image" src="https://github.com/user-attachments/assets/f21eddb3-adbf-488d-8536-1841ada8cbc0" />
<br>

```
import seaborn as sns
sns.boxplot(x='sepal_width',data=ir)
```
<img width="712" height="582" alt="image" src="https://github.com/user-attachments/assets/3d3d87bb-6a26-4dd6-adb1-ef4940144a48" />
<br>

```
 q1=ir.sepal_width.quantile(0.25)
 q3=ir.sepal_width.quantile(0.75)
 iqr=q3-q1
 print(iqr)
```

```
0.5
```

```
 out=ir[((ir.sepal_width<(q1-1.5*iqr))|(ir.sepal_width>(q3+1.5*iqr)))]
 out['sepal_width']
```
<img width="326" height="116" alt="image" src="https://github.com/user-attachments/assets/69f268f2-cbdd-44f1-91c9-7d1d18edd8ba" />
<br>

```
 nor=ir[~((ir.sepal_width<(q1-1.5*iqr))|(ir.sepal_width>(q3+1.5*iqr)))]
 nor['sepal_width']
```
<img width="487" height="268" alt="image" src="https://github.com/user-attachments/assets/8cd9c592-4cef-438e-80b4-0cfa70e4851b" />
<br>

```
sns.boxplot(x='sepal_width',data=nor)
```
<img width="672" height="578" alt="image" src="https://github.com/user-attachments/assets/d7418248-5fab-4f5a-9f6f-37dc460b6946" />
<br>

Z-Score Method:

```
import numpy as np
import pandas as pd
df=pd.read_csv("heights.csv")
df
```
<img width="192" height="498" alt="image" src="https://github.com/user-attachments/assets/794dba04-7d41-486b-b285-838331195fd3" />
<br>

```
import scipy.stats as stats
q1 = df['height'].quantile(0.25)
q2 = df['height'].quantile(0.5)
q3 = df['height'].quantile(0.75)
iqr = q3-q1
iqr
```

```
0.92499999999999998
```

```
low = q1 - 1.5*iqr
print(low)
high = q3 + 1.5*iqr
print(high)
```
<img width="205" height="55" alt="image" src="https://github.com/user-attachments/assets/8a498148-926d-4a86-b8c8-f2039a215273" />
<br>

```
df1 = df[((df['height'] >=low)& (df['height'] <=high))]
df1
```
<img width="213" height="433" alt="image" src="https://github.com/user-attachments/assets/1f6fd021-fb70-42a0-a771-08f3d41b78db" />
<br>

```
z = np.abs(stats.zscore(df['height']))
z
```
<img width="291" height="328" alt="image" src="https://github.com/user-attachments/assets/ef8a19f8-b8b5-459a-9349-e7b203282383" />
<br>

```
df1 = df[z<3]
df1
```
<img width="186" height="461" alt="image" src="https://github.com/user-attachments/assets/49cf82d1-ba8d-456c-b860-7a8dcc5d1c64" />

# Result
The given dataset was successfully read and cleaned using Python. Missing values and duplicate records were handled properly, and the cleaned data was saved into a new file named cleaned_data.csv.
