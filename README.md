# DATA-SCIENCE-PROJECT TASK-1

*COMPANY*: CODTECH IT SOLUTIONS

 *NAME*: AKSHAT JAIN

*INTERN ID*: CT04DH1930

*DOMAIN*: DATA SCIENCE

*DURATION*: 4 WEEKS

*MENTOR*: 

🛠️ Data Preprocessing Pipeline using Pandas & Scikit-Learn
✅ Task Overview
Objective:
Design and implement a modular, reusable ETL (Extract, Transform, Load) pipeline using Python, Pandas, and Scikit-Learn. The pipeline is aimed at preparing data for machine learning tasks by automating key preprocessing steps. This task focuses on developing a structured, real-world workflow that can handle data extraction, cleaning, transformation, and saving in a standardized format for future analysis or modeling.

📦 Project Description
This project demonstrates a complete data preprocessing pipeline using the popular California Housing dataset. The dataset provides information about housing in California districts and is ideal for exploring data cleaning and transformation techniques. The pipeline is implemented in Google Colab for interactive exploration and ease of execution.

The workflow includes:

📥 Extraction: Loading the dataset directly from Scikit-Learn’s built-in datasets.

🔧 Transformation: Preprocessing the data, including scaling of numerical features and handling of any potential data quality issues.

💾 Loading: Exporting the cleaned and transformed dataset to a .csv file for further use in machine learning models or external analysis tools.

🚀 Pipeline Structure
The project pipeline is structured into three modular phases, adhering to the ETL approach:

1️⃣ Extract:
Data is extracted using fetch_california_housing() from the sklearn.datasets module.

This method retrieves the dataset in the form of a Pandas DataFrame using the as_frame=True argument for easier manipulation.

2️⃣ Transform:
The transformation step involves data cleaning and feature scaling.

All numerical features in the dataset are standardized using Scikit-Learn’s StandardScaler, which ensures that the data has zero mean and unit variance.

These transformations are essential for improving the performance of many machine learning algorithms.

3️⃣ Load:
The cleaned and transformed dataset is saved to a .csv file using Pandas' to_csv() method.

This step ensures the data is preserved in a usable format for downstream machine learning models or external usage.

🧰 Technologies Used
Python 3.x – Primary programming language used for implementation.

Pandas – For data manipulation, transformation, and file export.

Scikit-Learn – For data extraction and preprocessing (feature scaling).

Google Colab – Interactive environment for running the notebook and visualizing results.


---

## 📂 File Structure
```
.
├── Data_Science_Task_1.ipynb       # Main Jupyter Notebook with complete ETL pipeline
├── README.md                       # Project overview and instructions (this file)
└── processed_data.csv              # Output file after transformation (generated)

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

# Execution Flow
df = extract_data()
df_transformed = transform_data(df)
df_transformed.to_csv("processed_data.csv", index=False)

```

---

🧠 Key Insights
Modular Functions: The use of well-structured, modular functions makes the code clean, reusable, and easy to scale for other datasets.

Efficient Preprocessing: Leveraging Scikit-Learn’s built-in preprocessing tools simplifies the task of feature scaling and ensures consistency across projects.

Real-world Readiness: The pipeline mimics real-world data engineering workflows and helps prepare data efficiently for machine learning models.

✅ How to Run
Clone or download the project repository.

Open the Data_Science_Task_1.ipynb notebook in Google Colab or any Jupyter environment.

Run all cells in sequential order to execute the ETL pipeline.

The transformed data will be saved as processed_data.csv in your workspace.

📊 Conclusion
This project represents a solid foundation in data preprocessing and pipeline creation using industry-standard tools. It emphasizes clean code, scalability, and practical skills needed in real data science workflows. By automating key data handling steps, this pipeline serves as a template for future projects requiring data cleaning and transformation.

