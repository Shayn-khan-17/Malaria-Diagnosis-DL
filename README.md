# 🦠 Malaria Diagnosis Using Deep Learning

A deep learning-based image classification project for detecting malaria-infected cells from microscopic blood-cell images.

This project explores and compares three different deep learning architectures:

* **Convolutional Neural Network (CNN)**
* **CNN + LSTM**
* **Bidirectional LSTM (Bi-LSTM)**

All three models were trained for **50 epochs** and evaluated on a malaria cell image dataset.

---

## 📌 Project Overview

Malaria is a serious infectious disease caused by *Plasmodium* parasites and is commonly diagnosed by examining blood-smear images under a microscope.

This project investigates how deep learning can be used to automatically classify microscopic blood-cell images for malaria diagnosis.

The main objective is to experiment with different neural network architectures and compare their ability to learn meaningful features from malaria cell images.

### Models Implemented

| Model        | Description                                                                                    |
| ------------ | ---------------------------------------------------------------------------------------------- |
| **CNN**      | Extracts spatial features directly from microscopic cell images                                |
| **CNN-LSTM** | Combines CNN-based spatial feature extraction with LSTM-based sequence modeling                |
| **Bi-LSTM**  | Uses bidirectional LSTM layers to process extracted feature representations in both directions |

---

## 🧠 Deep Learning Architectures

### 1. Convolutional Neural Network (CNN)

The CNN model is designed to learn spatial patterns and visual features from malaria cell images.

A CNN is particularly suitable for image classification because convolutional layers can automatically learn features such as:

* Cell shapes
* Textures
* Structural patterns
* Parasite-related visual characteristics

---

### 2. CNN-LSTM

The CNN-LSTM architecture combines convolutional feature extraction with recurrent sequence modeling.

The general pipeline is:

```text
Input Image
     ↓
CNN Feature Extraction
     ↓
Feature Representation
     ↓
LSTM
     ↓
Classification
```

The CNN extracts visual features while the LSTM processes the resulting feature representation.

---

### 3. Bidirectional LSTM (Bi-LSTM)

The Bi-LSTM architecture processes sequential feature representations in both forward and backward directions.

```text
Input Features
      ↓
  Bi-LSTM
   ↙    ↘
Forward  Backward
   ↘    ↙
 Feature Representation
      ↓
 Classification
```

This allows the model to use information from both directions when learning relationships within the extracted features.

---

## 📂 Repository Structure

```text
Malaria-Diagnosis-DL/
│
├── BI_LSTM.ipynb
├── CNN model.ipynb
├── CNNLSTM 50.ipynb
└── README.md
```

### Notebooks

**`CNN model.ipynb`**

Contains the implementation and training process for the CNN-based malaria classification model.

**`CNNLSTM 50.ipynb`**

Contains the CNN-LSTM architecture and training experiments.

**`BI_LSTM.ipynb`**

Contains the Bidirectional LSTM model implementation and training experiments.

---

## 📊 Dataset

The models are trained using a **malaria cell image dataset** containing microscopic blood-cell images.

The classification task is based on identifying whether a cell image belongs to the malaria-related class or the corresponding non-malaria/healthy class, depending on the dataset labeling.

> **Note:** The dataset itself is not included in this repository. You should download the dataset separately and update the dataset path inside the notebooks before training.

---

## ⚙️ Technologies Used

* Python
* TensorFlow / Keras
* NumPy
* Pandas
* Matplotlib
* Jupyter Notebook
* Convolutional Neural Networks
* LSTM
* Bidirectional LSTM
* Deep Learning
* Computer Vision

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/Shayn-khan-17/Malaria-Diagnosis-DL.git
cd Malaria-Diagnosis-DL
```

### 2. Create a Virtual Environment

```bash
python -m venv venv
```

Activate it on Linux/macOS:

```bash
source venv/bin/activate
```

On Windows:

```bash
venv\Scripts\activate
```

### 3. Install Dependencies

Install the required Python packages:

```bash
pip install tensorflow numpy pandas matplotlib jupyter
```

You can also install additional packages required by the notebooks if they are used in your environment.

### 4. Start Jupyter Notebook

```bash
jupyter notebook
```

Open one of the notebooks:

```text
CNN model.ipynb
CNNLSTM 50.ipynb
BI_LSTM.ipynb
```

### 5. Configure the Dataset

Update the dataset path in the notebook so that it points to the location where your malaria cell dataset is stored.

---

## 🏋️ Training

The models in this project were trained for **50 epochs**.

The general training workflow is:

```text
Dataset
   ↓
Image Preprocessing
   ↓
Train / Validation Split
   ↓
Model Construction
   ↓
Model Training
   ↓
Validation
   ↓
Performance Evaluation
```

---

## 📈 Model Comparison

The project is designed to compare different deep learning approaches for malaria cell classification.

| Model    | Feature Extraction            | Sequence Modeling | Training  |
| -------- | ----------------------------- | ----------------- | --------- |
| CNN      | CNN                           | No                | 50 epochs |
| CNN-LSTM | CNN                           | LSTM              | 50 epochs |
| Bi-LSTM  | Neural feature representation | Bi-LSTM           | 50 epochs |

For a more meaningful comparison, the models can be evaluated using:

* Accuracy
* Precision
* Recall
* F1-score
* Confusion Matrix
* Training Loss
* Validation Loss
* ROC-AUC

---

## 🔬 Future Improvements

Possible improvements to this project include:

* [ ] Add transfer learning using ResNet, EfficientNet, DenseNet, or MobileNet
* [ ] Apply data augmentation
* [ ] Perform hyperparameter optimization
* [ ] Add confusion matrices for all models
* [ ] Add precision, recall, and F1-score
* [ ] Compare ROC-AUC scores
* [ ] Add training/validation accuracy graphs
* [ ] Add training/validation loss graphs
* [ ] Perform cross-validation
* [ ] Deploy the best-performing model as a web application
* [ ] Add explainable AI techniques such as Grad-CAM
* [ ] Compare CNN/LSTM models with modern vision transformers

---

## ⚠️ Disclaimer

This project is intended for **educational and research purposes only**.

The predictions generated by these models should **not be considered a medical diagnosis**. Clinical diagnosis should be performed by qualified healthcare professionals using appropriate laboratory and diagnostic procedures.

---

## 👨‍💻 Author

**Shayan Khan**

Computer Science Student
Interested in Deep Learning, Computer Vision, Machine Learning, and AI-based Medical Image Analysis.

### GitHub

[Shayn-khan-17](https://github.com/Shayn-khan-17)

---

## ⭐ Support

If you find this project useful for learning or research, consider giving the repository a ⭐ on GitHub.

---

## 📄 License

This project does not currently specify a license. If you want others to freely use, modify, and distribute the code, consider adding an appropriate open-source license such as MIT.
