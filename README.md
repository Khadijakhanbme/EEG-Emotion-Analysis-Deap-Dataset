# EEG Emotion Analysis using the DEAP Dataset (Valence & Arousal)

This repository contains a signal processing and analysis workflow using EEG
recordings from the **DEAP (Database for Emotion Analysis using Physiological Signals)** dataset.

The analysis focuses on **Valence** and **Arousal** emotion dimensions using **EEG-only**
signals (32 channels) from a subset of subjects (10 subjects), as required by the project.

Full code + detailed explanations are provided in the notebook below.

---

## Notebook

- **Main notebook (Google Colab / Jupyter):**  
  `notebooks/DEAP_dataset_signal_processing.ipynb`

This notebook includes:
- Dataset inspection and structure explanation
- EEG channel selection (32 EEG channels only)
- Signal trimming / formatting
- Wavelet transform–based analysis (time–frequency)
- Visualizations related to Valence and Arousal

---

## Dataset Overview (DEAP)

Each subject file contains:
- `data`: shape **(40 × 40 × 8064)** → 40 trials × 40 channels × 8064 samples
- `labels`: shape **(40 × 4)** → Valence, Arousal, Dominance, Liking (ratings 1–9)

According to official DEAP documentation:
- 32 EEG channels
- 8 peripheral physiological channels

---

## Notes on Dataset Availability

⚠️ The DEAP dataset is **not included** in this repository due to licensing restrictions.

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
- pandas (if used)

---

## Author

Khadija Khan  
Biomedical Engineer
