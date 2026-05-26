# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

# Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:
```
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
df=pd.read_csv("titanic_dataset.csv")
df.head()
```

<img width="1109" height="189" alt="image" src="https://github.com/user-attachments/assets/57d98fba-8ab0-4159-8821-e78e4e83db5d" />


```
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
```

<img width="668" height="528" alt="image" src="https://github.com/user-attachments/assets/3ebfaa4d-f61f-4dc5-86d5-2634ca85a92d" />


```
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title('Multi Line Plot')
```

<img width="674" height="525" alt="image" src="https://github.com/user-attachments/assets/99991cb0-7d30-486b-bfa1-8031acfc3ffe" />


```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```

<img width="791" height="559" alt="image" src="https://github.com/user-attachments/assets/fbb54eef-12b5-427a-9173-b072a5a28bb3" />


```
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
```

<img width="707" height="516" alt="image" src="https://github.com/user-attachments/assets/cb45cc3d-9e9a-48b1-8e7f-805c8363016f" />


```
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()
```

<img width="687" height="523" alt="image" src="https://github.com/user-attachments/assets/94f45906-95d8-4586-9f10-d6b7cb0649e4" />


```
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```

<img width="726" height="527" alt="image" src="https://github.com/user-attachments/assets/31762940-cd3b-479f-a596-c5d9853b1365" />


```
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
```

<img width="720" height="554" alt="image" src="https://github.com/user-attachments/assets/a03858d1-58c6-48fd-aa77-ba32fc6d873f" />


```
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
```

<img width="785" height="516" alt="image" src="https://github.com/user-attachments/assets/7c6a9a4a-f74c-43e3-b06e-925ccc96f28b" />


```
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
```

<img width="717" height="521" alt="image" src="https://github.com/user-attachments/assets/3c9d7f7c-580d-431f-bdb6-863f9c029aab" />


```
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
```

<img width="777" height="567" alt="image" src="https://github.com/user-attachments/assets/2fb7f956-8103-4e4c-a8d6-a860ae64356b" />

# Result:
 Thus, the Data Visualization using seaborn python library for the given data is implemented successfully
