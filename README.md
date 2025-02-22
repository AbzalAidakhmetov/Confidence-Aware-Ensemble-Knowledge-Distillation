# Confidence Aware Ensemble Knowledge Distillation

This repository contains the code for our Advanced Machine Learning final project on Confidence Aware Ensemble Knowledge Distillation. The project demonstrates how to transfer knowledge from multiple large teacher models to a lightweight student model, thereby achieving improved performance on resource-constrained devices.

## Overview

Knowledge distillation (KD) is a technique that enables a smaller student model to learn from one or more larger teacher models. In this project, we experiment with both single-teacher and multi-teacher KD approaches on the CIFAR-100 dataset. Our multi-teacher framework includes several novel methods:

- **Confidence-Aware Weighted KD (CA-WKD)**
- **α-Guided CA-WKD**
- **Adaptive α-Guided KD**

These methods dynamically adjust the influence of each teacher based on their confidence scores, ensuring that the student model is primarily guided by the strongest predictions.

## Key Features

- **Multi-Teacher Distillation:** Combines predictions from diverse teacher models such as ResNet-50, DenseNet-121, and ViT-B16/224.
- **Novel KD Techniques:** Implements CA-WKD, α-Guided CA-WKD, and Adaptive α-Guided KD to balance teacher contributions.
- **Automated Training:** Utilizes [PyTorch Lightning](https://www.pytorchlightning.ai/) for streamlined training and [Weights & Biases](https://wandb.ai/) for experiment tracking and automation.
- **Efficient Performance:** Achieves significant accuracy improvements over the baseline by leveraging effective distillation strategies on the CIFAR-100 dataset.


## Results and Discussion

Our experiments demonstrate the effectiveness of the knowledge distillation approaches:

- **Baseline (Training Student from Scratch):** ~66.29% accuracy
- **Single Teacher KD:**
  - ResNet-50: ~73.75%
  - ViT-B16/224: ~74.00%
  - DenseNet-121: ~75.38%
- **Multi-Teacher KD:**
  - CA-WKD (Method 1): ~73.33%
  - Adaptive α-Guided KD (with temperature tuning): ~74.00%

These results confirm that proper teacher selection and dynamic weighting of their contributions can significantly boost the performance of the student model.

## References

1. Jing Gou et al., *Knowledge distillation: A survey*. International Journal of Computer Vision, 2021.
2. Mark Sandler et al., *Inverted residuals and linear bottlenecks: Mobile networks for classification, detection and segmentation*, 2018.
3. Lucas Beyer et al., *Knowledge distillation: A good teacher is patient and consistent*, 2022.
4. Hailin Zhang et al., *Confidence-aware multi-teacher knowledge distillation*. ICASSP 2022.

## Contributors

- Abzal Aidakhmetov
- Adilkhan Bakridenov
- Eldar Gabdulsattarov
- Nadir Nuralin
