# Fashion Product Multimodal Classification

## Overview

This project presents a multimodal deep learning framework for fashion product classification by combining image and text information.

The framework consists of three models:

- EfficientNetV2 for image classification
- DistilBERT for text classification
- Late Fusion neural network that combines both modalities

The multimodal model improves classification performance by leveraging complementary visual and textual features.

---

## Dataset

**Source**

Fashion Product Images Dataset (Kaggle)

After preprocessing:

- **44,020** products
- **90** fashion categories
- Image and metadata available for every sample

Dataset split:

| Split | Samples |
|-------|---------:|
| Training | 30,814 |
| Validation | 4,402 |
| Test | 8,804 |

---

## Project Pipeline

```
Image
   │
EfficientNetV2
   │
256-d Image Feature
                  \
                   \
                    → Late Fusion → Product Category
                   /
                  /
256-d Text Feature
   │
DistilBERT
   │
Metadata
```

---

## Models

### 1. EfficientNetV2 Image Model

- Transfer Learning
- Fine-tuning
- 256-dimensional image embeddings

---

### 2. DistilBERT Text Model

- Leakage-controlled metadata
- Frozen DistilBERT encoder
- 256-dimensional text embeddings

---

### 3. Multimodal Fusion

The image and text embeddings are concatenated into a **512-dimensional feature vector** and passed through a neural network classifier.

---

## Results

| Model | Test Accuracy |
|------|--------------:|
| DistilBERT | 55.0% |
| EfficientNetV2 | 88.8% |
| **Multimodal Fusion** | **91.4%** |

The multimodal model achieved the highest classification accuracy by combining visual and textual representations.

---

## Repository Structure

```
Fashion-Product-Multimodal-Classification/
│
├── 01_EfficientNetV2_Image_Model.ipynb
├── 02_DistilBERT_Text_Model.ipynb
├── 03_Multimodal_Fusion_Model.ipynb
├── README.md
└── LICENSE
```

---

## Technologies

- Python
- TensorFlow
- Hugging Face Transformers
- EfficientNetV2
- DistilBERT
- Scikit-learn
- NumPy
- Pandas
- Matplotlib

---

## Author

**Anamika K S**

MSc Artificial Intelligence
Dublin Business School
