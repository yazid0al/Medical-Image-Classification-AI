# 🧠 Medical-Image-Classification-AI
An AI vision model utilizing Google Teachable Machine and Keras to classify and detect brain tumors from medical MRI scans.

## 📖 Overview
This repository contains a deep learning image classification project designed to identify brain tumors from medical images. Built using TensorFlow and Keras, the Python script analyzes input scans and predicts the specific tumor class, such as **meningioma**, while providing a statistical confidence score.

This project serves as a showcase of applying Artificial Intelligence and computer vision to healthcare and medical diagnostics. 

## 📊 Dataset
The medical imaging data used to train this model was sourced from Kaggle: 
* **🔗 Dataset Link:** [Brain Tumor Image Dataset](https://www.kaggle.com/datasets/denizkavi1/brain-tumor)

The dataset consists of MRI scans categorized into specific brain tumor classes, providing the foundational data required for the model to distinguish between healthy and affected scans.

## ⚙️ Model Training
The underlying image classification model was prototyped and trained using [Google's Teachable Machine](https://teachablemachine.withgoogle.com/). This platform handled the transfer learning process based on the Kaggle dataset, allowing for the rapid export of a ready-to-use TensorFlow/Keras model (`keras_model.h5`) and the corresponding class names (`labels.txt`). 


## ✨ Features
* **⚡ Pre-trained Model Integration:** Utilizes the exported Keras model for rapid inference without needing to retrain from scratch.
* **🏷️ Dynamic Labeling:** Automatically maps predictions to human-readable class names via a `labels.txt` file.
* **🖼️ Image Preprocessing:** Uses the Python Imaging Library (Pillow) and NumPy to format images to the required `(1, 224, 224, 3)` tensor shape for the neural network.
* **🎯 Confidence Scoring:** Outputs both the predicted class and the model's confidence level for that prediction.

## 💻 Tech Stack
* 🐍 **Python 3**
* 🧡 **TensorFlow / Keras (`tf_keras`)**
* 🔢 **NumPy**
* 🖼️ **Pillow (PIL)**

## 🚀 Installation
 Clone the repository:
   ```bash
   git clone [https://github.com/yazid0al/Medical-Image-Classification-AI.git](https://github.com/yazid0al/Medical-Image-Classification-AI.git)
   cd Brain-Tumor-Classifier

## 🛠️ Usage & Getting the Output
Follow these steps to test the model and generate a prediction:

**Step 1: Prepare a Test Image**
Place a sample MRI scan image (e.g., `.jpg` or `.png`) into the root directory or a file, as I did for this project. 

**Step 2: Update the Image Path**
Open the main script in your code editor and ensure the image variable points to your test image.
```python
# Replace this with the path to your image
image_path = "test_image/pituitary_tumor.png"
```
**Example Output:**
```text
1/1 [==============================] - 0s 39ms/step
Class: Pituitary tumor
Confidence Score: 0.9991473
 ``` 
![Alt text describing the image](test_images/pituitary_tumor.png)
