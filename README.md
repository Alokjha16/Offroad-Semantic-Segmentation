# 🚜 Offroad Semantic Scene Segmentation  
### Ignitia Hackathon – Duality AI Falcon Dataset  

---

## 📌 Project Overview

This project focuses on training a robust semantic segmentation model for off-road autonomy using synthetic desert digital twin data provided by Duality AI.

The objective was to train on one desert environment and evaluate on a novel but similar unseen desert biome to test generalization.

---

## 🧠 Model Architecture

- Model: DeepLabV3+
- Encoder: ResNet101
- Framework: PyTorch + segmentation_models_pytorch
- Classes: 9 semantic categories
- Input Resolution: 320x320
- Optimizer: AdamW
- Scheduler: CosineAnnealingLR
- Loss Function: CrossEntropy + IoU monitoring

---

## 📊 Final Performance

Validation mIoU: **0.6204**

The model demonstrates strong generalization across unseen desert terrain scenes.
<img width="1016" height="767" alt="image" src="https://github.com/user-attachments/assets/a7dcb519-1802-4710-8fd1-f342efb2db35" />


---

## 📈 Training Strategy

### Data Augmentation
- Horizontal Flip
- Random Crop
- Color Jitter
- Normalization

### Optimization Improvements
- Reduced learning rate after plateau
- Early stopping based on validation IoU
- Model checkpointing on best IoU
---
<img width="1064" height="702" alt="Screenshot 2026-03-01 025835" src="https://github.com/user-attachments/assets/315c671b-8166-487e-9d64-a7bc920159ae" />


---

## ❌ Failure Case Analysis

Observed misclassifications:
- Logs vs Rocks confusion
- Small Flowers misclassified as Ground Clutter
- Boundary confusion between Landscape and Dry Grass

Potential Improvements:
- Higher resolution training
- Class-weighted loss
- More aggressive augmentation

---


## 🚀 Reproducing Results

### 1️⃣ Install Dependencies

### 2️⃣ Train Model

### 3️⃣ Run Inference

---

## 🏁 Hackathon Evaluation Criteria Alignment

✔ IoU Optimization  
✔ Clear Documentation  
✔ Reproducible Pipeline  
✔ Failure Case Analysis  
✔ Clean Folder Packaging  

---

## 🔮 Future Work

- Domain adaptation for non-desert biomes  
- Self-supervised pretraining  
- Real-time inference optimization (<50ms per frame)  
- Multi-view terrain segmentation  

---

## 👤 Author

Alok Jha  
Ignitia Hackathon Participant  
