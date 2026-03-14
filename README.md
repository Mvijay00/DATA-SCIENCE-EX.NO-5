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
import pandas as pd
import matplotlib.pyplot as plt

# STEP 1: Include the necessary Library (already done above)

# STEP 2: Read the Data
def read_data(filename):
    """Reads a CSV file and returns a DataFrame."""
    return pd.read_csv(filename)

# STEP 3 & 4: Visualization Functions
def plot_histogram(data, column, bins=10):
    """Draws a histogram for a numeric column."""
    plt.figure(figsize=(8,5))
    plt.hist(data[column], bins=bins, alpha=0.7, color='blue', edgecolor='black')
    plt.title(f'Histogram of {column}')
    plt.xlabel(column)
    plt.ylabel('Frequency')
    plt.show()

def plot_boxplot(data, column):
    """Draws a boxplot for a numeric column."""
    plt.figure(figsize=(6,5))
    plt.boxplot(data[column], patch_artist=True)
    plt.title(f'Boxplot of {column}')
    plt.ylabel(column)
    plt.show()

def plot_scatter(data, x_col, y_col):
    """Draws a scatter plot between two numeric columns."""
    plt.figure(figsize=(8,5))
    plt.scatter(data[x_col], data[y_col], alpha=0.6, color='green')
    plt.title(f'Scatter Plot of {x_col} vs {y_col}')
    plt.xlabel(x_col)
    plt.ylabel(y_col)
    plt.show()

def plot_bar(data, category_col):
    """Draws a bar plot for a categorical column."""
    plt.figure(figsize=(8,5))
    data[category_col].value_counts().plot(kind='bar', color='purple')
    plt.title(f'Bar Plot of {category_col}')
    plt.xlabel(category_col)
    plt.ylabel('Count')
    plt.show()

def plot_pie(data, category_col):
    """Draws a pie chart for a categorical column."""
    plt.figure(figsize=(6,6))
    data[category_col].value_counts().plot(kind='pie', autopct='%1.1f%%')
    plt.title(f'Pie Chart of {category_col}')
    plt.ylabel('')
    plt.show()

# STEP 5: Use the functions as needed (example below, update columns as appropriate)
if __name__ == "__main__":
    df = read_data('bmi.csv')  # Use any available CSV file
    plot_histogram(df, 'Height', bins=12)
    plot_boxplot(df, 'Weight')
    plot_scatter(df, 'Height', 'Weight')
    plot_bar(df, 'Gender')
    plot_pie(df, 'Gender')
```

# Result:

<img width="1087" height="590" alt="Screenshot 2025-10-07 215219" src="https://github.com/user-attachments/assets/d3f330db-66cd-4132-9768-ce9135b802ed" />
<img width="1081" height="565" alt="Screenshot 2025-10-07 215228" src="https://github.com/user-attachments/assets/6688c019-bcd1-4587-827d-da683f77f233" />
<img width="1121" height="574" alt="Screenshot 2025-10-07 215236" src="https://github.com/user-attachments/assets/6a72e52e-3df6-4b42-9073-e5163378603d" />
<img width="1247" height="607" alt="Screenshot 2025-10-07 215245" src="https://github.com/user-attachments/assets/70af8610-cd4f-4ee0-93f5-2eb09c66d531" />
<img width="806" height="610" alt="Screenshot 2025-10-07 215253" src="https://github.com/user-attachments/assets/853ad6a6-5b02-468c-b767-6b6d07ba8a61" />





