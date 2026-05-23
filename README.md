# Butterfly Image Classification using CNN

A Convolutional Neural Network (CNN) built with TensorFlow/Keras to classify butterfly images into their respective species categories. The model is trained on labeled images and generates predictions for unseen test images.

---

## Repository Structure

```
butterfly-cnn/
├── Butterfly Image Classification using CNN.ipynb   # Main notebook
├── butterfly_test_predictions.csv                   # Model predictions on test set
├── requirements.txt                                 # Python dependencies
└── README.md
```

> **Note:** The `train/`, `test/`, `Training_set.csv`, and `Testing_set.csv` files are not included in this repository. Download them directly from the dataset source below.

---

## Dataset

**Source:** [Butterfly Image Classification – Kaggle](https://www.kaggle.com/datasets/phucthaiv02/butterfly-image-classification)

After downloading, place the files so the structure looks like this:

```
butterfly-cnn/
├── train/                  # Training images
├── test/                   # Test images
├── Training_set.csv        # Image filenames + labels
├── Testing_set.csv         # Image filenames (no labels)
├── Butterfly Image Classification using CNN.ipynb
├── butterfly_test_predictions.csv
└── requirements.txt
```

---

## 🧠 Model Architecture

A sequential CNN with the following layers:

| Layer | Details |
|---|---|
| Conv2D | 32 filters, 3×3, ReLU |
| MaxPooling2D | 2×2 |
| Conv2D | 64 filters, 3×3, ReLU |
| MaxPooling2D | 2×2 |
| Conv2D | 128 filters, 3×3, ReLU |
| MaxPooling2D | 2×2 |
| Flatten | — |
| Dense | 256 units, ReLU |
| Dropout | 0.5 |
| Dense (Output) | N classes, Softmax |

- **Input image size:** 128 × 128 × 3
- **Optimizer:** Adam
- **Loss:** Categorical Crossentropy
- **Epochs:** 10 | **Batch size:** 32

---

## Setup & Usage

**1. Clone the repository**
```bash
git clone https://github.com/YOUR_USERNAME/butterfly-cnn.git
cd butterfly-cnn
```

**2. Install dependencies**
```bash
pip install -r requirements.txt
```

**3. Download the dataset**

Get it from [Kaggle](https://www.kaggle.com/datasets/phucthaiv02/butterfly-image-classification) and place `train/`, `test/`, `Training_set.csv`, `Testing_set.csv` in the project root.

**4. Run the notebook**

Open `Butterfly Image Classification using CNN.ipynb` in Jupyter and run all cells sequentially.

---

## Output

- Training and validation accuracy/loss curves plotted per epoch
- Predictions on the test set saved to `butterfly_test_predictions.csv`
- Top-3 predicted classes shown for sample test images

---

## Tech Stack

- Python 3.x
- TensorFlow / Keras
- scikit-learn
- NumPy
- Pandas
- Pillow
- Matplotlib

---
