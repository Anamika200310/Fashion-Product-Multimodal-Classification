# Fashion-Product-Multimodal-Classification
## Project Overview

This project develops a multimodal deep learning system for fashion product classification by combining visual and textual information.

The system integrates:

- EfficientNetV2 for image feature extraction
- DistilBERT for text representation learning
- Late Fusion neural network for multimodal classification

The model classifies fashion products into **90 product categories** using both product images and metadata.

---

## Dataset

The project uses the Fashion Product Images Dataset from Kaggle.

After preprocessing:

- 44,020 total samples
- 90 product categories
- Image + metadata available for every product

Dataset split:

- Training: 30,814
- Validation: 4,402
- Test: 8,804

---

## Models

### 1. EfficientNetV2 Image Model

- Transfer Learning
- Fine-tuning
- Image embeddings (256 dimensions)

---

### 2. DistilBERT Text Model

- Leakage-controlled metadata
- DistilBERT encoder
- Text embeddings (256 dimensions)

---

### 3. Multimodal Fusion Model

The image and text embeddings are concatenated into a 512-dimensional feature vector and passed through a fully connected classifier.

---

## Results

| Model | Test Accuracy |
|--------|--------------:|
| DistilBERT | 55.0% |
| EfficientNetV2 | 88.8% |
| Multimodal Fusion | **91.4%** |

The multimodal model achieved the best overall performance by combining complementary visual and textual information.

---

## Repository Structure

```
Fashion-Product-Multimodal-Classification
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
- NumPy
- Pandas
- Scikit-learn
- Matplotlib

---

## Author

**Anamika K S**
