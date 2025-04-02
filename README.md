# Micro Gas Turbine Electrical Power Prediction using Physics-Guided Attention-Bidirectional LSTM

---

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE) [![Python](https://img.shields.io/badge/Python-3.9%2B-blue)](https://www.python.org/) [![TensorFlow](https://img.shields.io/badge/TensorFlow-2.12%2B-orange)](https://www.tensorflow.org/)

This repository contains the implementation of a deep learning-based predictive model for **electrical power output forecasting** of a 3kW commercial micro gas turbine. The proposed model integrates:
- Physics-Guided Feature Engineering
- Bidirectional LSTM Encoder
- Attention Mechanism
- Smoothness-Aware Loss Function
- Uncertainty Quantification (Monte Carlo Dropout)

---

## Repository Structure
├── data/ # Contains train.zip and test.zip
├── notebooks/ # Jupyter Notebook(s) for training and evaluation 


---

## Dataset
- Sequential, Multivariate, Time-Series
- ~71,000 instances
- 8 experiments covering various gas turbine operating scenarios

Source: Bielski et al., *Knowledge-Guided Learning of Temporal Dynamics and its Application to Gas Turbines*, ACM e-Energy 2024

---

## Model Components
- Bidirectional LSTM Encoder
- Self-Attention Layer
- Dense Regression Head
- Smoothness Regularization
- MC-Dropout for Uncertainty

---

## Results Summary
| Metric | Value |
|--------|-------|
| RMSE | 0.19 W |
| MAE | 0.12 W |
| R² | 0.8128 |
| Smoothness Penalty | 0.32 |

---

## Requirements
- Python ≥ 3.9
- TensorFlow ≥ 2.12
- scikit-learn ≥ 1.0
- pandas, numpy, matplotlib

## Key Features
- Physics-Aware Features (Derivative, Time-Since-Change)
- Attention Mechanism for transition detection
- Uncertainty bands using MC-Dropout
- Transition vs Steady-State RMSE comparison

## Citation
@inproceedings{bielski2024knowledge,
  title={Knowledge-Guided Learning of Temporal Dynamics and its Application to Gas Turbines},
  author={Bielski, Pawel and others},
  booktitle={ACM e-Energy},
  year={2024}
}
