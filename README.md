# UI Element Sketch Classification

This project was developed as part of the [IASA Championship 2024 hackathon]([url](https://www.kaggle.com/competitions/iasa-champ-24-ui-element-sketch-classification)) for UI element sketch classification. The goal was to create a machine learning model capable of accurately classifying hand-drawn sketches of various UI elements into predefined categories.

## 🎨 Data Source
The dataset consists of sketched UI elements organized into 21 different classes, including common interface components such as buttons, icons, text fields, and other UI elements. The dataset is structured with:

- Training images organized by class folders
- Test images for final predictions
- Approximately 600 images per class in the training set

Dataset is available on [Kaggle]([url](https://www.kaggle.com/competitions/iasa-champ-24-ui-element-sketch-classification/data)).

## ⚙️ Machine Learning Architecture

- Base Model: MobileNet (pre-trained on ImageNet)
- Transfer Learning: Leveraged pre-trained weights for feature extraction

```
Input Layer (224, 224, 3)
    ↓
MobileNet Base (pre-trained)
    ↓
Global Average Pooling 2D
    ↓
Dense Layer (21 units, softmax)
    ↓
Output (21 classes)
```

## 📊 Results and Performance

- Final Validation Accuracy: 86.0%
