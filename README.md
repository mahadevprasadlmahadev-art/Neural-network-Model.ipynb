# 🧠 Neural Network Machine Learning Project

A machine learning project demonstrating **Neural Network Regression and Classification** using Python and Scikit-learn.

## 📌 Project Overview

This project implements two types of Neural Network models:

1. **Neural Network Regression**

   * Uses the **Boston Housing dataset**
   * Predicts house prices (`medv`)
   * Uses `MLPRegressor`
   * Tracks training and testing Mean Squared Error (MSE)
   * Performs hyperparameter tuning using `GridSearchCV`

2. **Neural Network Classification**

   * Uses the **Breast Cancer dataset**
   * Performs binary classification
   * Uses `MLPClassifier`
   * Tracks loss over epochs
   * Evaluates the model using accuracy, confusion matrix, and classification report

---

## 🛠️ Technologies Used

* Python 🐍
* NumPy
* Pandas
* Matplotlib
* Scikit-learn
* Neural Networks
* Machine Learning
* GridSearchCV

---

## 📂 Project Structure

```text
Neural-Network-Project/
│
├── neural_network_model.py
├── README.md
└── requirements.txt
```

---

# 1️⃣ Neural Network Regression

The regression model loads the Boston Housing dataset from a GitHub-hosted CSV file and separates the features from the target variable `medv`.

### Dataset

**Boston Housing Dataset**

* Input: Housing-related features
* Target: `medv`
* Train/Test split: **80% / 20%**

The data is divided using `train_test_split` with `random_state=42`.

### Feature Scaling

`StandardScaler` is used to standardize the input features before training the neural network.

### Neural Network Architecture

```text
Input Features
      ↓
Hidden Layer 1
   50 Neurons
      ↓
Hidden Layer 2
   50 Neurons
      ↓
Output
House Price
```

The regression model uses:

* `MLPRegressor`
* 2 hidden layers
* 50 neurons per hidden layer
* ReLU activation
* Adam optimizer
* 100 manually controlled epochs

These settings are defined in the uploaded project.

### Model Evaluation

The project calculates:

* Training MSE
* Testing MSE
* Training R² score
* Testing R² score

It also generates a **Train vs Test Loss graph**.

---

# 2️⃣ Hyperparameter Tuning

`GridSearchCV` is used to find better neural network parameters.

The project tests:

```python
hidden_layer_sizes:
(50,)
(50,50)
(100,)

activation:
relu
tanh

learning_rate_init:
0.001
0.01
```

The best model is selected using **3-fold cross-validation** and negative Mean Squared Error as the scoring metric.

---

# 3️⃣ Neural Network Classification

The classification section uses Scikit-learn's built-in **Breast Cancer dataset**.

### Dataset

The target is binary:

```text
0 → Malignant
1 → Benign
```

The dataset is split into:

* 80% Training data
* 20% Testing data

The features are standardized using `StandardScaler`.

### Neural Network Architecture

```text
Input Features
      ↓
Hidden Layer 1
   50 Neurons
      ↓
Hidden Layer 2
   50 Neurons
      ↓
Output
Binary Class
```

The classifier uses:

* `MLPClassifier`
* 2 hidden layers
* 50 neurons per hidden layer
* ReLU activation
* Adam optimizer
* 100 epochs

---

## 📊 Classification Evaluation

The model evaluates its predictions using:

* Accuracy
* Confusion Matrix
* Classification Report
* Loss vs Epoch graph

---

## 🚀 How to Run the Project

### Step 1: Clone the repository

```bash
git clone https://github.com/YOUR-USERNAME/Neural-Network-Project.git
```

### Step 2: Open the project

```bash
cd Neural-Network-Project
```

### Step 3: Install dependencies

```bash
pip install numpy pandas matplotlib scikit-learn
```

### Step 4: Run the Python file

```bash
python neural_network_model.py
```

---

## 📦 Requirements

Create a `requirements.txt` file:

```text
numpy
pandas
matplotlib
scikit-learn
```

Install them using:

```bash
pip install -r requirements.txt
```

---

## 📈 Project Results

The project produces:

### Regression

* Train vs Test MSE loss graph
* Train R² score
* Test R² score
* Best hyperparameters
* Best model Test MSE
* Best model Test R²

### Classification

* Neural Network loss graph
* Accuracy
* Confusion Matrix
* Classification Report

---

## 🎯 Learning Objectives

Through this project, you can learn:

* How Neural Networks work with tabular data
* Regression using `MLPRegressor`
* Classification using `MLPClassifier`
* Feature scaling
* Train-test splitting
* Model evaluation
* Loss tracking across epochs
* Hyperparameter tuning
* Grid Search
* Confusion Matrix and Classification Report

---

## 👨‍💻 Author

**Mahadev Prasad L**

🎓 Artificial Intelligence & Data Science Student
🏫 Maharaja Institute of Technology Thandavapura
📚 3rd Year – 5th Semester
🎓 VTU Student

---

## ⭐ Acknowledgement

This project was developed for learning and demonstrating **Neural Network-based Machine Learning techniques using Python and Scikit-learn**.

If you find this project useful, consider giving the repository a ⭐.
