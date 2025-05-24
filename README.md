
# Efficient and Adaptive Multi-Feature Anomaly Detection in WBANs

This repository contains the implementation and research related to **Efficient and Adaptive Multi-Feature Anomaly Detection in Wireless Body Area Networks (WBANs)**, a project conducted at the National Institute of Technology Karnataka.

## 📌 Abstract

WBANs (Wireless Body Area Networks) enable real-time health monitoring using wearable sensors. However, challenges like high false-positive alerts and resource constraints limit their practical deployment. This project presents a hybrid anomaly detection framework integrating an optimized **ConvLSTM** model and **Fuzzy Logic-based adaptive thresholding**. The approach captures spatial-temporal dependencies and dynamically adjusts detection sensitivity, ensuring accurate and efficient anomaly detection with minimal false positives.

## 🚀 Features

- ✅ Optimized ConvLSTM architecture for temporal-spatial anomaly detection
- ✅ Adaptive thresholding using Fuzzy Logic based on historical data variance
- ✅ High precision and recall with reduced computational overhead
- ✅ Real-time anomaly classification suitable for resource-constrained environments

## 🧠 Methodology

### 1. Data Preprocessing
- Physiological signals: Heart rate, blood pressure, SpO2, respiratory rate, and body temperature
- Normalization using `StandardScaler`
- Sliding window generation for time-series data

### 2. ConvLSTM Model
- Two ConvLSTM2D layers (256 & 128 filters)
- Dropout regularization to prevent overfitting
- Final Dense layer with sigmoid activation for binary classification

### 3. Adaptive Thresholding
- Fuzzy logic system adjusts the anomaly detection threshold dynamically
- Based on variance in recent physiological data
- Rules applied for low/medium/high variance to reduce false positives

### 4. Evaluation
- Metrics: Accuracy, Precision, Recall, F1-score, AUC
- ROC curve analysis for visual evaluation

## 📊 Results

| Model                              | Accuracy | Precision | Recall | F1 Score | AUC   |
|-----------------------------------|----------|-----------|--------|----------|--------|
| **Proposed (ConvLSTM + Fuzzy)**   | 99.38%   | 99.67%    | 99.50% | 99.59%   | 0.996 |
| ConvLSTM + Variance + Deviation   | 93.76%   | 99.54%    | 92.08% | 95.66%   | 0.973 |
| LSTM (no fuzzy logic)             | 93.10%   | 99.56%    | 91.06% | 95.12%   | 0.972 |
| CNN (no fuzzy logic)              | 88.72%   | 93.88%    | 90.83% | 92.33%   | 0.910 |

## 🗂️ Dataset

- Simulated physiological data from wearable sensors
- Features:
  - Heart Rate (HR)
  - Blood Pressure (BP)
  - Oxygen Saturation (SpO₂)
  - Respiratory Rate (RR)
  - Body Temperature
- Labels: `0` = Normal, `1` = Anomaly

## 📚 Related Work

The paper compares the proposed method against state-of-the-art techniques including:
- LSTM and CNN models
- Transformer-based architectures
- GANs for WBAN anomaly detection
- Convolutional Autoencoders

## 📈 Visuals

ROC curves demonstrate superior performance of the proposed method in terms of true positive rate and specificity.

## 📌 Conclusion

- Adaptive fuzzy logic significantly reduces false positives.
- ConvLSTM effectively captures complex temporal-spatial patterns in health data.
- The model is lightweight, efficient, and ideal for real-time WBAN deployments.

## 🛠 Future Work

- Incorporate additional features like ambient data or activity tracking
- Real-world deployment and testing in clinical scenarios
- Explore Transformer-based models and hardware optimization

## 👨‍💻 Authors

- Ajit Bhandari – [ajitbhandari.211cs102@nitk.edu.in](mailto:ajitbhandari.211cs102@nitk.edu.in)
- Aryan Gupta – [aryangupta.211cs108@nitk.edu.in](mailto:aryangupta.211cs108@nitk.edu.in)
- Chanddan H – [chanddanh.211cs113@nitk.edu.in](mailto:chanddanh.211cs113@nitk.edu.in)

## 📄 License

This project is for academic and research purposes only. Please cite appropriately if used.
