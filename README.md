# Arabic Handwritten Digits Recognition

An end-to-end machine learning system for recognizing **Arabic handwritten digits (0–9)**.  
The project covers the full ML pipeline—from image preprocessing and feature extraction, through model comparison and hyperparameter tuning, to final evaluation and **web deployment using Flask**.

---

## 📌 Project Overview

Handwritten digit recognition is a classic computer vision and machine learning problem.  
This project focuses on **Arabic handwritten digits**, applying traditional machine learning techniques combined with handcrafted features to achieve reliable classification performance.

The system:
- Processes raw digit images
- Extracts informative features
- Trains and compares multiple ML models
- Tunes hyperparameters for optimal performance
- Deploys the best model as a web application

---

## 📋 Pipeline Summary

| Step | Description |
|------|------------|
| 0 | Configuration → Set project name, data paths, image settings |
| 1 | Image Loading → Load and preprocess images |
| 2 | Feature Extraction → HOG, LBP, and color-based features |
| 3 | Dataset Split → Train / Validation / Test with scaling |
| 4 | Model Training → Compare 10 machine learning models |
| 5 | Hyperparameter Tuning → Grid Search & Manual tuning |
| 6 | Final Evaluation → Test metrics & confusion matrix |
| 7 | Model Saving → Export best model |
| 8 | Web Deployment → Flask web app with browser UI |

---

## 🧠 Feature Extraction

The following handcrafted features are used to represent digit images:

- **HOG (Histogram of Oriented Gradients)**  
  Captures edge and shape information.
  
- **LBP (Local Binary Patterns)**  
  Extracts texture patterns useful for digit structure.
  
- **Color / Intensity Features**  
  Encodes pixel-level intensity distributions.

All features are concatenated and scaled before model training.

---

## 🤖 Models Compared

The project evaluates **10 machine learning models**, including:

- Logistic Regression
- Linear SVM
- Kernel SVM
- k-Nearest Neighbors (KNN)
- Decision Tree
- Random Forest
- Naive Bayes
- Gradient Boosting
- AdaBoost
- Extra Trees

Models are compared using **validation accuracy**, and the best-performing ones are further tuned.

---

## 🔧 Hyperparameter Tuning

Hyperparameter tuning is performed using:
- Manual tuning
- Grid Search
- Random Search

Example tuned parameters:
- `C` for Linear SVM
- Number of neighbors for KNN
- Tree depth and estimators for ensemble models

The best hyperparameters are selected based on **validation performance**.

---

## 📊 Evaluation

Final evaluation is done on a **held-out test set** using:

- Accuracy
- Confusion Matrix
- Per-class performance analysis

Example result:
- **Linear SVM Accuracy:** ~82%
- Strong diagonal dominance in the confusion matrix, indicating reliable predictions for most digits.

---

## 🌐 Web Deployment

The trained model is deployed using **Flask**.

### Web App Features:
- Upload an image of a handwritten digit
- Automatic preprocessing
- Real-time digit prediction
- Simple browser-based UI

This allows easy interaction with the trained model without running code manually.

---

## 🗂 Project Structure

