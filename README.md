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
 from google.colab import drive
drive.mount('/content/drive')

ls drive/MyDrive/Colab Notebooks/

import pandas as pd
import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y1 = [3, 5, 2, 6, 1]
y2 = [1, 6, 4, 3, 8]
y3 = [5, 2, 7, 1, 4]

plt.figure(figsize=(8, 5))
sns.lineplot(x=x, y=y1, label='y1', marker='o')
sns.lineplot(x=x, y=y2, label='y2', marker='o')
sns.lineplot(x=x, y=y3, label='y3', marker='o')
plt.title('Line Plot')
plt.xlabel('X-axis')
plt.ylabel('Y-axis')
plt.legend()
plt.show()


![Screenshot 2024-12-25 162832](https://github.com/user-attachments/assets/d87c63a7-b722-4fd4-b553-eab8cfcf36d4)

tips = sns.load_dataset('tips')

plt.figure(figsize=(8, 5))
sns.barplot(x='day', y='total_bill', data=tips, hue='sex', palette='coolwarm')
plt.title('Total Bill by Day and Gender')
plt.xlabel('Day')
plt.ylabel('Total Bill')
plt.show()


![Screenshot 2024-12-25 162842](https://github.com/user-attachments/assets/f2c40115-e9ed-4a52-bb59-da534fc76e5a)

tit = pd.read_csv("/content/drive/MyDrive/Colab Notebooks/titanic_dataset.csv")

# Bar plot: Fare by Embarked Town
plt.figure(figsize=(8, 5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow')
plt.title('Fare of Passenger by Embarked Town')
plt.xlabel('Embarked Town')
plt.ylabel('Fare')
plt.show()


![Screenshot 2024-12-25 162850](https://github.com/user-attachments/assets/24e25253-ae8e-4325-8caa-cf57948c1e93)

plt.figure(figsize=(8, 5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow', hue='Pclass')
plt.title('Fare of Passenger by Embarked Town, Divided by Class')
plt.xlabel('Embarked Town')
plt.ylabel('Fare')
plt.legend(title='Pclass')
plt.show()


![Screenshot 2024-12-25 162901](https://github.com/user-attachments/assets/b7f3fe5d-69da-4af8-a89f-fa8dc73a1ac9)

plt.figure(figsize=(8, 5))
sns.scatterplot(x='total_bill', y='tip', data=tips)
plt.xlabel('Total Bill')
plt.ylabel('Tip Amount')
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
plt.show()


![Screenshot 2024-12-25 162909](https://github.com/user-attachments/assets/48a71ee8-8090-4810-8eec-c40e02e11958)

plt.figure(figsize=(8, 5))
sns.violinplot(x='Sex', y='Age', data=tit, palette='muted')
plt.title('Violin Plot of Age by Gender')
plt.xlabel('Gender')
plt.ylabel('Age')
plt.show()


![Screenshot 2024-12-25 162917](https://github.com/user-attachments/assets/898d41b5-2328-497d-9f4b-82597d24de22)

np.random.seed(0)
marks = np.random.normal(loc=70, scale=10, size=100)

plt.figure(figsize=(8, 5))
sns.histplot(marks, kde=True, color='blue', bins=15)
plt.title('Histogram of Marks with KDE')
plt.xlabel('Marks')
plt.ylabel('Frequency')
plt.show()


![Screenshot 2024-12-25 162931](https://github.com/user-attachments/assets/ecd5342c-6849-4337-ab28-3fd4f0246de9)


plt.figure(figsize=(8, 5))
sns.histplot(data=tit, x='Pclass', hue='Survived', kde=True, palette='Set2')
plt.title('Histogram of Pclass with Survival Hue')
plt.xlabel('Passenger Class')
plt.ylabel('Frequency')
plt.show()

![Screenshot 2024-12-25 162941](https://github.com/user-attachments/assets/392d1a54-5370-4184-b141-5b86c5990a00)

# Result:
 Include your result here
