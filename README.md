# **Image Classification Using Machine Learning**  

## **Project Overview**  
This project focuses on developing a binary **image classification model** to distinguish between **cats and dogs** using **traditional machine learning algorithms**. The dataset consists of **1000 images** (500 for each class), which are preprocessed and converted into a numerical format suitable for classification.  

The models implemented include **Logistic Regression, Decision Tree, and Random Forest**, with **hyperparameter tuning** applied to improve classification accuracy.  

---

## **Table of Contents**  
- [Dataset Information](#dataset-information)  
- [Preprocessing & Feature Engineering](#preprocessing--feature-engineering)  
- [Machine Learning Models](#machine-learning-models)  
- [Performance Evaluation](#performance-evaluation)  
- [Future Enhancements](#future-enhancements)  
- [Installation & Usage](#installation--usage)  
- [GitHub Setup](#github-setup)  

---

## **Dataset Information**  
- The dataset contains **1000 grayscale images** of cats and dogs, split equally between the two classes.  
- Images are stored in **two separate folders**: `cats/` and `dogs/`.  
- Each image is resized to **64×64 pixels** and converted into a **flattened feature vector** for machine learning models.  

---

## **Preprocessing & Feature Engineering**  
- **Grayscale Conversion**: Reducing image complexity by removing color information.  
- **Resizing**: Standardizing all images to **64×64 pixels** to maintain uniformity.  
- **Flattening**: Converting images into **1D feature vectors** for ML model compatibility.  
- **Feature Scaling**: Using **StandardScaler** to normalize pixel values, improving model convergence.  

---

## **Machine Learning Models**  
The following models were trained and evaluated:  

1. **Logistic Regression**  
   - Baseline linear classifier.  
   - Convergence issues addressed by increasing `max_iter` and using `saga` solver.  

2. **Decision Tree Classifier**  
   - Handles non-linearity better than Logistic Regression.  
   - Moderate accuracy but prone to overfitting.  

3. **Random Forest Classifier**  
   - Ensemble-based model to improve generalization.  
   - Achieved the highest baseline accuracy.  

4. **Hyperparameter Tuning (Random Forest)**  
   - Used `GridSearchCV` to optimize parameters like `n_estimators` and `max_depth`.  
   - Improved accuracy by approximately **1%**.  

---

## **Performance Evaluation**  

| Model | Accuracy |  
|--------|----------|  
| Logistic Regression | ~50% |  
| Decision Tree | ~56% |  
| Random Forest | ~64.5% |  
| Tuned Random Forest | ~65.5% |  

- **Random Forest outperformed other models** due to its ensemble learning approach.  
- Accuracy is limited because traditional ML models struggle with **high-dimensional image data**.  
- Further improvements require **deep learning techniques** like Convolutional Neural Networks (CNNs).  

---

## **Future Enhancements**  
- **Implement CNNs** (e.g., using TensorFlow/Keras) to improve feature extraction.  
- **Data Augmentation** (rotation, flipping) to increase dataset variability and model robustness.  
- **Hyperparameter Optimization** using `RandomizedSearchCV` for faster tuning.  
- **Transfer Learning** with pre-trained models (e.g., VGG16, ResNet) to leverage feature extraction.  

---

## **Installation & Usage**  

### **Prerequisites**  
Ensure you have the following installed:  
- Python 3.x  
- NumPy  
- Matplotlib  
- Scikit-Learn  
- Pillow  

### **Clone the Repository**  
```sh
git clone https://github.com/your-username/your-repo.git
cd your-repo
```

### **Run the Project**  
```sh
python main.py
```

---

## **GitHub Setup**  

### **Initialize Git and Push the Project**  
```sh
git init
git add .
git commit -m "Initial commit - Image Classification Project"
git branch -M main
git remote add origin https://github.com/your-username/your-repo.git
git push -u origin main
```

### **Future Updates**  
```sh
git add .
git commit -m "Updated preprocessing and model performance"
git push origin main
```

---

## **Conclusion**  
This project demonstrates how **traditional machine learning models** can be applied to image classification tasks. While the accuracy is limited, the results highlight the need for deep learning-based models for superior performance. Future work will focus on **implementing CNNs** and **exploring advanced feature extraction techniques** to improve classification accuracy.  

---
