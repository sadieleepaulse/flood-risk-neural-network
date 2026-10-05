# 🌍Flood Risk Prediction Using Neural Networks

## Project Overview

This project uses Deep Learning to predict flood risk in rural areas using environmental and climate-related data.

A feedforward neural network was developed using TensorFlow and Keras to classify whether an area is at risk of flooding. The model is evaluated using **accuracy** and **precision**, with a particular focus on precision due to the importance of reliable flood-risk predictions. 

The goal is to support data-driven decision-making for non-profit organizations involved in climate risk management and emergency response planning.

---

## 🎯Objectives

- Load and explore flood risk data
- Reprocess data for neural network training
- Build a feedforward neural network using Keras
- Predict flood risk as a binary classification problem
- Evaluate model performance using precision
- Analyze model effectiveness and potential limitations
- Recommend strategies for improving performance

---

## 🛠️Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- TensorFlow
- Keras

---

## 📁Repository Structure
```text
flood-risk-neural-network/
│
├── flood_dataset.csv
├── flood-risk-prediction.ipynb
├── requirements.txt
├── README.md
│
└── screenshots/
├── model-summary.png
└── training-results.png
```

---

## 📊Dataset

The dataset contains historical environmental and flood-related indicators used to predict flood risk. 

### Target Variable

```text
FloodRisk
```

Where:

```text
0 = Low Risk
1 = High Risk
```

---

## ⚙️Data Preprocessing

Before training the neural network, the following preprocessing steps were performed:

- Loaded the dataset using Pandas
- Checked for missing values
- Separated features and target variable
- Split the data into training and testing sets
- Standardized numerical features using StandardScaler

Feature scaling was applied to improve neural network performance and training stability. 

---

## 🧠Neural Network Architecture

A feedforward neural network was created using TensorFlow and Keras.

### Architecture

```text
Input Layer
↓
Hidden Layer (16 Neurons, ReLU)
↓
Hidden Layer (8 Neurons, ReLU)
↓
Output Layer (1 Neuron, Sigmoid)
```

### Activation Functions

#### ReLU

Used in the hidden layers to learn complex patterns within the dataset.

#### Sigmoid

Used in the output layer because flood risk prediction is a binary classification problem. 

---

## 📸Model Architecture

Screenshot of the Keras model summary:

<img width="1068" height="394" alt="model-summary" src="https://github.com/user-attachments/assets/34c1ff15-c664-40e8-bdc4-56990714f013" />

```text
screenshots/model-summary.png
```

---

## 📈Results

### Model Performance 
| Metric | Score |
|----------|----------|
| Accuracy | 0.65% |
| Precision | 0.67% |

### Interpretation 

The neural network was evaluated using both accuracy and precision.

- **Accuracy** measures the overall percentage of correct predictions.
- **Precision** measures how many areas predicted as high flood risks were actually high-risk areas.

A higher precision score indicates that positive flood-risk predictions are more reliable. 

---

## 💎Why Precision Matters

Precision is calculated as:

```text
Precision = True Positives / (True Positives + False Positives)
```

In flood-risk forecasting, a false positive occurs when an area is predicted to be at high risk of flooding when it is not.

Low precision may lead to: 

- Unnecessary emergency planning
- Misallocation of limited resources
- Increased operational costs
- Reduced efficiency in disaster response efforts

A high precision score helps ensure that aid, funding, and emergency resources are directed to communities that genuinely require assistance.

---

## 🌱Real-World Impact

Flood prediction models can help organizations:

- Identify vulnerable communities
- Improve disaster preparedness
- Support emergency response planning
- Allocate resources more efficiently
- Reduce the impact of natural disasters

Using Deep Learning techniques allows organizations to make more informed decisions and better support communities at risk. 

---

## 🚀Potential Improvements

If precision is low, the following approaches may improve model performance:

### 1. Hyperparameter Tuning

Optimize model settings such as:

- Number of hidden layers
- Number of neurons
- Learning rate
- Batch size
- Number of epochs

### 2. Handle Class Imbalance

Flood events may be less common than non-flood events.

Potential solutions include:

- SMOTE
- Oversampling minority class
- Undersampling majority class
- Applying class weights during training

These approaches can help the neural network better identify flood-risk patterns. 

---

## ⚠️Model Limitation

Neural networks require sufficient data to learn meaningful patterns. 

If the dataset is small or does not adequately represent real-world flood scenarios, the model may struggle to generalize to new data.

---

## 🔮Future Enhancements

- Compare performance with Random Forest models
- Apply advanced hyperparameter tuning
- Use Cross Validation
- Generate ROC and Precision-Recall Curves
- Build an interactive dashboard using Streamlit
- Visualize predictions using Power BI
- Deploy the model as a web application

---

## 📚Requirements

Install the required dependencies:

```bash
pip install -r requirements.txt
```

### requirements.txt

```txt
pandas
numpy
scikit-learn
tensorflow
```

---

## ▶️Running the Project

Run the Python script:

```bash
python flood-risk-prediction.ipynb
```

The program will:

1. Load the dataset
2. Preprocess the data
3. Train the neural network
4. Generate predictions
5. Calculate evaluation metrics
6. Display model performance results
