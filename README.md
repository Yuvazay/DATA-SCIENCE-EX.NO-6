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
import pandas as pd

import seaborn as sns

import matplotlib.pyplot as plt

df=pd.read_csv("titanic_dataset.csv")

df.head()

x=[1,2,3,4,5]

y=[3,6,2,7,1]

sns.lineplot(x=x,y=y)

plt.title('Line Plot')

<img width="650" height="568" alt="image" src="https://github.com/user-attachments/assets/4d39387d-2cfe-42ac-94ec-45a08de3752d" />

x=[1,2,3,4,5]

y1=[3,5,2,6,1]

y2=[1,6,4,3,8]

y3=[5,2,7,1,4]

sns.lineplot(x=x,y=y1)

sns.lineplot(x=x,y=y2)

sns.lineplot(x=x,y=y3

plt.title('Multi Line Plot')

<img width="1026" height="580" alt="image" src="https://github.com/user-attachments/assets/bc428df3-70ae-48e2-9d53-02eba2cd5f5e" />

plt.figure(figsize=(8,5))

sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')

plt.title("Fare Of Passenger By Embarked Town")


<img width="1227" height="596" alt="image" src="https://github.com/user-attachments/assets/c542ed4d-8bd7-4b92-8a82-d2393e194d18" />

sns.scatterplot(x="Age", y="Fare", data=df)

plt.title('Scatterplot of Age vs Fare')

plt.show()

<img width="1084" height="569" alt="image" src="https://github.com/user-attachments/assets/79f58346-1110-4b73-9a6b-61782bebd497" />


sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))

plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')

plt.show()


<img width="1059" height="581" alt="image" src="https://github.com/user-attachments/assets/c5c04343-ee81-40bd-a93a-9d49274e69b6" />

sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)

<img width="1002" height="567" alt="image" src="https://github.com/user-attachments/assets/1d17599e-b5e1-4d3b-961f-2587d40876e9" />

sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')

plt.title("Age By Passenger Class")

<img width="968" height="566" alt="image" src="https://github.com/user-attachments/assets/2de5de0e-1766-4ef4-951e-8868769a7344" />

sns.violinplot(x="Pclass", y="Fare", data=df)

plt.title('Violin Plot of Fare by Passenger Class')

plt.show()

<img width="1152" height="571" alt="image" src="https://github.com/user-attachments/assets/848b5ef9-13bc-488f-9974-4587fe1c24df" />


sns.kdeplot(data=df['Age'], shade=True)

plt.title('Density Plot of Passenger Ages')

plt.show()

<img width="1118" height="559" alt="image" src="https://github.com/user-attachments/assets/88db7699-b57c-4097-84e5-ecb1db8369ef" />


numeric_df = df.select_dtypes(include=['float64', 'int64'])

corr_matrix = numeric_df.corr()


sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')

plt.title('Heatmap of Titanic Dataset')

plt.show()


<img width="1002" height="602" alt="image" src="https://github.com/user-attachments/assets/41deb85f-e2f7-46ef-bbfe-943c3bcaf167" />

# Result:

Thus, the Data Visualization using seaborn python library for the given data is implemented successfully
