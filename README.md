# 🐼 Python Data Analysis Project (Pandas)

## 📌 Overview
This project was completed as part of a **Data Technician Bootcamp**, focusing on using **Python and the pandas library** to explore, clean, and analyse datasets.

The project demonstrates how Python can be used for **data analysis and manipulation**, particularly when working with **retail and sales datasets**. Using pandas, various techniques were applied to filter, transform, and summarise data in order to uncover useful insights.

Visualisations were also created using **built-in pandas plotting and libraries such as matplotlib** to better understand trends and patterns in the data.

---

## 🎯 Project Objective

The objective of this project was to develop practical skills in:

- Data cleaning and preparation
- Data exploration and filtering
- Data transformation and summarisation
- Visualising patterns and trends

These skills are essential for **data analysts working with real-world datasets**.

---

## 🛠️ Skills Demonstrated

- 🐼 Using **pandas** for data manipulation and analysis  
- 🔎 **Filtering and subsetting datasets**  
- 📍 Selecting data with **`.loc[]` and `.iloc[]`**  
- 🧹 **Cleaning and preparing datasets**  
- 📊 **Grouping and summarising data**  
- 📉 **Sorting and organising data**  
- 📈 **Data visualisation using pandas and matplotlib**

---

## 🧮 Data Exploration with Pandas

Pandas was used to explore the dataset and inspect its structure.

```python
import pandas as pd

df = pd.read_csv("retail_sales_data.csv")
df.head()
```

This helps quickly understand the **structure, columns, and sample records** in the dataset.

---

## 🔎 Filtering and Subsetting Data

Filtering was used to analyse specific parts of the dataset, such as sales from particular categories or regions.

```python
df[df["Sales"] > 500]
```

---

### Selecting Data with `.loc[]`

`.loc[]` was used to select rows and columns by **labels or conditions**.

```python
df.loc[df["Product Category"] == "Electronics"]
```

---

### Selecting Data with `.iloc[]`

`.iloc[]` was used to select data based on **integer positions**.

```python
df.iloc[0:5, 0:3]
```

---

## 🧹 Data Cleaning and Preparation

Several pandas methods were used to prepare the dataset for analysis.

### Handling Missing Values

```python
df.dropna()
df.fillna(0)
```

### Sorting Data

```python
df.sort_values(by="Sales", ascending=False)
```

### Grouping Data

```python
df.groupby("Product Category")["Sales"].sum()
```

These methods help ensure the dataset is **clean, organised, and ready for analysis**.

---

## 📊 Data Analysis

Pandas functions were used to summarise and analyse retail and sales performance.

Examples include:

- Calculating **total sales by product category**
- Comparing **sales across customer demographics**
- Identifying **high-performing product categories**
- Sorting and ranking products based on sales performance

These analyses help uncover **business insights from retail data**.

---

## 📈 Data Visualisation

Visualisations were created using pandas plotting and **matplotlib** to better understand patterns in the dataset.
```
import matplotlib.pyplot as plt
import seaborn as sns
```
### 💻 Sample Code and Visualisation
#### Histogram
```
df.hist(figsize=(10,8))
plt.show()
```
<img width="831" height="682" alt="image" src="https://github.com/user-attachments/assets/c4851fc0-603d-43e4-a922-4ac6c2f7923c" />

---
#### 
``` Correlation Heatmap
corr = df[["IMF_Estimate", "UN_Estimate", "WorldBank_Estimate"]].corr()

plt.figure(figsize=(9,6))
sns.heatmap(corr)

plt.show()
```
<img width="700" height="511" alt="image" src="https://github.com/user-attachments/assets/36093fa9-96b0-4e95-adf3-fe6b3a3fbe74" />

--- 
#### Bar Plot
```
sns.barplot(x="UN_Region", y="WorldBank_Estimate", data=df, errorbar=None)

plt.show()
```
<img width="589" height="433" alt="image" src="https://github.com/user-attachments/assets/c98abc01-a911-4216-b934-2d5a7768fee9" />

---
#### Scatter Plot
```
df.plot(x='UN_Region', y='UN_Estimate', kind='scatter',
        figsize=(10,6),
        title="Scatter Plot")

plt.show()
```
<img width="877" height="547" alt="image" src="https://github.com/user-attachments/assets/f31ad516-37ad-4553-aec0-5c2637cd7332" />

---
#### Box Plot and Outliers
```
sns.boxplot(x=df["UN_Estimate"])

plt.show()
```
<img width="520" height="433" alt="image" src="https://github.com/user-attachments/assets/aeb9b88f-c092-49e0-993f-f809bb9756a2" />

--- 

Charts help present findings clearly and support **data-driven decision making**.

---

## 🧰 Tools Used

- 🐍 **Python**
- 🐼 **pandas**
- 📊 **matplotlib**
- 📓 **Google Colab / Jupyter Notebook**

---


