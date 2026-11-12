# Rock-Paper-Scissors Image Classification using CNN

## About the Project

This project explores the fundamentals of Computer Vision through a Rock-Paper-Scissors image classification model built using **Convolutional Neural Networks (CNNs)**.
The project focuses on enabling machines to recognise and classify hand gestures by learning visual patterns from image data.
The model uses supervised learning to classify images into three categories: Rock, Paper and Scissors.

## Dataset

The project uses the [Rock-Paper-Scissors Dataset](https://www.kaggle.com/datasets/sanikamal/rock-paper-scissors-dataset) available on Kaggle.

The dataset consists of labelled images belonging to three categories:

- **Rock**
- **Paper**
- **Scissors**

These images serve as input data for training, validating and testing the classification model.

## Technologies & Libraries

- Python
- TensorFlow
- Keras
- NumPy
- Matplotlib
- Scikit-learn
- Google Colab

## Methodology

The project was implemented through the following stages:

### 1. Data Loading and Preprocessing

The image dataset was loaded and prepared for the CNN model.

- Used image processing utilities to load the dataset.
- Converted images into RGB format.
- Resized all images to **128 × 128 pixels**.
- Normalised pixel values to a range of 0 to 1.
- Encoded categorical class labels into numerical representations.
- Divided the dataset into training, validation and testing sets using a **70:15:15 ratio**.

### 2. CNN Model Architecture

A Sequential Convolutional Neural Network was implemented using TensorFlow and Keras.

The architecture consists of:

- **Conv2D:** Implemented convolutional layers with 32, 64 and 128 filters to extract visual features such as edges, shapes and patterns.
- **ReLU Activation:** Introduced non-linearity to help the network learn complex visual representations.
- **MaxPooling2D:** Reduced the spatial dimensions of feature maps while retaining important information.
- **GlobalAveragePooling2D:** Converted extracted feature maps into a compact feature representation.
- **Dropout:** Reduced the likelihood of overfitting by randomly deactivating neurons during training.
- **Dense:** Connected extracted features to the classification layer.
- **Softmax Activation:** Generated class probabilities for Rock, Paper and Scissors.

### 3. Model Compilation

The CNN model was configured for multi-class classification using:

- **Optimizer – Adam:** Used to update model weights and minimise training error.
- **Loss Function – Sparse Categorical Cross-Entropy:** Calculated the difference between predicted probabilities and actual class labels.
- **Metric – Accuracy:** Monitored the proportion of correctly classified images.

### 4. Model Training

The model was trained using the preprocessed training dataset.

- Used the training dataset to learn visual patterns and features.
- Used the validation dataset to monitor model performance during training.
- Updated model weights through backpropagation and the Adam optimisation algorithm.
- Tracked training and validation accuracy and loss across epochs.

### 5. Model Evaluation and Visualisation

The trained model was evaluated using the unseen testing dataset.

The following techniques were used to analyse its performance:

- **Model Evaluation:** Evaluated the model using test data and calculated loss and accuracy.
- **Prediction:** Used the trained model to generate predictions for input images.
- **Accuracy and Loss Curves:** Used Matplotlib to visualise training and validation performance.
- **Confusion Matrix:** Used Scikit-learn to compare actual and predicted class labels and analyse classification performance.

## Key Concepts Explored

- Supervised Learning
- Computer Vision
- Image Preprocessing
- Convolutional Neural Networks
- Feature Extraction
- Activation Functions
- Pooling and Regularisation
- Multi-class Image Classification
- Model Training and Evaluation
- Generalisation and Overfitting
