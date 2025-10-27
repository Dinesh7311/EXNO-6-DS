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

NAME: DINESH S

REGISTER NO: 212224240038

# Coding and Output:


 import pandas as pd
 
 import seaborn as sns
 
 import matplotlib.pyplot as plt
 
 df=pd.read_csv("titanic_dataset.csv")
 
 df.head()

 <img width="815" height="135" alt="image" src="https://github.com/user-attachments/assets/34d63c72-f71d-453f-90d4-52b9f6ef3755" />

  1.Line Plot:

  x=[1,2,3,4,5]
  
  y=[3,6,2,7,1]
  
  sns.lineplot(x=x,y=y)
  
  plt.title('Line Plot')

  <img width="447" height="384" alt="image" src="https://github.com/user-attachments/assets/44077066-1e0e-4b55-aba5-1eb4b2273aa6" />


 2.Multi Line Plot:

 x=[1,2,3,4,5]
 
 y1=[3,5,2,6,1]
 
 y2=[1,6,4,3,8]
 
 y3=[5,2,7,1,4]
 
 sns.lineplot(x=x,y=y1)
 
 sns.lineplot(x=x,y=y2)
 
 sns.lineplot(x=x,y=y3)

 plt.title('Multi Line Plot')


 <img width="455" height="372" alt="image" src="https://github.com/user-attachments/assets/aae7edeb-a842-43a8-98af-878f1d39a1e7" />

 TO VISUALIZE RELATIONSHIPS
 
 1.Bar Chart

 plt.figure(figsize=(8,5))
 
 sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')

 plt.title("Fare Of Passenger By Embarked Town")

 <img width="575" height="414" alt="image" src="https://github.com/user-attachments/assets/2a21388d-edf6-493a-b7c5-06d1599b846f" />


 2.Scatter Plot
 
 sns.scatterplot(x="Age", y="Fare", data=df)
 
 plt.title('Scatterplot of Age vs Fare')
 
 plt.show()

 <img width="536" height="382" alt="image" src="https://github.com/user-attachments/assets/7e616ef7-16d0-423e-a39a-e0761846e32e" />

  3.Bubble Chart
  
 sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
 
 plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
 
 plt.show()

 <img width="532" height="378" alt="image" src="https://github.com/user-attachments/assets/b2a3991a-da60-47ec-97d1-eb8bb270ee05" />

  TO CAPTURE DISTRIBUTIONS
  
 1.Histogram
 
 sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)

 <img width="515" height="392" alt="image" src="https://github.com/user-attachments/assets/51dcc4c3-c86d-4e54-bee8-513487bbb036" />

  2.Box Plot
  
 sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
 
 plt.title("Age By Passenger Class")

 <img width="492" height="403" alt="image" src="https://github.com/user-attachments/assets/14ded5b9-57f1-42f2-bf98-6fe36179f7c1" />

 3.Violin Plot
 
 sns.violinplot(x="Pclass", y="Fare", data=df)
 
 plt.title('Violin Plot of Fare by Passenger Class')
 
 plt.show()

 <img width="480" height="391" alt="image" src="https://github.com/user-attachments/assets/b095e65d-4c8e-43db-a8a0-cd5524d763c7" />

  4.Density Plot
  
 sns.kdeplot(data=df['Age'], shade=True)
 
 plt.title('Density Plot of Passenger Ages')
 
 plt.show()

 <img width="560" height="476" alt="image" src="https://github.com/user-attachments/assets/d6c49d8d-da66-4571-b742-6e0c43e009f4" />

 5.Heatmap
 
 numeric_df = df.select_dtypes(include=['float64', 'int64'])
 
 corr_matrix = numeric_df.corr()
 
 sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
 
 plt.title('Heatmap of Titanic Dataset')
 
 plt.show()

 <img width="511" height="430" alt="image" src="https://github.com/user-attachments/assets/5e908cf8-e351-4b07-8385-91b260912352" />

 
# Result:
 Thus, the Data Visualization using seaborn python library for the given data is implemented successfully
