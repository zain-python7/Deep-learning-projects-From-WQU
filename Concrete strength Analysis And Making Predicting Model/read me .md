# Concrete Strength Prediction using PyTorch

## Project Overview

This project implements a **Multilayer Perceptron (MLP)** model in PyTorch to predict the compressive strength of concrete based on various input features. The dataset used is the [Concrete Compressive Strength Data Set](https://archive.ics.uci.edu/ml/datasets/concrete+compressive+strength).

---

## What’s in this project?

- **Data Loading & Preprocessing:**  
  - Load the concrete dataset from CSV using Pandas.  
  - Separate input features and target variable.  
  - Split data into training and testing sets using `train_test_split`.  
  - Standardize input features using `StandardScaler` to improve training stability.

- **Model Definition:**  
  - Defined a custom `ConcreteMLP` class inheriting from `torch.nn.Module`.  
  - Used fully connected layers with ReLU activations.

- **Training Loop:**  
  - Trained the model for 300 epochs using Mean Squared Error loss (`nn.MSELoss`).  
  - Used the Adam optimizer for efficient parameter updates.  
  - Recorded and printed training loss every 50 epochs.

- **Tensor Conversion:**  
  - Converted NumPy arrays to PyTorch tensors for model compatibility.

---

## How to run

1. Make sure you have Python 3.x installed with the following libraries:  
   - `pandas`  
   - `numpy`  
   - `torch` (PyTorch)  
   - `scikit-learn`

2. Place the dataset file `Concrete_Data.csv` in the project directory.

3. Run the main script to train the model:  
   ```bash
   python train_concrete_mlp.py
