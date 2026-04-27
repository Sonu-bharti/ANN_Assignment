# 🧠 ANN Assignment – PyTorch Implementation

## 📌 Overview
This project demonstrates the implementation of **Artificial Neural Networks (ANNs)** using **PyTorch** for two core machine learning tasks:

- 🔹 **Classification** – Titanic Survival Prediction  
- 🔹 **Regression** – House Price Prediction  

It covers the complete ML pipeline:
- Data preprocessing  
- Data visualization  
- Model building (PyTorch)  
- Training & testing  
- Performance evaluation  
- Hyperparameter tuning  

---

## 📂 Project Structure
```
ANN_ASSIGNMENT/
│
├── data/
│   ├── titanic.csv
│   ├── house.csv
│
├── classification.py
├── regression.py
│
├── output/
├── outputRegression/
│
├── README.md
```

---

## 📊 Dataset Description

### 🔹 Titanic Dataset (Classification)
- **Source:** Kaggle / GitHub  
- **Features:** Age, Gender, Fare, Passenger Class, etc.  
- **Target:**  
  - `survived` → (0 = No, 1 = Yes)

---

### 🔹 House Prices Dataset (Regression)
- **Source:** Boston Housing Dataset  
- **Features:** Crime rate, number of rooms, etc.  
- **Target:**  
  - `medv` → Median house value  

---

## ⚙️ Data Preprocessing

### ✔ Steps Performed:
- Handling missing values:
  - Mean (numerical features)
  - Mode (categorical features)
- Dropping irrelevant columns  
- One-hot encoding for categorical variables  
- Feature scaling using **StandardScaler**  
- Train-test split (80% training, 20% testing)  

---

## 📈 Data Visualization

### 🔹 Classification:
- Survival count plot  
- Age distribution  
- Gender vs survival  
- Correlation heatmap  

### 🔹 Regression:
- Price distribution  
- Feature correlation heatmap  
- Actual vs predicted plot  
- Error distribution  

---

## 🧠 Model Architecture

### 🔹 Classification Model (ANN)
- Input Layer  
- Hidden Layers:
  - Dense (32) → ReLU  
  - Dense (16) → ReLU  
  - Dense (8) → ReLU  
- Output Layer:
  - Dense (1)  
- Loss Function:
  - `BCEWithLogitsLoss`

---

### 🔹 Regression Model (ANN)
- Input Layer  
- Hidden Layers:
  - Dense (32) → ReLU  
  - Dense (16) → ReLU  
- Output Layer:
  - Dense (1)  
- Loss Function:
  - `Mean Squared Error (MSE)`  

---

## 🏋️ Training Details
- **Optimizer:** Adam  
- **Epochs:** 50 / 100  
- **Batch Size:** 16 / 32  
- **Device:** CPU / GPU (if available)  

---

## 📊 Evaluation Metrics

### 🔹 Classification:
- Accuracy  
- Confusion Matrix  
- Precision, Recall, F1-score  

### 🔹 Regression:
- Mean Absolute Error (MAE)  
- Mean Squared Error (MSE)  

---

## ⚙️ Hyperparameter Tuning

| Model Setup     | Epochs | Batch Size | Layers   | Result     |
|----------------|--------|------------|----------|------------|
| Baseline       | 50     | 32         | 16-8     | Moderate   |
| More Neurons   | 50     | 32         | 32-16    | Improved   |
| More Epochs    | 100    | 32         | 32-16    | Better     |
| Smaller Batch  | 50     | 16         | 32-16    | Best       |

---

## 💾 Output Files

### 🔹 Classification Output:
- Accuracy results  
- Confusion matrix  
- Predictions CSV  
- Accuracy graph  
- Trained model (`.pt`)  

### 🔹 Regression Output:
- MAE results  
- Predictions CSV  
- Actual vs predicted plot  
- Error distribution  
- Model comparison graph  

---

## 🚀 How to Run the Project

### 🔹 Step 1: Install Dependencies
```bash
pip install torch pandas numpy matplotlib seaborn scikit-learn
```

### 🔹 Step 2: Run Classification
```bash
python classification.py
```

### 🔹 Step 3: Run Regression
```bash
python regression.py
```

---

## 📌 Key Observations
- Increasing neurons improves model performance  
- Too many epochs can lead to overfitting  
- Smaller batch sizes improve learning but increase training time  
- Proper preprocessing significantly impacts accuracy  

---

## 📚 Technologies Used
- 🐍 Python  
- 🔥 PyTorch  
- 📊 Pandas, NumPy  
- 📉 Matplotlib, Seaborn  
- 🤖 Scikit-learn  

---

## 👨‍💻 Author
**Sonu Bharti**  
B.Tech CSE  

---

## ✅ Conclusion
This project demonstrates how **Artificial Neural Networks** can effectively solve both **classification and regression problems** using PyTorch, along with proper preprocessing, evaluation, and hyperparameter tuning.
