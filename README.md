# Digital Signal Processing(DSP) project
# 🩺 ECG Signal Preprocessing (MATLAB)

This project focuses on preprocessing raw ECG (Electrocardiogram) signals using MATLAB. The goal is to clean the signals by removing various types of noise such as baseline wander, power line interference, and high-frequency artifacts. Preprocessing enhances signal quality and prepares the data for further analysis like QRS detection or classification tasks.This system was developed as part of the DSP course project under the guidance of Dr. Prabhakar Manage.

---

## 📌 Features

- ✅ Baseline Wander Removal  
- ✅ Power Line Interference Suppression (Notch Filter)  
- ✅ Bandpass Filtering (Low-pass & High-pass)  
- ✅ Normalization and Smoothing  
- ✅ Plotting of Raw vs. Processed ECG Signals  

---

## 🧠 Motivation

ECG signals often contain noise due to patient movement, electrode contact issues, and electrical interference. Preprocessing is a crucial first step in biomedical signal analysis to ensure accurate diagnostics and robust machine learning models.

---

## 🛠️ Tools & Technologies

- MATLAB R2023a (or any compatible version)
- Signal Processing Toolbox
- Sample ECG data (e.g., MIT-BIH dataset or MATLAB-simulated ECG)

---

# 🔬 Methodology

The ECG signal preprocessing pipeline involves the following stages:

1. **Data Acquisition**  
   - ECG signal is loaded from a `.mat` file (`rec_5.mat`) at a sampling rate of 500 Hz.
   - The signal is preprocessed for a sample window of 4000 data points.

2. **Preprocessing**  
   - Noise and artifacts are removed using three main filters:
     - High-pass (Baseline wander)
     - Low-pass (High-frequency noise)
     - Notch (Power-line interference)

3. **QRS Detection**  
   - Derivative, rectification, and smoothing are applied to highlight the QRS complex.
   - `findpeaks` function detects R-peaks.

4. **Heart Rate Calculation**  
   - Time between successive R-peaks is measured and converted to beats per minute (BPM).




