# Home_Assignment2
# Neural Networks and Deep Learnin 
Student Name**: Sharath chandra Seriyala 

University**: University of Central Missouri  

Assignment**: Home Assignment 2 (Chapters 5 & 6)  


---

## 📌 Assignment Overview

This assignment covers fundamental operations in Convolutional Neural Networks (CNNs), edge detection using custom kernels, pooling mechanisms, and preprocessing strategies for neural network training.

---

## ✅ Q1: Convolution Operations with Different Strides and Padding

**Goal:** Apply a custom 3×3 convolutional kernel to a 5×5 input matrix using different stride and padding combinations.

**Configurations Tested:**
- Stride = 1, Padding = VALID
- Stride = 1, Padding = SAME
- Stride = 2, Padding = VALID
- Stride = 2, Padding = SAME

**Libraries:** TensorFlow, NumPy  
**Result:** Output feature maps were printed and verified for each configuration.

---

## ✅ Q2: CNN Feature Extraction with Filters and Pooling

### 🔹 Task 1: Edge Detection Using Sobel Filter

**Steps:**
- Loaded a grayscale image (`dog.jpeg`)
- Applied Sobel filter in X and Y directions
- Used `cv2.filter2D` to manually apply Sobel kernels

**Result:** Displayed 3 side-by-side plots:
- Original Grayscale
- Sobel X
- Sobel Y

### 🔹 Task 2: Max and Average Pooling

**Steps:**
- Generated a random 4×4 matrix
- Applied 2×2 Max Pooling and Average Pooling using TensorFlow

**Result:** Printed original matrix, max-pooled, and average-pooled outputs.

---

## ✅ Q3: Data Preprocessing – Normalization vs. Standardization

### 🔹 Steps:
1. Loaded the **Iris dataset**
2. Applied:
   - **Min-Max Normalization**
   - **Z-score Standardization**
3. Visualized feature distributions using histograms
4. Trained Logistic Regression model on:
   - Original Data
   - Normalized Data
   - Standardized Data

### 📊 Accuracy Comparison:
| Preprocessing Type    | Accuracy |
|------------------------|----------|
| Original Data          | 1.0000   |
| Min-Max Normalization  | 0.9111   |
| Z-Score Standardization| 1.0000   |

---

## 🧠 When to Use Normalization vs Standardization in Deep Learning

| Scenario                             | Use Normalization | Use Standardization |
|--------------------------------------|-------------------|---------------------|
| Bounded input values (e.g. images)   | ✅                | ❌                  |
| Input features with varying scales   | ❌                | ✅                  |
| Used with CNNs                       | ✅                | ❌                  |
| Used with RNN, LSTM, MLP             | ❌                | ✅                  |
| Need faster convergence for training | ❌                | ✅                  |

📌 **Conclusion**: For most deep learning models, **Z-score standardization** is preferable due to better stability and faster training. **Min-Max normalization** is best for image data and CNNs.

---
