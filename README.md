# EXNO-5-DS-DATA VISUALIZATION USING MATPLOT LIBRARY

# Aim:
  To Perform Data Visualization using matplot python library for the given datas.

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

import seaborn as sns
import matplotlib.pyplot as plt

df = sns.load_dataset("iris")
plt.figure(figsize=(8,5))
sns.histplot(df["sepal_length"], kde=True)
plt.title("Distribution of Sepal Length")
plt.show()


sns.jointplot(x="sepal_length", y="sepal_width", data=df, height=6)
plt.show()


sns.pairplot(df, hue="species")
plt.show()


plt.figure(figsize=(8,6))
sns.heatmap(df.select_dtypes(include='number').corr(), 
            annot=True, cmap="coolwarm")
plt.title("Correlation Heatmap")
plt.show()


plt.figure(figsize=(8,5))
sns.boxplot(x="species", y="petal_length", data=df)
plt.title("Boxplot of Petal Length")
plt.show()


plt.figure(figsize=(8,5))
sns.violinplot(x="species", y="petal_width", data=df)
plt.title("Violinplot of Petal Width")
plt.show()


plt.figure(figsize=(6,4))
sns.countplot(x="species", data=df)
plt.title("Count of Species")
plt.show()


plt.figure(figsize=(8,5))
sns.barplot(x="species", y="sepal_length", data=df)
plt.title("Average Sepal Length")
plt.show()

```


# Output:
<img width="687" height="468" alt="output 1" src="https://github.com/user-attachments/assets/6ec6c1b7-2243-4f0b-853d-d567634e426e" />
<img width="589" height="590" alt="output 2" src="https://github.com/user-attachments/assets/ae1fac38-f7f6-4370-9965-d10bf8d6024a" />
<img width="1112" height="986" alt="output 3" src="https://github.com/user-attachments/assets/afc42941-eab4-4d49-a47c-2aa9ba5b8f46" />
<img width="637" height="526" alt="output 4" src="https://github.com/user-attachments/assets/3c60f828-47a9-475c-91d0-6ddab3a986c1" />
<img width="678" height="468" alt="output 5" src="https://github.com/user-attachments/assets/a2ec23aa-2ab5-4772-afff-3dbfb91d01b3" />
<img width="691" height="468" alt="output 6" src="https://github.com/user-attachments/assets/a0d00388-caa5-4d9f-bad3-3823849c9a63" />
<img width="532" height="391" alt="output 7" src="https://github.com/user-attachments/assets/add1cd08-f244-4d35-94df-863b62f1dd25" />
<img width="678" height="468" alt="output 8" src="https://github.com/user-attachments/assets/faf5e508-469c-45bb-9327-95c2b621d8f4" />
