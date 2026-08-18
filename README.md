[CIFAR-10 Image Classification using CNN — README.md](https://github.com/user-attachments/files/31198550/CIFAR-10.Image.Classification.using.CNN.README.md)
# CIFAR-10 Image Classification using CNN

This project uses a **Convolutional Neural Network (CNN)** to classify images from the **CIFAR-10 dataset** into 10 different categories.

The model is developed using **Python, TensorFlow, and Keras** and is trained to learn visual patterns from color images.

## 📌 Project Overview

The **CIFAR-10 dataset** contains 60,000 color images divided into 10 different classes.

The 10 classes are:

- ✈️ Airplane
- 🚗 Automobile
- 🐦 Bird
- 🐱 Cat
- 🦌 Deer
- 🐶 Dog
- 🐸 Frog
- 🐴 Horse
- 🚢 Ship
- 🚚 Truck

Each image has a resolution of **32 × 32 pixels** with **3 RGB color channels**.

## 🧠 CNN Architecture

The project uses a CNN to automatically learn important features from the images.

```text
Input Image (32 × 32 × 3)
        ↓
Convolutional Layer (32 filters)
        ↓
Max Pooling
        ↓
Convolutional Layer (64 filters)
        ↓
Max Pooling
        ↓
Dropout (25%)
        ↓
Convolutional Layer (64 filters)
        ↓
Flatten
        ↓
Dense Layer (128 neurons)
        ↓
Dropout (50%)
        ↓
Output Layer (10 classes)
```

### Layers Used

- **Conv2D:** Extracts features such as edges, shapes, and patterns.
- **MaxPooling2D:** Reduces the size of feature maps while keeping important information.
- **Dropout:** Helps prevent overfitting during training.
- **Flatten:** Converts the extracted features into a one-dimensional vector.
- **Dense:** Learns relationships between the extracted features.
- **Softmax:** Produces probabilities for the 10 possible classes.

## 📊 Dataset

The project uses the **CIFAR-10 dataset**.

| Property | Value |
|---|---:|
| Total Images | 60,000 |
| Training Images | 50,000 |
| Testing Images | 10,000 |
| Image Size | 32 × 32 |
| Color Channels | 3 (RGB) |
| Number of Classes | 10 |

The images are normalized before training so that pixel values are scaled from **0–255 to 0–1**.

## ⚙️ Model Configuration

The CNN model is trained with the following settings:

| Parameter | Value |
|---|---|
| Optimizer | Adam |
| Learning Rate | 0.0001 |
| Loss Function | Sparse Categorical Crossentropy |
| Metric | Accuracy |
| Epochs | 25 |
| Validation Split | 20% |

## 📈 Results

After training for **25 epochs**, the model was evaluated on the CIFAR-10 test dataset.

### Test Performance

- **Test Accuracy:** **66.86%**
- **Test Loss:** **0.9434**

The model correctly classified approximately **67 out of every 100 test images**.

The notebook also includes graphs to visualize:

- Training Accuracy
- Validation Accuracy
- Training Loss
- Validation Loss

These graphs help understand how the model performs during training and whether overfitting occurs.

## 🔍 Image Prediction

After training, the model can be used to predict the class of an image from the test dataset.

The predicted class is compared with the actual class to check whether the model classified the image correctly.

Example:

```text
Actual Class: Cat
Predicted Class: Cat
```

## 💾 Model Saving

The trained CNN model can be saved and loaded later for making predictions without training the model again.

Example:

```python
model.save("cifar10_cnn_model.keras")
```

To load the saved model:

```python
from tensorflow.keras.models import load_model

model = load_model("cifar10_cnn_model.keras")
```

## 🛠️ Technologies Used

- **Python**
- **TensorFlow**
- **Keras**
- **NumPy**
- **Matplotlib**
- **Jupyter Notebook**

## 🚀 How to Run

### 1. Clone the Repository

```bash
git clone https://github.com/Rohit-Kumar-Mandolliya/CIFAR10-CNN-Image-Classification.git
```

### 2. Install Dependencies

```bash
pip install tensorflow numpy matplotlib jupyter
```

Or, if you have a `requirements.txt` file:

```bash
pip install -r requirements.txt
```

### 3. Open the Notebook

Open:

```text
CIFAR10_Image_Classification.ipynb
```

using Jupyter Notebook or JupyterLab.

### 4. Run the Notebook

Run the cells step by step to:

1. Load the CIFAR-10 dataset
2. Preprocess the images
3. Normalize the data
4. Build the CNN model
5. Compile the model
6. Train the model
7. Evaluate the model
8. Plot accuracy and loss
9. Make image predictions

## 📁 Project Structure

```text
CIFAR10-CNN-Image-Classification/
│
├── CIFAR10_Image_Classification.ipynb
├── README.md
├── requirements.txt
└── cifar10_cnn_model.keras
```

## 🎯 Conclusion

This project demonstrates how **Convolutional Neural Networks (CNNs)** can be used for image classification.

The model learns visual features from the CIFAR-10 dataset and classifies images into 10 different categories.

With a **test accuracy of 66.86%**, this project provides a practical introduction to **CNN-based computer vision and image classification using TensorFlow/Keras**.

## 🔮 Future Improvements

The model's accuracy can potentially be improved by:

- Adding more convolutional layers
- Using **Batch Normalization**
- Applying **Data Augmentation**
- Using a learning-rate scheduler
- Training for more epochs
- Tuning the CNN architecture
- Using transfer learning with pretrained models

## 👨‍💻 Author

**Rohit Kumar**
