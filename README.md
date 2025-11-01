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

 Name:Janani Gowrisankar
 Register No:212224100022
```
 import pandas as pd
 import seaborn as sns
 import matplotlib.pyplot as plt
 df=pd.read_csv("titanic_dataset.csv")
 df.head()
```

<img width="1679" height="287" alt="image" src="https://github.com/user-attachments/assets/ab8ded44-562e-43dc-bcab-883930edbff0" />


 1.Line Plot:
```
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
```

<img width="884" height="641" alt="image" src="https://github.com/user-attachments/assets/9b2112fd-e9cc-4e82-b858-5772f6528586" />


2.Multi Line Plot:
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

<img width="813" height="644" alt="image" src="https://github.com/user-attachments/assets/a3c0c793-9614-4ccf-a6fb-5832897f884f" />


# TO VISUALIZE RELATIONSHIPS

 1.Bar Chart
 ```
 plt.figure(figsize=(8,5))
 sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
 plt.title("Fare Of Passenger By Embarked Town")
```

<img width="1019" height="679" alt="image" src="https://github.com/user-attachments/assets/9e4e17d6-b939-4503-b0d2-473865db199d" />


2.Scatter Plot
```
 sns.scatterplot(x="Age", y="Fare", data=df)
 plt.title('Scatterplot of Age vs Fare')
 plt.show()
```

<img width="960" height="663" alt="image" src="https://github.com/user-attachments/assets/1185ebfe-ae8c-4edc-bbe4-2189e8f5f47a" />


 3.Bubble Chart
 ```
 sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
 plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
 plt.show()
```

 <img width="907" height="659" alt="image" src="https://github.com/user-attachments/assets/08c6e120-0143-4982-9704-7f11824af5e8" />


# TO CAPTURE DISTRIBUTIONS

 1.Histogram
 
 ```
 sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```
 
<img width="868" height="635" alt="image" src="https://github.com/user-attachments/assets/95874732-2d86-495e-b448-360eef2ac8a8" />


  2.Box Plot
  
  ```
 sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
 plt.title("Age By Passenger Class")
```

 <img width="876" height="667" alt="image" src="https://github.com/user-attachments/assets/a65fba1d-5205-4f92-bf85-86154d7af5c0" />

 3.Violin Plot
 
 ```
 sns.violinplot(x="Pclass", y="Fare", data=df)
 plt.title('Violin Plot of Fare by Passenger Class')
 plt.show()
```

<img width="880" height="657" alt="image" src="https://github.com/user-attachments/assets/f377abea-b6e5-44e0-955c-c13ec985cb60" />


  4.Density Plot
  
  ```
 sns.kdeplot(data=df['Age'], shade=True)
 plt.title('Density Plot of Passenger Ages')
 plt.show()
```

 <img width="791" height="588" alt="image" src="https://github.com/user-attachments/assets/d78f544a-e217-4d68-994b-4c7c3af075e4" />


 5.Heatmap
 
 ```
 numeric_df = df.select_dtypes(include=['float64', 'int64'])
 corr_matrix = numeric_df.corr()
 sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
 plt.title('Heatmap of Titanic Dataset')
 plt.show()
```

<img width="920" height="680" alt="image" src="https://github.com/user-attachments/assets/a98170ad-690c-47d1-9aba-6f88ec3f9df9" />

 
# Result:
 Thus, the Data Visualization using seaborn python library for the given data is implemented successfully
