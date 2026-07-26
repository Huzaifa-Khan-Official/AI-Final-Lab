# Handwritten Digit Recognition using CNN

## Project Title
**Handwritten Digit Recognition using Convolutional Neural Networks (CNN) on MNIST Dataset**

---

## Objective
To build a deep learning model using Convolutional Neural Networks (CNN) that can accurately recognize and classify handwritten digits (0–9) from the MNIST dataset. The model leverages spatial feature extraction through Conv2D and MaxPooling layers to achieve high classification accuracy (~99%).

---

## Dataset
- **Name:** MNIST (Modified National Institute of Standards and Technology)
- **Source:** Loaded directly via `tensorflow.keras.datasets.mnist`
- **Training samples:** 60,000 grayscale images (28×28 pixels)
- **Test samples:** 10,000 grayscale images (28×28 pixels)
- **Classes:** 10 (digits 0 through 9)

---

## Model / Algorithm
**Convolutional Neural Network (CNN)**

Architecture:
```
Input (28×28×1)
  → Conv2D(32 filters, 3×3, ReLU)
  → MaxPooling2D(2×2)
  → Conv2D(64 filters, 3×3, ReLU)
  → MaxPooling2D(2×2)
  → Flatten
  → Dense(64, ReLU)
  → Dropout(0.2)
  → Dense(10, Softmax)   ← Output
```

---

## Installation Steps

### 1. Clone the Repository
```bash
git clone https://github.com/Huzaifa-Khan-Official/<repo-name>.git
cd <repo-name>
```

### 2. Create a Virtual Environment (Recommended)
```bash
python -m venv venv

# Windows
venv\Scripts\activate

# macOS / Linux
source venv/bin/activate
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

---

## Required Libraries

| Library | Version | Purpose |
|---|---|---|
| tensorflow | >=2.13.0 | CNN model building & training |
| numpy | >=1.24.0 | Array operations |
| matplotlib | >=3.7.0 | Plotting training curves & predictions |

All dependencies are listed in `requirements.txt`.

---

## How to Run the Project

### Option A — Jupyter Notebook (Recommended)
```bash
jupyter notebook handwritten_digit_recognition.ipynb
```
Run all cells top to bottom (`Cell → Run All`).

### Option B — Google Colab
1. Upload `handwritten_digit_recognition.ipynb` to [colab.research.google.com](https://colab.research.google.com)
2. Click **Runtime → Run all**
3. MNIST dataset downloads automatically (~11 MB)

---

## Expected Output

```
Training data shape: (60000, 28, 28)
Test data shape:     (10000, 28, 28)
Reshaped training data: (60000, 28, 28, 1)

Training the model...
Epoch 1/10 - accuracy: ~0.96
...
Epoch 10/10 - accuracy: ~0.99

Test Loss:     ~0.03
Test Accuracy: ~0.9900 (99.00%)

Predictions vs Actual Labels:
Predicted: [7 2 1 0 4 1 4 9 5 9]
Actual:    [7 2 1 0 4 1 4 9 5 9]
Match:     [True True True True True True True True True True]
```

**Generated files:**
- `training_history.png` — accuracy & loss curves over epochs
- `predictions.png` — 2×5 grid of test digits with predicted labels
- `mnist_cnn_model.h5` — saved trained model

---

## Project Structure

```
├── handwritten_digit_recognition.ipynb          # Main Jupyter Notebook (with outputs)
├── requirements.txt         # Python dependencies
├── README.md                # This file
├── Project_Report.pdf       # Full project report
├── training_history.png     # Generated: training curves
├── predictions.png          # Generated: prediction grid
└── mnist_cnn_model.h5       # Generated: saved model
```

---

## Results Summary

| Metric | Value |
|---|---|
| Test Accuracy | ~99% |
| Test Loss | ~0.03 |
| Epochs | 10 |
| Batch Size | 128 |
| Optimizer | Adam |

---

## Group Members

| Name | Seat No. |
|---|---|
| MUHAMMAD HUZAIFA | B23110006102 |
| AHMED ABBASI | B23110006007 |
| MUZAMMIL HUSSAIN | B23110006130 |
| MAAZ NAEEM MALLICK | B23110006059 |

---

## License
This project is submitted as Final Lab for Artifical Intelligence Semester Course at UBIT.
