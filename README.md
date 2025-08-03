 Cat vs Dog Image Classifier | SkillCraft Internship - ML Task 3

This repository contains the solution for **SkillCraft Internship - Machine Learning Track (Task 3)**.  
The project involves building an image classification model to distinguish between **cats and dogs** using **Transfer Learning (VGG16)** and **Support Vector Machine (SVM)**.

---

 Dataset

- Total images: **1000** (Balanced: 500 cats, 500 dogs)
- Loaded from Google Drive
- Preprocessed and resized to **224x224**

---

 Approach

###  Preprocessing
- Resize all images to 224x224
- Normalize pixel values
- Encode labels (0: Cat, 1: Dog)

###  Feature Extraction
- Used pre-trained **VGG16** (without top layers) from Keras
- Extracted **25088** features per image

###  Classification
- Trained **SVM (Support Vector Machine)** on extracted features
- Split: 80% training, 20% testing

---

 Results

-  **Accuracy:** 97.5%
-  **Precision, Recall, F1-Score:** All above 96%

####  Classification Report:
```
               precision    recall  f1-score   support

           0       0.96      0.99      0.98       100
           1       0.99      0.96      0.97       100

    accuracy                           0.98       200
   macro avg       0.98      0.97      0.97       200
weighted avg       0.98      0.97      0.97       200
```

 Confusion Matrix:
```
[[99  1]
 [ 4 96]]
```

---

 Libraries Used

- Python (3.x)
- Google Colab
- TensorFlow (VGG16)
- Keras
- Scikit-learn (SVM, evaluation)
- NumPy, Matplotlib

---

 How to Run

1. Upload the dataset to Google Drive
2. Open the link : https://colab.research.google.com/drive/18dI0GELPuNH9kRbH511h8V3JzJ6i0Ii2?usp=sharing
3. Mount Drive and set path
4. Run cells step by step

---

 Learnings

- Transfer learning using pre-trained CNNs
- Feature extraction and dimensionality handling
- Traditional ML classifier on deep learning features
- Evaluation using confusion matrix and classification report



