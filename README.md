# EEG Emotion Analysis using the DEAP Dataset (Valence & Arousal)

This project explores the relationship between EEG signals and emotional states (valence & arousal) using the **DEAP (Database for Emotion Analysis using Physiological Signals)** dataset. By applying Discrete Wavelet Transform (DWT), the study captures both frequency-specific and spatial patterns of brain activity linked to emotions.

##  Project Overview

- 📊 **Dataset:** DEAP (32-channel EEG recordings across 40 trials per subject)  
- 📉 **Data Scope:** Analysis performed on a subset of **10 subjects** using **EEG-only signals (32 channels)**  
- ⚙️ **Preprocessing:** Verified dataset quality (no additional filtering required)  
- 🔍 **Feature Extraction:** Multi-resolution analysis using **Discrete Wavelet Transform (DWT - db4)**  
- 🧠 **Objective:** Identify EEG patterns correlated with emotional dimensions — **Valence** and **Arousal**  

The analysis focuses specifically on **Valence** and **Arousal** emotion dimensions using EEG signals to understand how different brain regions and frequency bands contribute to emotional responses.

---
##  Methodology

### 1. Data Validation
- Checked signal integrity, shapes, and label ranges  
- Verified frequency content using Power Spectral Density (PSD) analysis  

### 2. Feature Extraction
- Applied **Discrete Wavelet Transform (DWT - db4)**  
- Extracted **sub-band energy features (A5–D1)**  

### 3. Multi-Level Analysis
- **Channel-wise analysis** → Identify emotion-sensitive electrodes  
- **Region-wise analysis** → Compare brain regions (frontal, temporal, etc.)  
- **Band-wise analysis** → Understand frequency contributions  
- **Subject-wise analysis** → Evaluate consistency across individuals  

---

## 📈 Key Findings

-  **Valence** is strongly associated with **mid-frequency bands (D3, D4)**  
-  **Arousal** shows stronger patterns in **higher frequency bands (D1, D2)**  
-  Emotional information is **not uniformly distributed** across EEG channels  
-  **Temporal and frontal regions** are particularly informative  
-  Results show **consistent trends across subjects**, despite variability  

---

##  Results

### 📊 Time-Frequency Analysis

<p align="center">
  <img src="results/time- frequency analysis _Valence.png" width="45%"/>
  <img src="results/Time Frequency analysis_Arousal.png" width="45%"/>
</p>
 
Illustrates how energy distribution varies across frequency bands, showing distinct patterns for emotional dimensions.

---

###  Region-wise Analysis

<p align="center">
  <img src="results/Region Wise Analysis_Arousal.png" width="45%"/>
  <img src="results/Region Wise Analysis_Valence.png" width="45%"/>
</p>

Highlights how different brain regions (frontal, temporal, etc.) contribute differently to arousal and valence.

---

### 📈 Channel Importance

<p align="center">
  <img src="results/Highly correlated channels with Arousal.png" width="45%"/>
  <img src="results/Top correlated channels with Valence.png" width="45%"/>
</p>

Identifies the most emotion-sensitive EEG channels for both arousal and valence.

---

### 🤖 Model Performance

<p align="center">
  <img src="results/Best Moel _XGBoost_Confusion Matrix for Arousal.png" width="45%"/>
</p>

Demonstrates classification performance, showing  prediction accuracy for emotional states.

---

### 📊 Region Sensitivity Overview

<p align="center">
  <img src="results/Region wise emotion sensitivity.png" width="45%"/>
</p>

Compares overall contribution of brain regions to emotional processing.

---

##  Conclusion

This project demonstrates that emotional states such as **valence and arousal** can be effectively characterized using EEG signals through **time-frequency analysis**. The use of DWT enables capturing both temporal and spectral features, revealing that different frequency bands and brain regions contribute distinctly to emotional processing. These findings highlight the potential of EEG-based approaches for **affective computing and real-world emotion recognition systems**.

---

##  Future Work

- Extract more features and apply machine learning models for emotion classification  
- Integrate more data and explore deep learning approaches (CNN/LSTM)  
- Integrate multimodal signals (EDA, ECG)  


---

## Notes on Dataset Availability

The DEAP dataset is **not included** in this repository due to licensing restrictions.

To run the notebook:
1. Download the DEAP dataset from the official source
2. Update the dataset path inside the notebook where indicated
3. Run cells sequentially

---

## Requirements

Typical Python dependencies:
- numpy
- scipy
- matplotlib
- pywavelets
- pandas

---

## Author

Khadija Khan  
Biomedical Engineer
