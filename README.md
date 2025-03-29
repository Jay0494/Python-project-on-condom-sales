### **README.md for Condom Sales Analysis**  

```markdown
# Condom Sales Analysis  

## 📌 Project Overview  
In this project, I analyze global condom sales data to uncover patterns, trends, and insights about consumer behavior. Using Python and key data science libraries, I explore the dataset, clean and visualize the data, and extract meaningful conclusions. After preparing the data, I exported it as a CSV file and loaded it into Power BI for further visualization and dashboard creation.  

## 📊 Dataset Description  
I worked with the **"Rich Global Condom Usage Dataset.csv"**, which contains various attributes related to condom sales worldwide. Some of the key aspects of the dataset include:  
- **Country/Region** – The location where sales were recorded.  
- **Sales Volume** – The number of condoms sold.  
- **Yearly Trends** – How sales are distributed over time.  
- **Demographics** – Possible segmentation by age, gender, or other factors.  

## 🔍 My Thought Process  

### 1️⃣ Loading and Exploring the Data  
```python
import pandas as pd 
import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt

df = pd.read_csv("Rich_Global_Condom_Usage_Dataset.csv")
pd.set_option('display.max_columns', None)
```
- I started by importing essential libraries like `pandas`, `numpy`, `seaborn`, and `matplotlib`.  
- I then loaded the dataset into a Pandas DataFrame.  
- To make sure I could see all the columns, I adjusted the display settings.  

### 2️⃣ Cleaning the Data  
```python
df.info()
df.dropna(inplace=True)  # Removing missing values if necessary
```
- I checked the data types and looked for missing values.  
- Since missing data can affect analysis, I decided to drop null values to keep the dataset clean.  

### 3️⃣ Visualizing the Data in Python  
```python
plt.figure(figsize=(10,5))
sns.histplot(df['Sales_Volume'], bins=30, kde=True)
plt.title("Distribution of Condom Sales")
plt.show()
```
- I created a histogram to see how sales are distributed.  
- I included a KDE (Kernel Density Estimation) plot to get a smoother representation of the distribution.  
- This helped me understand if there were any extreme values or common sales trends.  

### 4️⃣ Exporting Data for Power BI Visualization  
```python
df.to_csv("Cleaned_Condom_Sales.csv", index=False)
```
- After cleaning and preparing the dataset, I exported it as a CSV file named **"Cleaned_Condom_Sales.csv"**.  
- I then loaded this file into **Power BI** for further visualization and interactive dashboard creation.  
- In Power BI, I created charts and reports to better understand sales trends, regional patterns, and consumer behavior.  

### 5️⃣ Extracting Insights  
After looking at the data and visualizations, here are some key observations:  
- **Sales Distribution**: Some regions have significantly higher sales than others.  
- **Country-wise Trends**: A few countries dominate the market, while others have very low sales.  
- **Seasonality**: Sales may fluctuate based on time of year.  

## 🚀 Next Steps  
There are several ways I could extend this analysis:  
- **Predictive Modeling** – Using machine learning to predict future sales.  
- **Demographic Insights** – Analyzing which groups buy more and why.(See powerbi file)  
- **Advanced Power BI Dashboards** – Adding more interactive elements to visualize patterns effectively(See powerbi file).

  ## POWERBI DASHBOARD
  ![cd insights 1](https://github.com/user-attachments/assets/7a1db6c7-30c2-4b27-b313-965a1e2c45bd)

![cd insights 2](https://github.com/user-attachments/assets/b3e7d803-ac5b-4ff4-aac4-0dea3de5b60f)

---

🔹 *Author: Elijah*  
📅 *Date: March 2025*  
```
