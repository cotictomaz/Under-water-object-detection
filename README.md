# 🌊 Underwater Object Detection with RetinaNet and Faster R-CNN

This repository contains my work on **object detection in underwater environments**, where I fine-tune and compare **RetinaNet** and **Faster R-CNN** models using different backbone networks.  
The project is implemented in **PyTorch** and includes **data augmentation**, **training**, **evaluation**, and an **interactive visualization** of model predictions.

---

## Project Overview

Underwater imagery poses unique challenges for computer vision:  
low visibility, lighting variations, color distortions, and occlusions from water particles.  
This project explores how modern deep learning detectors perform in this domain.

### Objectives
- Fine-tune **RetinaNet** and **Faster R-CNN** on the *Aquarium Object Detection Dataset*.  
- Experiment with **different backbone architectures** (e.g., ResNet50, MobileNet).  
- Apply **diverse data augmentation** strategies to improve model robustness.  
- Compare models quantitatively using **mAP** metrics on train/validation/test splits.  
- Provide an **interactive notebook interface** to visualize and compare model predictions.

---

## Dataset

The [Aquarium Object Detection Dataset](https://public.roboflow.com/object-detection/aquarium) is collected by Brad Dwyer(Roboflow team) from two aquariums in the United States: The Henry Doorly Zoo in Omaha (October 16, 2020) and the National Aquarium in Baltimore (November 14, 2020). The dataset consists of 638 images splitted into train, test and validation data.

---

## 🧠 Models and Methods

| Backbone           | Train mAP | Valid mAP | Test mAP |
|-----------------|-----------|-----------|-----------|
| ResNet-50 (DA)  | 0.5      | 0.41      | 0.41      |
| ResNet-50 (noDA)     | 0.88      | 0.37      | 0.37      |
| MobileNet (DA)           | 0.54      | 0.36      | 0.01      |
| MobileNet (noDA)           | 0.65      | 0.31      | 0.34      |

---

## Data Augmentation Techniques

The training pipeline includes a rich set of augmentations to simulate realistic underwater conditions:

- Random horizontal/vertical flips  
- Rotations
- Gaussian blur  
- Random scaling  

These transformations are implemented using **Albumentations** for efficiency and flexibility.

---

## 🧪 Evaluation Metrics

Each model is evaluated on:
- **Mean Average Precision (mAP)**
- **Precision-Recall curves** and **Confusion matrix** will be added in the future.

---

## 💻 Interactive Visualization

At the end of the notebook, an **interactive widget** allows you to:
- Select a model and a backbone
- Pick an image from the test set and select the score and iou thresholds (for postprocessing)
- Display the predicted bounding boxes and class labels  
- Compare detections side-by-side

This makes it easy to **visually assess** the performance differences between detectors.

---
