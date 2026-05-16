# 🚘 Cars Data Analysis Using Python Pandas

## 📌 Project Introduction

This project is based on performing data analysis and preprocessing operations on an automobile dataset using Python and the Pandas library inside Jupyter Notebook. The dataset contains information about various cars including their manufacturer, origin, mileage, engine details, cylinders, weight, horsepower, and fuel efficiency.

The primary goal of this project is to understand how Python and Pandas are used in real-world data analytics for cleaning, exploring, and manipulating structured datasets efficiently.

In this project, different data analysis techniques were implemented such as:

- Data Cleaning
- Handling Missing Values
- Data Filtering
- Counting Unique Records
- Removing Unnecessary Data
- Applying Functions on Columns
- Exploratory Data Analysis (EDA)

This project provides practical exposure to working with datasets and understanding how data scientists preprocess and analyze data before generating insights.

---

# 📂 Dataset Information

The dataset contains details about different car models and their specifications.

### Dataset Features:

- Make
- Model
- Type
- Origin
- DriveTrain
- MSRP
- Invoice
- EngineSize
- Cylinders
- Horsepower
- MPG_City
- MPG_Highway
- Weight
- Wheelbase
- Length

Each record in the dataset represents details of a specific automobile.

---

# 🛠️ Tools & Technologies Used

## 🐍 Python
Python was used as the programming language for performing data analysis tasks and dataframe operations.

## 📊 Pandas
Pandas library was used for:
- Data Cleaning
- Data Manipulation
- Handling Missing Values
- Filtering Data
- Statistical Analysis
- Applying Functions

## 📓 Jupyter Notebook
Jupyter Notebook was used to execute Python code interactively and visualize outputs step-by-step.

---

# 🔍 Pandas Functions Implemented

## 🔹 import pandas as pd
Used to import the Pandas library.

### Syntax:
```python
import pandas as pd
```

---

## 🔹 pd.read_csv()
Used to import the CSV dataset into Jupyter Notebook.

### Syntax:
```python
df = pd.read_csv("Cars_data.csv")
```

---

## 🔹 head()
Displays the first 5 rows of the dataset.

### Syntax:
```python
df.head()
```

---

## 🔹 shape
Shows the total number of rows and columns in the dataset.

### Syntax:
```python
df.shape
```

---

## 🔹 isnull().sum()
Detects missing/null values from each column.

### Syntax:
```python
df.isnull().sum()
```

---

## 🔹 fillna()
Used to replace null values with a specific value such as mean.

### Syntax:
```python
df['Cylinders'] = df['Cylinders'].fillna(df['Cylinders'].mean())
```

---

## 🔹 value_counts()
Displays unique values along with their occurrence count.

### Syntax:
```python
df['Make'].value_counts()
```

---

## 🔹 isin()
Filters records containing specific values.

### Syntax:
```python
df[df['Origin'].isin(['Asia', 'Europe'])]
```

---

## 🔹 apply()
Applies a function on dataframe columns.

### Syntax:
```python
df['MPG_City'] = df['MPG_City'].apply(lambda x: x + 3)
```

---

# 📊 Tasks Performed in the Project

## ✅ Q1) Data Cleaning

### Task:
Find all null values in the dataset and fill them with the mean value of that column.

### Code Used:
```python
df.isnull().sum()

df['Cylinders'] = df['Cylinders'].fillna(df['Cylinders'].mean())
```

### Explanation:
- Missing values were identified using `isnull().sum()`
- Null values in numerical columns were replaced with the mean value
- This improves data quality and avoids errors during analysis

---

# 📊 Q2) Value Counts Analysis

### Task:
Check the different types of car manufacturers and count their occurrences.

### Code Used:
```python
df['Make'].value_counts()
```

### Explanation:
- Displays all unique car brands
- Shows how many times each manufacturer appears
- Helps identify the most common car companies in the dataset

---

# 📊 Q3) Filtering Records

### Task:
Display all records where Origin is Asia or Europe.

### Code Used:
```python
df[df['Origin'].isin(['Asia', 'Europe'])]
```

### Explanation:
- Filters records based on continent/region
- Displays only Asian and European cars
- Simplifies regional analysis

---

# 📊 Q4) Removing Unwanted Records

### Task:
Remove all records where Weight is greater than 4000.

### Code Used:
```python
df = df[df['Weight'] <= 4000]
```

### Explanation:
- Removes heavy vehicles from the dataset
- Keeps only cars with acceptable weight range
- Makes the dataset more focused for analysis

---

# 📊 Q5) Applying Function on Column

### Task:
Increase all values of MPG_City column by 3.

### Code Used:
```python
df['MPG_City'] = df['MPG_City'].apply(lambda x: x + 3)
```

### Explanation:
- `apply()` function was used to modify column values
- Increased city mileage values by 3
- Demonstrates how functions can be applied to dataframe columns

---

# 📌 Important Insights

✔️ Missing values can be handled efficiently using Pandas functions.

✔️ Data filtering helps in region-specific analysis.

✔️ Value counting helps identify the most frequent car manufacturers.

✔️ Unwanted records can be removed easily using conditional filtering.

✔️ Functions can be applied dynamically on dataframe columns using `apply()`.

✔️ Pandas makes data preprocessing simple and efficient.

---

# 📁 Project Structure

```text
├── Cars_Data_Analysis.ipynb
├── Cars_data.csv
├── README.md
```

---

# 🎯 Final Conclusion

This project demonstrates how Python and Pandas can be used for real-world automobile data analysis and preprocessing tasks. Different operations such as handling null values, filtering records, removing unnecessary data, analyzing value counts, and applying functions on dataframe columns were successfully implemented.

Through this project, practical understanding was gained in:

- Data Cleaning
- Exploratory Data Analysis (EDA)
- Data Manipulation using Pandas
- Handling Real-world Datasets
- Python-based Data Analytics

Overall, this project serves as a strong beginner-friendly foundation for learning Data Analysis and Data Science using Python.
