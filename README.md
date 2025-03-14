# Voided Volume Classification with Machine Learning

## 📌 Project Overview
This project presents a machine learning-based approach for **voided urine volume classification** using **audio signals**. The study focuses on **non-invasive uroflowmetry** using sound recordings, eliminating the need for conventional uroflowmeters. We extract **frequency-based features** from audio and use classification models to estimate **urine volume** accurately.

## 🏗️ Methodology
1. **Data Collection**
   - Recorded urine flow sounds using a **4-channel microphone** at **96 kHz**.
   - Simulated urination using a **syringe method** to standardize recordings.
   - Two datasets were created:
     - **Original Audio Dataset**
     - **Augmented Dataset** (using polarity inversion, gain adjustments, and noise addition)

2. **Feature Extraction**
   - **Fast Fourier Transform (FFT)** – Captures frequency spectrum features.
   - **Mel-frequency Cepstral Coefficients (MFCC)** – Extracts essential sound patterns.

3. **Machine Learning Models**
   - **Support Vector Machine (SVM)**
   - **Random Forest (RF)**
   - **XGBoost (XGB)**
   - Models were trained using both **FFT** and **MFCC** features.

## 📊 Results & Performance
| Feature Extraction | Model | Accuracy (%) | F1-score (%) | AUC | 
|-------------------|----------|--------------|-------------|------|
| FFT | **XGBoost** | **91.66%** | **91.72%** | **0.91** |
| FFT | SVM | 83.33% | 83.33% | 0.83 |
| FFT | RF | 75.00% | 75.17% | 0.75 |
| MFCC | RF | **61.11%** | **61.48%** | 0.77 |
| MFCC | XGBoost | 66.66% | 57.14% | 0.61 |

- **XGBoost outperformed all models**, especially with FFT features.
- **Data augmentation** improved accuracy across all models.

## 🖥 Usage Guide
### Installation
1. **Clone the Repository**
   ```bash
   git clone https://github.com/moh701/Voided-Volume-Classification-with-Machine-Learning.git
   cd Voided-Volume-Classification-with-Machine-Learning
