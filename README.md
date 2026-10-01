# MultiScale-CNN-BiGRU-Attention Framework for Automated CT-Based Brain Stroke Classification

A novel deep learning framework that integrates **Multi-Scale CNN**, **Bidirectional GRU (BiGRU)**, and **Attention** mechanism for accurate three-class brain stroke classification from CT images.

**Paper accepted at:** 2026 IEEE 2nd International Conference on Quantum Photonics, Artificial Intelligence, and Networking (QPAIN), Chittagong, Bangladesh.

---

## Model Overview

| Component | Role |
|-----------|------|
| **Multi-Scale CNN (ResNet-50)** | Extracts hierarchical spatial features at multiple scales |
| **BiGRU** | Models bidirectional contextual dependencies across feature scales |
| **Attention Mechanism** | Emphasizes discriminative stroke-related regions |
| **Grad-CAM** | Provides visual explanations of model decisions |

### Key Results
- **Test Accuracy:** 96.02%
- **5-Fold CV Accuracy:** 94.61% (average)
- **Classes:** Bleeding, Ischemia, Normal

---

## Project Structure

```
├── MultiScale_CNN_BiGRU_Attention_Framework_for_Automated_CT_Based_Brain_Stroke_Classification_.pdf
├── README.md
├── requirements.txt
└── .gitignore
```

---

## Installation

```bash
# Clone the repository
git clone https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
cd YOUR_REPO_NAME

# Create virtual environment (recommended)
python -m venv venv
source venv/bin/activate          # Linux/Mac
# venv\Scripts\activate           # Windows

# Install dependencies
pip install -r requirements.txt
```

---

## Dataset

Experiments were conducted on the **Brain Stroke CT Dataset** publicly available on Kaggle.

**Class distribution:**

| Class     | Total Images | Training (80%) | Testing (20%) |
|-----------|--------------|----------------|---------------|
| Bleeding  | 1,093        | 874            | 219           |
| Ischemia  | 1,131        | 905            | 226           |
| Normal    | 4,426        | 3,541          | 885           |
| **Total** | **6,650**    | **5,320**      | **1,330**     |

> **Note:** Dataset files are **not** included in this repository. Please download from Kaggle.

---

## Hyperparameters

| Parameter              | Value                          |
|------------------------|--------------------------------|
| Input image size       | 128 × 128                      |
| Batch size             | 32                             |
| Number of classes      | 3                              |
| Epochs                 | 10                             |
| Learning rate          | 1 × 10⁻⁴                       |
| Optimizer              | AdamW                          |
| Loss function          | Weighted Cross-Entropy         |
| Backbone               | ResNet-50 (ImageNet pretrained)|
| GRU hidden units       | 256 (Bidirectional)            |
| Dropout rate           | 0.05                           |

---

## Results Summary

| Metric                  | Score     |
|-------------------------|-----------|
| Test Accuracy           | 96.02%    |
| 5-Fold CV Accuracy      | 94.61%    |
| Macro Precision         | 92.60%    |
| Macro Recall            | 92.34%    |
| Macro F1-score          | 0.924     |
| Specificity             | 0.926     |

### Class-wise Performance

| Class     | Precision | Recall  | F1-score |
|-----------|-----------|---------|----------|
| Bleeding  | 0.9414    | 0.9289  | 0.9351   |
| Ischemia  | 0.9245    | 0.9032  | 0.9138   |
| Normal    | 0.9732    | 0.9820  | 0.9776   |

---

## Citation

If you use this work, please cite:

```bibtex
@inproceedings{rofik2026multiscale,
  title={MultiScale-CNN-BiGRU-Attention Framework for Automated CT-Based Brain Stroke Classification},
  author={Rofik, Amimul A Hasan and Ali, Md. Yousuf and Khan, Salman Bin Arif and Islam, Ashikul and Liva, Ismatul Ferdush and Joy, Md. Arman Hossain},
  booktitle={2026 IEEE 2nd International Conference on Quantum Photonics, Artificial Intelligence, and Networking (QPAIN)},
  year={2026},
  organization={IEEE}
}
```

---

## Authors

- **Amimul A Hasan Rofik** (Corresponding Author) – amimulhasan35@gmail.com  
- Md. Yousuf Ali  
- Salman Bin Arif Khan  
- Ashikul Islam  
- Ismatul Ferdush Liva  
- Md. Arman Hossain Joy  

**Affiliation:** Department of Biomedical Engineering, Islamic University, Kushtia-7003, Bangladesh

---

## License

This project is released for research and educational purposes.
