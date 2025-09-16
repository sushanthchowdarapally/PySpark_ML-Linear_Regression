# Linear Regression - Salary Prediction

## 📌 Project Overview
This project demonstrates how to build a **Linear Regression model** to predict the salary of a person working in the **Sales Department (Morning Session)**.  
The notebook walks through the process of data preparation, model training, evaluation, and visualization.

## 📂 Notebook Details
- **Filename:** `linear_Regresssion.ipynb`  
- **Total Cells:** 76  
- **Code Cells:** 40  
- **Markdown Cells:** 36  

The notebook is structured with explanations (Markdown cells) and corresponding implementations (Code cells).

## ⚙️ Requirements
The project uses **PySpark** for handling data and applying machine learning models.  

To install the dependencies, run:
```bash
pip install pyspark
```

Other commonly used libraries may include:
- pandas  
- numpy  
- matplotlib / seaborn (for visualization)

## 🚀 Workflow
1. **Problem Definition**  
   Predicting salary of employees based on given features.

2. **Environment Setup**  
   - Install PySpark  
   - Initialize Spark session  

3. **Data Preprocessing**  
   - Load dataset  
   - Handle missing values  
   - Feature selection & transformation  

4. **Model Building**  
   - Train Linear Regression model using Spark MLlib  
   - Split dataset into training & test sets  

5. **Model Evaluation**  
   - Evaluate performance using RMSE, MAE, and R² score  

6. **Results & Visualization**  
   - Compare predicted vs actual values  
   - Visualize trends and insights  

## 📊 Example Code Snippet
```python
from pyspark.ml.regression import LinearRegression

# Create linear regression model
lr = LinearRegression(featuresCol="features", labelCol="salary")

# Fit the model
lr_model = lr.fit(training_data)

# Evaluate
predictions = lr_model.transform(test_data)
predictions.show()
```

## 🏁 Conclusion
This notebook provides a complete pipeline for **linear regression using PySpark**, making it scalable for large datasets. It can be extended further for:
- Feature engineering  
- Hyperparameter tuning  
- Deployment as a predictive service  
