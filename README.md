# 🚗 EV Price Prediction Using Machine Learning

This project uses **Machine Learning and Linear Regression** to analyze electric vehicle (EV) data and predict the **price of an EV based on its driving range**.

The project is developed using **Python** in a Jupyter/Google Colab Notebook. The dataset contains information about electric vehicles available in India, including their brand, model, price, range, power, and battery capacity.

---

## 📌 Project Overview

Electric vehicle price prediction is a regression problem where machine learning is used to understand the relationship between vehicle specifications and their prices.

In this project, **EV Range** is used as the input feature to predict the **Price** of the vehicle using Linear Regression.

### 🎯 Objectives

* Analyze an electric vehicle dataset
* Explore EV specifications using Python
* Check and handle missing values
* Select EV Range as the input feature
* Predict EV prices using Linear Regression
* Compare actual and predicted prices
* Evaluate model performance using regression metrics
* Visualize the prediction results

---

## 📊 Dataset

The dataset contains **26 electric vehicle records** and **6 columns**.

### Dataset Features

| Column    | Description                   |
| --------- | ----------------------------- |
| `Brand`   | Name of the EV manufacturer   |
| `Model`   | Name of the EV model          |
| `Price`   | Price of the electric vehicle |
| `Range`   | Driving range of the EV       |
| `Power`   | Motor power                   |
| `Battery` | Battery capacity              |

### Sample Data

| Brand    | Model         | Price | Range | Power | Battery |
| -------- | ------------- | ----: | ----: | ----: | ------: |
| Maruti   | SuzukieVitara | 15.99 |   440 |   142 |      49 |
| Tata     | PunchEV       |  9.69 |   275 |    87 |      30 |
| Mahindra | XEV9e         | 21.90 |   542 |   228 |      59 |
| Mahindra | BE6           | 18.90 |   557 |   228 |      59 |
| MG       | WindsorEV     | 14.00 |   332 |   134 |      38 |

---

## 🛠️ Technologies Used

* 🐍 **Python**
* 🐼 **Pandas** – Data loading and manipulation
* 🧮 **NumPy** – Numerical operations
* 📊 **Matplotlib** – Data visualization
* 📈 **Seaborn** – Data visualization
* 🤖 **Scikit-learn** – Machine Learning
* 📉 **Linear Regression** – EV price prediction
* 📓 **Google Colab / Jupyter Notebook**

---

## 🔄 Project Workflow

```text
EV Dataset
    ↓
Load Dataset
    ↓
Data Exploration
    ↓
Check Dataset Information
    ↓
Handle Missing Values
    ↓
Feature Selection
    ↓
Train-Test Split
    ↓
Linear Regression
    ↓
Generate Predictions
    ↓
Compare Actual vs Predicted Prices
    ↓
Model Evaluation
    ↓
Visualization
```

---

## 🧹 Data Preprocessing

Before training the model, the dataset is checked and prepared for analysis.

The preprocessing steps include:

1. Loading the dataset using Pandas
2. Checking the number of rows and columns
3. Inspecting data types and dataset information
4. Checking for missing values
5. Removing rows with missing values using `dropna()`
6. Selecting `Range` as the input feature
7. Selecting `Price` as the target variable

After preprocessing, the `Range` and `Price` columns contain no missing values.

---

## 🤖 Machine Learning Model

### Linear Regression

The project uses **Linear Regression** to predict the price of an electric vehicle based on its driving range.

The selected variables are:

```python
X = df[["Range"]]
y = df["Price"]
```

The dataset is divided into **training and testing data using an 80:20 split**, with `random_state=42`.

The Linear Regression model is then trained using the training dataset.

### 📐 Regression Equation

The trained model produced the following approximate equation:

```text
Price = 0.1414 × Range - 34.3961
```

Where:

* **Slope:** 0.1414
* **Intercept:** -34.3961
* **Range:** EV driving range
* **Price:** Predicted EV price

---

## 📈 Actual vs Predicted Prices

The model predictions are compared with the actual EV prices from the testing dataset.

### Example Results

| Actual Price | Predicted Price |
| -----------: | --------------: |
|        21.49 |           41.68 |
|        17.29 |           31.78 |
|        15.99 |           27.82 |
|        72.50 |           33.90 |
|         3.25 |           -9.65 |
|         7.99 |            0.96 |

These results demonstrate the difference between the actual vehicle prices and the prices predicted by the Linear Regression model.

---

## 📊 Model Evaluation

The model is evaluated using commonly used regression metrics:

* **MAE (Mean Absolute Error)**
* **MSE (Mean Squared Error)**
* **RMSE (Root Mean Squared Error)**
* **R² Score**

### Results

| Metric   |    Value |
| -------- | -------: |
| MAE      |  17.5081 |
| MSE      | 410.5502 |
| RMSE     |  20.2620 |
| R² Score |   0.2179 |

The model achieved an **R² score of approximately 0.218**. This indicates that using only **EV Range** as the predictor explains a limited portion of the variation in EV prices in this dataset.

---

## 📉 Visualization

The project includes an **Actual vs Predicted EV Prices** scatter plot.

The visualization contains:

* **X-axis:** Actual Price
* **Y-axis:** Predicted Price
* **Reference Line:** Used to visually compare actual and predicted values

This visualization helps understand how closely the model's predictions match the actual prices.

---

## 📁 Project Structure

```text
EV-Price-Prediction/
│
├── Task_ML.ipynb
├── ev_car_India_dataset.csv
└── README.md
```

---

## ▶️ How to Run the Project

### 1. Clone the Repository

```bash
git clone https://github.com/Rabinson-20/ML-Task-8.git
```

### 2. Open the Project

Open `Task_ML.ipynb` using any of the following:

* Google Colab
* Jupyter Notebook
* JupyterLab
* VS Code

### 3. Add the Dataset

Make sure the following dataset is available in the project directory:

```text
ev_car_India_dataset.csv
```

### 4. Install Required Libraries

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

### 5. Run the Notebook

Execute the notebook cells from **top to bottom** to reproduce the data analysis, model training, predictions, and evaluation results.

---

## 🚀 Future Improvements

The current model uses only **Range** to predict EV price. The model could be further developed by including additional vehicle features.

Possible improvements include:

* Battery capacity
* Motor power
* Brand
* Vehicle model
* Multiple Linear Regression
* Decision Tree Regression
* Random Forest Regression
* Categorical feature encoding
* Feature scaling
* Hyperparameter tuning

Using multiple relevant features may provide a more complete representation of EV pricing.

---

## 🎓 Learning Outcomes

Through this project, I learned how to:

* Load and inspect datasets using Pandas
* Perform basic data preprocessing
* Identify and handle missing values
* Select input and target variables
* Split data into training and testing sets
* Build a Linear Regression model
* Generate machine learning predictions
* Calculate regression evaluation metrics
* Visualize actual and predicted values
* Interpret machine learning model performance

---

## 👨‍💻 Author

**SAMRABINSON P**

BCA Student | Aspiring Full Stack Developer | Machine Learning Enthusiast
# ML-TASK-8
