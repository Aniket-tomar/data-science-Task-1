# DATA-SCIENCE-PROJECT TASK-1

*COMPANY*: CODTECH IT SOLUTIONS

 *NAME*: AKSHAT JAIN

*INTERN ID*: CT04DH1930

*DOMAIN*: DATA SCIENCE

*DURATION*: 4 WEEKS

*MENTOR*: 

# 🛠️ Data Preprocessing Pipeline using Pandas & Scikit-Learn

## ✅ Task Overview
**Objective:**  
Design and implement an **ETL pipeline (Extract, Transform, Load)** using tools like **Pandas** and **Scikit-Learn**.

**Task Prompt:**  
> *Create a pipeline for data preprocessing, transformation, and loading using tools like Pandas and Scikit-Learn.*

---

## 📦 Project Description

This project demonstrates a complete ETL (Extract-Transform-Load) pipeline using the **California Housing dataset**. It includes:

- 📥 **Extraction** from sklearn’s built-in datasets  
- 🔧 **Transformation** using preprocessing steps such as feature scaling  
- 💾 **Loading** the cleaned and transformed data for future modeling or export

---

## 🚀 Pipeline Structure

### 1️⃣ Extract
- Load housing dataset using `fetch_california_housing()`

### 2️⃣ Transform
- Clean data (e.g. handle missing values)
- Standardize numerical features using `StandardScaler`

### 3️⃣ Load
- Save the transformed dataset using `to_csv()`

---

## 🧰 Technologies Used

- Python 3.x  
- Pandas  
- Scikit-Learn  
- Google Colab (for interactive workflow)

---

## 📂 File Structure
```
.
├── Data_Science_Task_1.ipynb       # Main notebook with ETL pipeline
├── README.md                       # This file
```

---

## 📸 Sample Code Snippet
```python
from sklearn.datasets import fetch_california_housing
from sklearn.preprocessing import StandardScaler

def extract_data():
    data = fetch_california_housing(as_frame=True)
    return data.frame

def transform_data(df):
    scaler = StandardScaler()
    df[df.columns] = scaler.fit_transform(df)
    return df
```

---

## 🧠 Key Insights

- Modular functions make the pipeline reusable
- Using Scikit-Learn standard tools makes scaling and transforming easier and faster
- Pipeline is structured and commented for clarity and reusability

---

## ✅ How to Run

1. Clone this repo  
2. Open the notebook `Data_Science_Task_1.ipynb`  
3. Run all cells in order  
4. Export final CSV output if needed
