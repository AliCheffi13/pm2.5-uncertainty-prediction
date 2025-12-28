# Probabilistic PM2.5 Forecasting with LSTM

## Overview

This project explores the use of a **probabilistic LSTM model** to forecast **PM2.5 air pollution levels** using historical meteorological data.  
The objective is not to build a production-ready system, but to understand and experiment with:

- Sequential modeling using deep learning
- Uncertainty-aware predictions
- Real-world time-series data challenges
- Model evaluation under imperfect and noisy conditions

The project was developed as a learning-focused research prototype.

---

## Project Structure

├── notebook/
│ └── pm25_lstm_uncertainty.ipynb
│
├── models/
│ └── best_model.pt
│
├── data/
│ └── README.md
│
├── requirements.txt
└── README.md

---

## Dataset

- Source: **Beijing PM2.5 Dataset (UCI Machine Learning Repository)**
- Temporal resolution: hourly
- Target variable: **PM2.5 concentration**
- Input features: meteorological variables (temperature, pressure, wind direction, etc.)

The dataset contains realistic noise and missing values, which are handled explicitly during preprocessing.

---

## Model Description

The model is based on an **LSTM (Long Short-Term Memory)** architecture and predicts:

- **μ (mean)**: expected PM2.5 value
- **σ (uncertainty)**: predictive uncertainty

Training uses a **Gaussian Negative Log-Likelihood loss**, enabling the model to express confidence rather than only point estimates.

This approach simulates a _virtual sensor_, useful in contexts where physical sensors are unavailable or unreliable.

---

## Training Strategy

- Sliding window sequence generation
- Feature normalization based on training data only
- Early stopping and learning rate scheduling
- GPU-compatible training (if available)

The goal is to observe learning behavior rather than maximize benchmark performance.

---

## Results & Observations

- The model successfully learns temporal trends.
- Performance degrades for extreme pollution values, highlighting real-world complexity.
- Uncertainty estimates reflect prediction instability in noisy regions.

These limitations are expected and are treated as part of the experimental learning process.

---

## Limitations and Future Work

Possible improvements include:

- Larger datasets or multi-city training
- Attention mechanisms
- Bayesian or ensemble-based uncertainty estimation

---

## How to Run

```bash
pip install -r requirements.txt
jupyter notebook
```

Open the notebook located in the notebook/ directory and follow the execution order.
