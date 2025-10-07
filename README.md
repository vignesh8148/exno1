<img width="858" height="752" alt="{E5DD6BE4-DDE5-4911-AC95-342A0FD99010}" src="https://github.com/user-attachments/assets/ff16495f-8d31-47d7-b69c-7add4df15746" /># Exno:1
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
<img width="917" height="729" alt="{8293E64D-EFB3-4FD3-BD08-DB6A32AA1A38}" src="https://github.com/user-attachments/assets/ce5fdba3-2475-4881-ac1e-e8595fdee98f" />
```
import pandas as pd
data=pd.read_csv("data 1.csv")
df=pd.DataFrame(data)
print(df.isnull())
```
<img width="829" height="572" alt="{16E75406-5B9B-462D-AE76-9CFA9D497869}" src="https://github.com/user-attachments/assets/3e2d9c1b-1bc7-4f03-86bc-3d4f8fe757c8" />
```
import pandas as pd
data=pd.read_csv("data 1.csv")
df=pd.DataFrame(data)
print(df.isnull().sum())
```
<img width="353" height="224" alt="image" src="https://github.com/user-attachments/assets/25417ad2-a977-41f0-acf0-63d3083929aa" />
```
import pandas as pd
data=pd.read_csv("data 1.csv")
df=pd.DataFrame(data)
drop=df.dropna()
print("Before dropna",df)
print("After dropna",drop)
```
<img width="898" height="739" alt="{44C47DB9-206C-4F4B-AA93-1648F54C1E32}" src="https://github.com/user-attachments/assets/125e4837-a5bd-4cf9-9d89-023eca7e4a5a" />
```
import pandas as pd
data=pd.read_csv("data 1.csv")
df=pd.DataFrame(data)
drop=df.dropna(axis=1)
print("Before dropna /n/n",df)
print("After dropna /n/n",drop)
```
<img width="1043" height="707" alt="{B59CC9C2-FA00-4933-8B18-61DA5B71853E}" src="https://github.com/user-attachments/assets/fc437b23-0b23-44ed-ab0f-57000cd1783a" />
```
import pandas as pd
data=pd.read_csv("data 1.csv")
df=pd.DataFrame(data)
drop=df.dropna(axis=1)
print("Before dropna /n/n",df)
print("After dropna /n/n",drop)
```
<img width="859" height="736" alt="{D0DAEFE2-CE7E-4A69-B23E-B59AAB302323}" src="https://github.com/user-attachments/assets/86e93e55-6e10-4af1-8ed6-30941b0f4750" />
```
import pandas as pd
data=pd.read_csv("data 1.csv")
df=pd.DataFrame(data)
drop=df.dropna(axis=1,inplace=True)
print("Before dropna /n/n",df)
print("After dropna /n/n",drop)
```
<img width="1005" height="335" alt="image" src="https://github.com/user-attachments/assets/5935867f-afe6-4c0a-87bc-1c1f104cb673" />
```
import pandas as pd
data=pd.read_csv("data 1.csv")
df=pd.DataFrame(data)
fill=df.fillna(method='ffill')
print(fill)
```
<img width="854" height="314" alt="{BB1CD6F6-2D06-4413-A1A9-12E39AC7D9C4}" src="https://github.com/user-attachments/assets/5eb087a0-7406-428e-a6b9-7125e24d721a" />
```
import pandas as pd
data=pd.read_csv("data 1.csv")
df=pd.DataFrame(data)
fill=df.fillna(method='bfill')
print(fill)
```
<img width="863" height="742" alt="{086A2FF5-89DE-4072-8A3F-1FAAC9074B57}" src="https://github.com/user-attachments/assets/db77b1c4-4f9c-4830-919e-7024e0ca093c" />
```
import pandas as pd
data=pd.read_csv("data 1.csv")
df=pd.DataFrame(data)
mean=df.mean()
print(mean)
```
<img width="453" height="137" alt="image" src="https://github.com/user-attachments/assets/b2c600af-72b9-4ea6-bb83-5309b3189148" />
```
import pandas as pd
data=pd.read_csv("data 1.csv")
df=pd.DataFrame(data)
median=df.median()
print(median)
```
<img width="376" height="122" alt="image" src="https://github.com/user-attachments/assets/1d3a0d71-f87c-424a-b426-168a04e39b24" />
```
import pandas as pd
data=pd.read_csv("data 1.csv")
df=pd.DataFrame(data)
mode=df.mode()
print(mode)
```
<img width="809" height="745" alt="{47575A84-A5B1-47AC-8EA7-27AF0B041E01}" src="https://github.com/user-attachments/assets/9b7a2b97-a32e-427e-847d-418f9fce26a4" />
```
 import pandas as pd
data=pd.read_csv("data 1.csv")
df=pd.DataFrame(data)
interpolate =df.interpolate()
print(interpolate)
```
<img width="1017" height="721" alt="{AE441EBA-A86E-4C11-891F-6C241EE47B09}" src="https://github.com/user-attachments/assets/fbfbcdc6-1d6f-43b0-bb0c-7c822782e316" />
```
 import pandas as pd 
import matplotlib.pyplot as plt
import numpy as np

data  = pd.read_csv("data3.csv")

df = pd.DataFrame(data)

print(df)
```
<img width="733" height="306" alt="{502EF6B1-8DF8-488C-A8C9-E03F06E4B25E}" src="https://github.com/user-attachments/assets/09c6df70-1ad7-45e1-9989-4a4936559b7b" />
```
 import pandas as pd 
import matplotlib.pyplot as plt
import numpy as np

data  = pd.read_csv("data3.csv")

df = pd.DataFrame(data)

print(df)

print(pd.descripe())
```
<img width="997" height="698" alt="{D99542E8-7C7F-461B-8856-A4A5B585CB8B}" src="https://github.com/user-attachments/assets/f40e58a4-c34b-47e6-862d-6ea7f6d16e8d" />
```
plt.bar(df["species"],df["sepal_width"])
plt.show()
```
<img width="726" height="509" alt="{F2EB54B4-368E-4E34-A760-68DE30EF0153}" src="https://github.com/user-attachments/assets/da52b10b-c652-4707-b420-872844540033" />
```
plt.scatter(df["sepal_length"],df["sepal_width"])
plt.show()
```
<img width="789" height="531" alt="{73FAB8AB-B57A-471F-A943-32F5CB40256A}" src="https://github.com/user-attachments/assets/b6e9e274-3946-4905-a458-ad44b95b818a" />
```
plt.plot(df["species"],df["sepal_length"])
plt.show()
```
<img width="843" height="478" alt="{9B99CF4A-3F05-4261-BEC8-B552C2D7B800}" src="https://github.com/user-attachments/assets/ddc319cb-4430-4293-a1ff-1852e8805f23" />
```
import pandas as pd
data=pd.read_csv("data 1.csv")
df=pd.DataFrame(data)
print(df.isnull().any())
```
<img width="516" height="247" alt="image" src="https://github.com/user-attachments/assets/bc6b318d-9653-48af-a0a2-c977b3b8b589" />

# Result
          <<include your Result here>>
