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
data=pd.read_csv("data 1.csv")
df=pd.DataFrame(data)
print(df)
```
<img width="858" height="752" alt="{E5DD6BE4-DDE5-4911-AC95-342A0FD99010}" src="https://github.com/user-attachments/assets/b43c6f3d-c5e0-4048-9131-848279898de0" />

```
import pandas as pd
data=pd.read_csv("data 1.csv")
df=pd.DataFrame(data)
print(df.isnull())
```
<img width="750" height="607" alt="image" src="https://github.com/user-attachments/assets/5079459d-2546-4775-b39d-d897c9f882f1" />

```
import pandas as pd
data=pd.read_csv("data 1.csv")
df=pd.DataFrame(data)
drop=df.dropna()
print("Before dropna",df)
print("After dropna",drop)
```
<img width="914" height="730" alt="image" src="https://github.com/user-attachments/assets/8092a2b9-a101-446a-b5c1-df71e4d03550" />
```
 import pandas as pd
data=pd.read_csv("data 1.csv")
df=pd.DataFrame(data)
print(df.isnull().sum())
```
<img width="326" height="224" alt="image" src="https://github.com/user-attachments/assets/5d696c40-f400-42ea-a8de-9175ab3b2737" />
```
import pandas as pd
data=pd.read_csv("data 1.csv")
df=pd.DataFrame(data)
drop=df.dropna(axis=1)
print("Before dropna /n/n",df)
print("After dropna /n/n",drop)
```
<img width="985" height="750" alt="image" src="https://github.com/user-attachments/assets/3dbf69ff-5aba-4457-b22b-7c43511960b7" />
```
import pandas as pd
data=pd.read_csv("data 1.csv")
df=pd.DataFrame(data)
drop=df.dropna(axis=1,inplace=True)
print("Before dropna /n/n",df)
print("After dropna /n/n",drop)
```
<img width="761" height="320" alt="image" src="https://github.com/user-attachments/assets/f93a3e28-6073-4774-bebb-b9c16e856125" />
```
import pandas as pd
data=pd.read_csv("data 1.csv")
df=pd.DataFrame(data)
fill=df.fillna(method='ffill')
print(fill)
```
<img width="755" height="328" alt="image" src="https://github.com/user-attachments/assets/d0632021-0286-4b86-9f0c-71cd7de54405" />
```
import pandas as pd
data=pd.read_csv("data 1.csv")
df=pd.DataFrame(data)
fill=df.fillna(method='bfill')
print(fill)
```
<img width="861" height="745" alt="image" src="https://github.com/user-attachments/assets/66feec4a-04c8-4e47-aed6-7e8b6881b0e5" />
```
 import pandas as pd
data=pd.read_csv("data 1.csv")
df=pd.DataFrame(data)
mean=df.mean()
print(mean)
```
<img width="452" height="136" alt="image" src="https://github.com/user-attachments/assets/195762bf-7122-435a-acf0-9269e8840625" />
```
import pandas as pd
data=pd.read_csv("data 1.csv")
df=pd.DataFrame(data)
median=df.median()
print(median)
```
<img width="374" height="131" alt="image" src="https://github.com/user-attachments/assets/f0f3df99-27b7-44b5-9c39-b66a1c5c94b2" />
```
import pandas as pd
data=pd.read_csv("data 1.csv")
df=pd.DataFrame(data)
mode=df.mode()
print(mode)
```
<img width="867" height="731" alt="image" src="https://github.com/user-attachments/assets/49bb204e-2a6e-4b04-93de-66140629aff9" />
```
import pandas as pd
data=pd.read_csv("data 1.csv")
df=pd.DataFrame(data)
interpolate =df.interpolate()
print(interpolate)
```
<img width="1004" height="743" alt="{74A544D0-CB9B-4387-9DAA-83E65D40181E}" src="https://github.com/user-attachments/assets/c2689394-59cd-40d5-85c6-ca3bfb028d4d" />
```
import pandas as pd 
import matplotlib.pyplot as plt
import numpy as np
data  = pd.read_csv("data3.csv")
df = pd.DataFrame(data)
print(df)
```
<img width="737" height="314" alt="image" src="https://github.com/user-attachments/assets/be3385eb-bf66-4587-8df4-8b626d330037" />
```
 import pandas as pd 
import matplotlib.pyplot as plt
import numpy as np
data  = pd.read_csv("data3.csv")
df = pd.DataFrame(data)
print(df)
print(pd.descripe())
```
<img width="842" height="724" alt="{B6E6BD6E-C999-44E3-8C91-478466FDE40B}" src="https://github.com/user-attachments/assets/87662228-c307-4067-b42f-830e69784e95" />
```
plt.bar(df["species"],df["sepal_width"])
plt.show()
```
<img width="670" height="497" alt="{4F9C3C81-A2A5-417C-AC99-DABF7A23B877}" src="https://github.com/user-attachments/assets/f69e5686-9b8b-477c-bf70-78f3d7c5dce8" />
```
plt.scatter(df["sepal_length"],df["sepal_width"])
plt.show()
```
<img width="751" height="534" alt="{E4F7E23E-86EE-4FE1-A35C-8AC6259B1F31}" src="https://github.com/user-attachments/assets/81b2e22d-d3b0-4dcd-9dc8-db1403c722c5" />
```
plt.plot(df["species"],df["sepal_length"])
plt.show()
```
<img width="732" height="517" alt="{ABF2C86F-DAE3-47E2-ABCC-A092A1DF16A7}" src="https://github.com/user-attachments/assets/5d112d40-c120-4428-b3ce-18352bee6aad" />
```
 import pandas as pd
data=pd.read_csv("data 1.csv")
df=pd.DataFrame(data)
print(df.isnull().any())
```
<img width="384" height="234" alt="image" src="https://github.com/user-attachments/assets/594160b7-318f-4095-a7db-6ca500a3d66a" />
# Result
          <<include your Result here>>
