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

## 🧹 ECG Preprocessing Techniques

The following preprocessing steps were applied to improve the quality of the ECG signal before analysis:

- **Baseline Wander Removal**  
  A high-pass filter eliminates slow, low-frequency drifts caused by respiration or body movement. This helps stabilize the ECG baseline.

- **High-Frequency Noise Suppression**  
  A low-pass filter is used to remove high-frequency artifacts, such as muscle noise or electrical interference, while preserving important cardiac features.

- **Power-Line Interference Removal**  
  A notch filter centered at 50 Hz (typical of power-line noise) effectively removes electrical interference without distorting the main ECG signal.

These steps significantly enhance signal clarity, enabling accurate QRS complex detection and heart rate calculation.

## 📊 Results

The preprocessing steps significantly improved the ECG signal quality and enabled accurate R-peak detection. Below is a visualization of each step from raw signal to QRS detection

<img width="1145" height="647" alt="ecg_implementation_results" src="https://github.com/user-attachments/assets/2fc280b8-7ff7-4f98-9d40-bd5b783d1bc1" />

**Figure:**
1. Raw ECG Signal  
2. After Baseline Wander Removal  
3. After High-Frequency Noise Removal  
4. After Power Line Interference Removal  
5. Smoothed Signal for R-Peak Detection  
6. Final Filtered ECG Signal with R-Peaks Marked

The pipeline results in a clear signal and accurate heart rate estimation using detected R-R intervals.







