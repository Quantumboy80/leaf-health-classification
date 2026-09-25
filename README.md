# 🌿 Leaf Health Classification using Next-Generation YOLO Models

## Comparative Performance of Next-Gen YOLO Models for Leaf Health Classification in Ornamental Species

[![Research Paper](https://img.shields.io/badge/Research%20Paper-BIO%20Web%20of%20Conferences-blue)](https://doi.org/10.1051/bioconf/202622801001)
[![DOI](https://img.shields.io/badge/DOI-10.1051%2Fbioconf%2F202622801001-green)](https://doi.org/10.1051/bioconf/202622801001)
[![YOLO](https://img.shields.io/badge/YOLO-v8%20%7C%20v9%20%7C%20v11-red)](https://github.com/ultralytics/ultralytics)
[![Python](https://img.shields.io/badge/Python-3.x-blue)](https://www.python.org/)

A deep-learning based comparative study of **YOLOv8, YOLOv9, and YOLOv11** for automated leaf health classification in ornamental plant species.

The research focuses on **Ixora and Bougainvillea**, evaluating different YOLO generations under a common experimental setup using detection accuracy, localization performance, robustness, and inference-speed metrics.

---

## 📌 Overview

Plant disease detection is an important application of computer vision in modern horticulture and precision agriculture.

While many existing studies primarily focus on agricultural crops, this research investigates automated health and disease detection in **ornamental plant species**.

The study compares three generations of YOLO models:

- **YOLOv8**
- **YOLOv9**
- **YOLOv11**

The models were evaluated on a curated dataset of annotated leaf images containing healthy and diseased samples from **Ixora and Bougainvillea**.

The objective is to investigate the trade-off between:

- Detection accuracy
- Disease localization
- Environmental robustness
- Subtle disease-pattern detection
- Inference speed
- Overall model efficiency

---

## 🎯 Objectives

The main objectives of this research are:

- Compare the detection performance of YOLOv8, YOLOv9, and YOLOv11.
- Evaluate model accuracy and inference efficiency.
- Investigate deep-learning based disease detection in ornamental plants.
- Analyze model performance under environmental variations.
- Evaluate the ability of different YOLO generations to identify subtle disease symptoms.
- Study the trade-off between detection accuracy and real-time inference speed.
- Identify suitable YOLO architectures for automated ornamental plant health monitoring.

---

## 🌱 Plant Species

The study focuses on two ornamental plant species:

| Plant Species | Application |
|---|---|
| 🌺 **Ixora** | Healthy and diseased leaf detection |
| 🌸 **Bougainvillea** | Healthy and diseased leaf detection |

The dataset contains both healthy and diseased leaf samples.

The diseased samples represent different visible symptoms and conditions, including patterns associated with:

- Fungal infections
- Bacterial spots
- Nutrient deficiencies
- Pest-induced damage

---

## 🗂️ Dataset

The research uses a curated dataset referred to as **OrnaFoliage**.

The dataset contains approximately **5,000 augmented leaf images**.

### Dataset Split

| Dataset | Percentage |
|---|---:|
| Training | 70% |
| Validation | 15% |
| Testing | 15% |

The dataset contains approximately:

- **40% healthy samples**
- **60% diseased samples**

Data augmentation was used to improve model robustness against variations commonly encountered in real-world images.

### Augmentation Techniques

- Horizontal flipping
- Vertical flipping
- Rotation
- Brightness adjustment
- Contrast adjustment
- Gaussian noise
- Mosaic augmentation
- MixUp augmentation

Images were annotated using bounding boxes and prepared for YOLO-based object detection.

---

## 🧠 Models Evaluated

### YOLOv8

YOLOv8 was used as a strong real-time object detection baseline, providing a balance between detection accuracy and inference speed.

### YOLOv9

YOLOv9 was evaluated to investigate improvements in feature learning and generalization compared with earlier YOLO architectures.

### YOLOv11

YOLOv11 was evaluated as a newer YOLO architecture with improvements aimed at feature extraction, multi-scale representation, and efficient object detection.

All evaluated models were trained and tested under comparable experimental conditions.

---

## ⚙️ Experimental Setup

| Parameter | Configuration |
|---|---|
| Dataset | OrnaFoliage |
| Image Size | 640 × 640 |
| Training Epochs | 300 |
| Batch Size | 16 |
| Optimizer | AdamW |
| Learning Rate | 0.001 |
| GPU | NVIDIA RTX 3080 |
| Image Format | RGB |
| Normalization | [0, 1] |

---

## 📊 Performance Comparison

### Detection Performance

| Model | mAP@0.5 | Precision | Recall | ERS |
|---|---:|---:|---:|---:|
| YOLOv8 | 87.5% | 86.8% | 86.2% | 0.90 |
| YOLOv9 | 89.7% | 89.0% | 88.4% | 0.88 |
| **YOLOv11** | **92.3%** | **91.5%** | **90.8%** | **0.92** |

### Efficiency & Additional Metrics

| Model | F1-Score | FPS | DLA | SPDR |
|---|---:|---:|---:|---:|
| YOLOv8 | 86.5% | **85** | 0.82 | 82.3% |
| YOLOv9 | 88.7% | 72 | 0.85 | 85.1% |
| **YOLOv11** | **91.1%** | 68 | **0.89** | **88.5%** |

> **Note:** The reported metrics are based on the experimental results presented in the research paper.

---

## 🔬 Evaluation Metrics

In addition to standard object-detection metrics, the research considers application-specific evaluation parameters.

### mAP@0.5

Mean Average Precision at an Intersection over Union (IoU) threshold of 0.5, used to evaluate object detection performance.

### Precision

Measures the proportion of predicted positive detections that are correct.

### Recall

Measures the proportion of actual positive instances correctly detected by the model.

### F1-Score

The harmonic mean of precision and recall.

### DLA — Disease Localization Accuracy

Measures the ability of the model to accurately localize disease-related regions.

### ERS — Environmental Robustness Score

Evaluates model robustness under environmental variations and challenging visual conditions.

### SPDR — Subtle Pattern Detection Rate

Measures the ability to identify subtle disease-related visual patterns.

### FPS — Frames Per Second

Measures inference speed and provides an indication of real-time detection capability.

---

## 📈 Model Comparison

### mAP@0.5

```text
YOLOv8   ████████████████████████████████████████ 87.5%
YOLOv9   █████████████████████████████████████████ 89.7%
YOLOv11  ██████████████████████████████████████████ 92.3%

## 🔍 Key Findings

The experimental results reported in the study indicate that:

- **YOLOv11 achieved the highest reported mAP@0.5 of 92.3%.**
- YOLOv11 achieved the highest reported precision, recall, and F1-score among the evaluated models.
- **YOLOv8 achieved the highest reported inference speed at 85 FPS.**
- YOLOv9 provided an intermediate performance profile across the evaluated metrics.
- YOLOv11 demonstrated stronger performance in detecting subtle disease-related patterns.
- Model performance can be affected by environmental conditions and occlusion.
- The results demonstrate a trade-off between **detection accuracy, robustness, computational requirements, and inference speed**.

---

## 📁 Repository Structure

```text
leaf-health-classification/
│
├── yolo9/
│   └── content/
│       └── runs/
│           ├── detect/
│           └── segmentation/
│
├── yolo11/
│   └── content/
│       └── runs/
│           ├── detect/
│           └── segmentation/
│
├── README.md
│
└── bioconf_biospectrum2026_01001.pdf
