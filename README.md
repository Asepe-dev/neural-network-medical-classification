# Neural Network Medical Classification

## Overview

This project demonstrates the implementation of an Artificial Neural Network (ANN) using TensorFlow/Keras and compares its performance with a traditional machine learning model from Scikit-Learn.

The dataset used is the Breast Cancer Wisconsin Dataset, which is included in Scikit-Learn and contains medical measurements used to classify tumors as malignant or benign.

---

## Objectives

The objectives of this project are:

1. Build a Sequential Neural Network with:
   - Input layer
   - Hidden layer containing 64 neurons with ReLU activation
   - Output layer with Sigmoid activation

2. Train the model for 50 epochs.

3. Plot training and validation loss curves.

4. Compare the Neural Network with a Scikit-Learn model (Random Forest Classifier).

5. Experiment with:
   - Additional hidden layers
   - Different numbers of neurons
   - Dropout regularization

6. Evaluate whether Neural Networks are worth the added complexity compared to traditional machine learning algorithms.

---

## Dataset

### Breast Cancer Wisconsin Dataset

Source:
Scikit-Learn Built-in Dataset

Characteristics:

- 569 samples
- 30 numerical features
- Binary classification problem
- Target classes:
  - Malignant
  - Benign

The dataset is loaded directly using:

```python
from sklearn.datasets import load_breast_cancer
```

No external downloads are required.

---

## Data Preprocessing

The following preprocessing steps were performed:

- Dataset loading
- Train-test split (80/20)
- Feature standardization using StandardScaler

---

## Neural Network Architecture

The baseline model consists of:

- Input Layer
- Dense Hidden Layer
  - 64 neurons
  - ReLU activation
- Output Layer
  - 1 neuron
  - Sigmoid activation

Loss Function:

- Binary Crossentropy

Optimizer:

- Adam

Metrics:

- Accuracy

---

## Training

The model was trained for 50 epochs with a validation split of 20%.

Training and validation losses were recorded and visualized using Matplotlib.

---

## Model Comparison

The Neural Network was compared against a Random Forest Classifier from Scikit-Learn.

Evaluation metric:

- Accuracy

The comparison allows assessment of whether the additional complexity of Neural Networks provides a significant advantage on structured medical datasets.

---

## Experiments

Three modifications were tested:

### Experiment 1
Added an additional hidden layer.

### Experiment 2
Increased hidden neurons from 64 to 128.

### Experiment 3
Added a Dropout layer (30%) to reduce overfitting.

The performance of each model was compared against the baseline Neural Network and Random Forest model.

---

## Results

Results showed the effect of architectural changes on classification accuracy and model generalization.

Screenshots of:
- Model architecture
- Loss curves
- Accuracy comparison
- Experimental results

are included in the `screenshots` folder.

---

## Technologies Used

- Python
- Google Colab
- TensorFlow / Keras
- Scikit-Learn
- NumPy
- Pandas
- Matplotlib

---

## Repository Structure

```
neural-network-medical-classification/
│
├── Neural_Network.ipynb
├── README.md
└── screenshots/
    ├── model_summary.png
    ├── loss_curve.png
    ├── comparison_table.png
    └── experiment_results.png
```

---

## Conclusion

This project demonstrates how Artificial Neural Networks can be implemented for medical classification tasks and compared with traditional machine learning approaches. While Neural Networks offer flexibility and strong predictive capabilities, simpler models such as Random Forests can often achieve competitive performance on structured datasets with lower computational complexity.
