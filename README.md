# 🧠 Brain Tumor Classification using Custom CNN (TensorFlow)

This project aims to classify MRI brain scans into four categories of brain tumors using a **custom-built Convolutional Neural Network (CNN)** in TensorFlow and Keras. The model was trained on the **Brain Tumor MRI Dataset** by [Sartaj Bhuvaji on Kaggle](https://www.kaggle.com/datasets/sartajbhuvaji/brain-tumor-classification-mri).

---

## 📂 Dataset

**Source:** [Brain Tumor MRI Dataset (Kaggle)](https://www.kaggle.com/datasets/sartajbhuvaji/brain-tumor-classification-mri)

**Classes:**
- Glioma Tumor  
- Meningioma Tumor  
- Pituitary Tumor  
- No Tumor  

**Total Images:** ~3,000  
**Image Size:** 224 × 224 pixels  
**Color Mode:** RGB  

The dataset was combined from the provided **Training** and **Testing** folders, then split manually into:
- **70% Training**
- **15% Validation**
- **15% Testing**

Each subset was batched, cached, and prefetched for optimal GPU performance.

---

### 🧪 Final Model Performance (Epoch 50/50)

| Metric | Training | Validation | Test |
|:--------|:----------:|:------------:|:------:|
| **Loss** | 0.0532 | 0.1306 | 0.1699 |
| **Accuracy** | 0.9974 | 0.9693 | 0.9511 |
| **Precision** | 0.9978 | 0.9693 | 0.9529 |
| **Recall** | 0.9965 | 0.9693 | 0.9470 |
| **AUC** | 1.0000 | 0.9964 | 0.9923 |

---

### 📊 Results Interpretation

The custom Convolutional Neural Network (CNN) achieved **excellent performance** on the Brain MRI dataset for tumor classification.  
Key takeaways:

- 🧠 **High Accuracy (95%)** on the test set indicates strong generalization and reliability across unseen MRI scans.  
- 🎯 **Precision (95%)** means the model makes very few false positive tumor predictions — a critical feature for clinical safety.  
- ❤️ **Recall (94.7%)** shows the model effectively detects nearly all tumor cases, minimizing the risk of missed diagnoses.  
- 📈 **AUC (0.9923)** reflects excellent separability between tumor and non-tumor classes, showing strong model confidence.  
- 🧩 The training metrics (near 100%) with slightly higher validation/test losses suggest **good generalization without major overfitting**, thanks to early stopping and learning rate scheduling.

  ### 📊 Validation Graphs & Confusion matrix
  <img width="1001" height="470" alt="image" src="https://github.com/user-attachments/assets/bb65ce4b-3773-4cba-98b8-f65c42f2008f" />

  <Figure size 800x600 with 2 Axes><img width="766" height="547" alt="image" src="https://github.com/user-attachments/assets/70b2967b-9d1b-41b2-990d-085ca24615a0" />



Overall, this CNN demonstrates robust feature extraction and classification capabilities for brain tumor detection, showing real-world potential for assisting radiologists in diagnostic workflows.

