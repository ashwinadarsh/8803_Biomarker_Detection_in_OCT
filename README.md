# 8803_Biomarker_Detection_in_OCT

Please refer to the pdf if the ipynb fails to load.

---

# Multi-label Biomarker Detection in OCT Scans

**Authors:** Ashwin Adarsh (aadarsh6@gatech.edu), Joseph F. Ferraro (jferraro8@gatech.edu)  
**Affiliation:** Georgia Institute of Technology

## Overview

This project compares six state-of-the-art deep learning models for multi-label biomarker detection from Optical Coherence Tomography (OCT) B-Scans. The goal is to identify six clinically relevant biomarkers using a consistent training and evaluation framework.

## Architectures Evaluated

- **ResNet18**
- **ResNet50**
- **DenseNet121**
- **InceptionNet V3** (Best Macro F1)
- **Vision Transformer (ViT B 16)**
- **ConvNeXt Tiny** (Best Accuracy)

## Dataset

We use the **OLIVES** dataset, consisting of over 78,000 OCT scans with ~9,400 annotated images and rich clinical metadata, including BCVA and CST.

## Training Details

- **Framework:** PyTorch  
- **Environment:** Google Colab (T4 GPU)  
- **Optimizer:** Adam (lr = 1e-4)  
- **Loss:** BCEWithLogitsLoss  
- **Epochs:** 10  
- **Batch Size:** 8  
- **Input Size:** 299×299 (Inception), 224×224 (others)

## Key Findings

- **InceptionNet V3** achieved the best **Macro F1 Score**.
- **ConvNeXt Tiny** led in **Accuracy**.
- **DenseNet121** had the lowest **Loss** and strong Micro F1.
- **ViT B 16** underperformed due to dataset constraints.

## Future Work

- Incorporate self-supervised learning
- Improve transformer tuning
- Explore patient-level personalization

## Resources

- 📄 [Paper (PDF)](https://github.com/ashwinadarsh/8803_Biomarker_Detection_in_OCT/blob/main/oct_biomarker_detection.pdf)  
- 📊 [Colab Notebook](https://colab.research.google.com/drive/1Yp2B4DJNirkTQC-1uybRm1PvwKMhtCbs?usp=sharing)  
- 📁 [GitHub Repository](https://github.com/ashwinadarsh/8803-Biomarker-Detection-in-OCT)

