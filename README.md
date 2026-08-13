# 🐱🐶 Transfer Learning using CNNs

A Deep Learning project that uses **Transfer Learning with VGG16** to classify images as **Cat** or **Dog**.

## 📌 Overview

The pretrained VGG16 model is used as a feature extractor, with custom Dense layers added for binary classification.

```text
Image
  ↓
VGG16 (ImageNet)
  ↓
Feature Extraction
  ↓
Flatten
  ↓
Dense(256, ReLU)
  ↓
Dense(1, Sigmoid)
  ↓
Cat / Dog
```

## 🛠️ Technologies

- Python
- TensorFlow / Keras
- VGG16
- NumPy
- Matplotlib
- Pillow

## 📊 Dataset

**Cat vs Dog Dataset**

Classes:

- 🐱 Cat
- 🐶 Dog

Images are resized to:

```text
150 × 150 × 3
```

## 🧠 Model

**VGG16 pretrained on ImageNet**

```python
VGG16(
    weights="imagenet",
    include_top=False,
    input_shape=(150, 150, 3)
)
```

Custom classification layers:

```python
Flatten()
Dense(256, activation="relu")
Dense(1, activation="sigmoid")
```

## 📈 Training

The model is trained using:

- Optimizer: **Adam**
- Loss: **Binary Crossentropy**
- Metric: **Accuracy**
- Epochs: **10**

Training and validation loss are visualized to monitor model performance and overfitting.

## 🔮 Prediction

The trained model can classify a new image as:

```text
🐱 Cat
or
🐶 Dog
```

with a confidence score.

## 📁 Project Structure

```text
Transfer-Learning-using-CNNs/
│
├── Transfer_Learning_using_CNNs.ipynb
├── cat_dog_vgg16.keras
├── requirements.txt
└── README.md
```

## 🚀 Run Locally

```bash
git clone https://github.com/Fahadqureshi0/Transfer-Learning-using-CNNs.git
cd Transfer-Learning-using-CNNs
pip install -r requirements.txt
```

Open the notebook using **Google Colab** or **Jupyter Notebook**.

## 🔮 Future Improvements

- Streamlit prediction interface
- Image upload
- Data augmentation
- Fine-tuning VGG16
- Confusion matrix
- Grad-CAM visualization

## 👨‍💻 Author

**Fahad Qureshi**

## 📄 License

This project is licensed under the **MIT License**.
