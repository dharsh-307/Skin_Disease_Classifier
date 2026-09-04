# Skin_Disease_Classifier
AI-powered skin disease classification system using a Convolutional Neural Network (CNN) to classify skin images into eczema, melanoma, acne, and psoriasis.
# 🩺 Skin Disease Classifier

An AI-powered skin disease classification system that uses **Deep Learning and Convolutional Neural Networks (CNN)** to classify skin images into different disease categories.

## 📌 Project Overview

The **Skin Disease Classifier** is a machine learning project designed to assist in the preliminary classification of skin conditions from images.

The system analyzes an uploaded skin image and predicts the most likely category among:

* 🔴 Eczema
* 🟤 Melanoma
* 🔵 Acne
* 🟣 Psoriasis

The project demonstrates how **Artificial Intelligence, Computer Vision, and Deep Learning** can be applied to healthcare-related image classification.

> ⚠️ **Disclaimer:** This project is intended for educational and research purposes only. It is not a medical diagnostic tool and should not replace professional medical advice.

## 🎯 Objectives

* Develop an image classification model using CNN.
* Train the model using a skin disease image dataset.
* Classify skin images into multiple disease categories.
* Evaluate the performance of the trained model.
* Demonstrate the application of AI in healthcare.

## ✨ Features

* 🖼️ Skin image classification
* 🧠 CNN-based deep learning model
* 📊 Model training and evaluation
* 📈 Accuracy and loss analysis
* 💾 Saved trained model
* 🔍 Prediction of skin disease categories

## 🛠️ Technologies Used

| Technology                      | Purpose                 |
| ------------------------------- | ----------------------- |
| Python                          | Programming language    |
| TensorFlow / Keras              | Deep learning model     |
| CNN                             | Image classification    |
| NumPy                           | Numerical operations    |
| Pandas                          | Dataset handling        |
| Matplotlib                      | Data visualization      |
| Scikit-learn                    | Model evaluation        |
| Google Colab / Jupyter Notebook | Development environment |

## 📂 Project Structure

```text
skin-disease-classifier/
│
├── skin_disease_classifier.ipynb
├── skin_disease_model.keras
├── README.md
│
├── dataset/
│   ├── train/
│   ├── validation/
│   └── test/
│
└── requirements.txt
```

> The file names may be different depending on your project. Update the structure before uploading if necessary.

## 📊 Dataset

The model was trained using a skin disease image dataset containing images of different skin conditions.

### Classes

```text
Eczema
Melanoma
Acne
Psoriasis
```

The dataset is divided into training, validation, and testing sets to evaluate the model's performance.

## 🧠 Methodology

The project follows these steps:

1. **Data Collection** – Collect skin disease images.
2. **Data Preprocessing** – Resize and normalize the images.
3. **Data Augmentation** – Apply transformations to improve model generalization.
4. **Model Building** – Create a CNN architecture.
5. **Model Training** – Train the CNN using the prepared dataset.
6. **Model Evaluation** – Measure accuracy and loss.
7. **Prediction** – Use the trained model to classify new images.

## 🔄 Workflow

```text
Skin Image
    ↓
Image Preprocessing
    ↓
CNN Model
    ↓
Feature Extraction
    ↓
Disease Classification
    ↓
Predicted Category
```

## 🚀 How to Run

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/skin-disease-classifier.git
```

### 2. Navigate to the Project

```bash
cd skin-disease-classifier
```

### 3. Install Dependencies

```bash
pip install tensorflow numpy pandas matplotlib scikit-learn
```

### 4. Open the Notebook

Open the notebook in **Google Colab** or **Jupyter Notebook**.

### 5. Train or Load the Model

If the trained model is already available:

```python
from tensorflow.keras.models import load_model

model = load_model("skin_disease_model.keras")
```

### 6. Make a Prediction

```python
import numpy as np
from tensorflow.keras.preprocessing import image

img = image.load_img(
    "sample_image.jpg",
    target_size=(224, 224)
)

img_array = image.img_to_array(img)
img_array = np.expand_dims(img_array, axis=0)
img_array = img_array / 255.0

prediction = model.predict(img_array)

predicted_class = np.argmax(prediction[0])

print("Predicted Class:", predicted_class)
```

> Update the image size and class labels according to your trained model.

## 📈 Model Evaluation

The model can be evaluated using:

* Accuracy
* Precision
* Recall
* F1-score
* Confusion Matrix
* Training and validation loss

Example:

```python
loss, accuracy = model.evaluate(test_data)

print("Test Accuracy:", accuracy)
```

## 🔮 Future Enhancements

* Add more skin disease categories.
* Improve model accuracy using transfer learning.
* Develop a web application for image upload and prediction.
* Add confidence scores for predictions.
* Deploy the model using Flask or Streamlit.
* Integrate a dermatologist consultation feature.

## 👩‍💻 Author

**Catherine.P**

BCA Student | AI & Machine Learning Enthusiast

## 📄 License

This project is created for educational purposes.
