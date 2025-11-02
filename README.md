# EX:6 DATA VISUALIZATION USING SEABORN LIBRARY

## Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

## EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

## Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

## Coding and Output:
```
Name: BALAJI KAMARAJ
Reg.no: 212224040043
```
```py
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
df=pd.read_csv("titanic_dataset.csv")
df.head()
```

<img width="1272" height="322" alt="image" src="https://github.com/user-attachments/assets/e5091091-eb03-4bf6-93cf-f8f745994731" />



### 1.Line Plot
```py
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
```

<img width="667" height="543" alt="image" src="https://github.com/user-attachments/assets/c220cf9b-2ab6-4fca-83a7-1a5b9af73e42" />


### 2.Multi Line Plot
```py
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title('Multi Line Plot')
```

<img width="667" height="543" alt="image" src="https://github.com/user-attachments/assets/69dd004a-fcd4-4ede-b425-d719793032c1" />



## TO VISUALIZE RELATIONSHIPS
### 1.Bar Chart
```py
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```

<img width="857" height="587" alt="image" src="https://github.com/user-attachments/assets/e7de9dd2-f593-4b1c-9a45-ea55928e9105" />


### 2.Scatter Plot
```py
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
```

<img width="713" height="568" alt="image" src="https://github.com/user-attachments/assets/b0a039db-f41a-4076-aae3-f2eddbd163af" />


### 3.Bubble Chart
```py
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()
```

<img width="713" height="568" alt="image" src="https://github.com/user-attachments/assets/85bc27b0-1fc2-49b9-bf08-9f61b473e82f" />


## TO CAPTURE DISTRIBUTIONS
### 1.Histogram
```py
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```

<img width="713" height="540" alt="image" src="https://github.com/user-attachments/assets/932d02c5-738f-4859-b3b2-e1527656ccb7" />


### 2.Box Plot
```py
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
```

<img width="702" height="568" alt="image" src="https://github.com/user-attachments/assets/a6207084-e17b-4f16-9303-6bbd61d10903" />


### 3.Violin Plot
```py
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
```

<img width="713" height="568" alt="image" src="https://github.com/user-attachments/assets/048a54e5-d55f-4c5d-b369-eb329a49659c" />


### 4.Density Plot
```py
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
```

<img width="730" height="568" alt="image" src="https://github.com/user-attachments/assets/cc9fab5e-78e5-412c-bc40-fe1c09abeb65" />


### 5.Heatmap
```py
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
```

<img width="745" height="631" alt="image" src="https://github.com/user-attachments/assets/4d8805c7-7607-47c2-be77-c5dea0d4b25b" />



## Result:
  Thus, the Data Visualization using seaborn python library for the given data is implemented successfully

