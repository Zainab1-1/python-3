import pandas as pd
df= pd.read_csv("C:\\Users\\HP\\Downloads\\folder.py\\folder.py\\New folder\\dataaaaaa.csv")

df.shape
df.info()
# Data cleaning
df.dropna()
df.dropna(inplace=True)
# Replace empty values
df.fillna(45)
# Replace a specefic columns
df['Sub_Category'].fillna(999)
df['Online_Sales_Percentage'].mean() 

df['Online_Sales_Percentage'].fillna(999)

df['Online_Sales_Percentage'].std()
df['Online_Sales_Percentage'].median()# middle value
# Fixing wrong data
df['Online_Sales_Percentage']
df.loc[2,'Online_Sales_Percentage']=65457
# Data duplications
df.duplicated()
pd.set_option("display.max_rows",None)
pd.set_option("display.max_columns",None)
df.duplicated()
# df.drop_duplicates()
df.describe()
# Adding a new column in data frame
df['col']=9
df
# Remove a column
df.drop(columns=['col'],inplace=True)
df
# Adding a row
a=pd.DataFrame({' University':100,
                'Country':'Pakistan',
                  'city':'Lahore'},
                  index=[0])
a
df=pd.concat([a,df])
df
# Removing a row
df.drop(0,inplace=True)
df
# slicing
df[2:5]
df[3:6:5]
df['Sub_Category'][45:56]
# Flow chaert
df['Sub_Category'].value_counts().plot(kind="bar")
df['Sub_Category'].value_counts().plot(kind="bar")
df['Sub_Category'].value_counts().plot(kind="box")
df['Sub_Category'].value_counts().plot(kind="density")
# pie
df['Sub_Category'].value_counts().plot(kind="pie")
# Data preprocessing
df.isnull().sum() 
df.rename(columns={'University': 'Uni'}, inplace=True)

df.dropna(axis=1)
# data agregation
df.aggregate(['sum', 'min'])
df.aggregate({"Month":['sum', 'min'], 
              "Online_Sales_Percentage":['max', 'min'], 
             }) 
df = pd.read_csv("C:\\Users\\HP\Downloads\\folder.py\\folder.py\\New folder\\dataaaaaa.csv")
df
df.to_excel("newdata.xlsx", sheet_name="newsheet")
pip install openpyxl# python-3
