# Image Classification with Preprocessing

## Project Overview
This project focuses on **image classification** using deep learning models, specifically **ResNet** and **VGG16**. The dataset consists of a basic set of images used for training, and the trained model is later used for classifying new images. The project explores the impact of different architectures on training and validation accuracy.

## 📂 Dataset
- The dataset comprises images belonging to multiple classes.
- Preprocessing techniques such as **resizing, normalization, and data augmentation** are applied to improve generalization.

## 🏗️ Models Used
### 1️⃣ **ResNet**
- A deep residual network known for its skip connections that help in training deep architectures.
- **Training Observations:**
  - Training accuracy kept increasing.
  - Validation accuracy fluctuated, showing inconsistency.
  - Possible **overfitting** or improper learning rate scheduling.

### 2️⃣ **VGG16**
- A classic CNN architecture with **16 layers**, known for its simplicity and strong feature extraction.
- **Training Observations:**
  - Training accuracy steadily increased.
  - Validation accuracy improved initially but later started decreasing (**overfitting**).
  - Potential improvements: **regularization, dropout, or data augmentation**.

## ⚙️ Preprocessing Steps
- **Image Resizing**: Standardized input size for the models.
- **Normalization**: Pixel values scaled between 0 and 1.
- **Data Augmentation**: Random rotations, flips, and zooms to enhance generalization.

## 🏋️ Training Details
- **Optimizer**: Adam
- **Loss Function**: Categorical Crossentropy
- **Batch Size**: 32
- **Epochs**: 50 (Can be adjusted)
- **Validation Split**: 20%

## 📈 Results & Insights
- **ResNet** tends to struggle with generalization due to **fluctuating validation accuracy**.
- **VGG16** exhibits clear **overfitting** where validation accuracy declines after a certain epoch.
- **Next Steps:**
  - Implement **Dropout and Batch Normalization**.
  - Experiment with **learning rate scheduling**.
  - Use **more diverse datasets** to improve generalization.

## 🛠️ How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/ShreyaSari/image-classification-and-pre-processing.git
   cd image-classification
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Train the model:
   ```bash
   python train.py --model resnet
   ```
   or
   ```bash
   python train.py --model vgg16
   ```
4. Classify an image:
   ```bash
   python classify.py --image sample.jpg
   ```

## 🎯 Future Enhancements
- Implement **EfficientNet** for comparison.
- Add **Explainability Methods (Grad-CAM, SHAP)**.
- Deploy the model as a **web app using Flask/FastAPI**.

---
✨ **Made with ❤️ by Shreya Sari** ✨

