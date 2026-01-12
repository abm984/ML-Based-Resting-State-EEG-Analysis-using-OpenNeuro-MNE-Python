# ML-Based-Resting-State-EEG-Analysis-using-OpenNeuro-MNE-Python
To analyze resting-state EEG signals and apply machine learning using frequency-domain features, without relying on event markers, following a fully reproducible research workflow.


# ML-Based Resting-State EEG Analysis using OpenNeuro

## 📌 Project Overview
This project demonstrates an **end-to-end machine learning pipeline for resting-state EEG analysis** using an open-access dataset from **OpenNeuro**.  
The focus is on **frequency-domain feature extraction** and **window-based classification**, implemented using **MNE-Python** and **scikit-learn**, and executed on **Google Colab**.

Since the dataset does not contain event markers, the project follows a **fixed-length epoching strategy**, which is a standard approach for resting-state EEG analysis.

---

## 🎯 Project Objective
To design and implement a reproducible workflow that:
- Processes raw resting-state EEG data
- Extracts meaningful frequency-band features
- Applies supervised machine learning for classification
- Demonstrates practical EEG–ML integration without relying on event annotations

---

## 🧠 Dataset
- **Source:** OpenNeuro  
- **Dataset ID:** `ds004504`  
- **Modality:** EEG  
- **Format:** BIDS-compliant  
- **Type:** Resting-state EEG (no task-based events)

📎 Dataset is accessed programmatically using the `openneuro-py` library.

---

## 🛠️ Tools & Technologies
- **Python**
- **MNE-Python** – EEG preprocessing and signal analysis
- **OpenNeuro** – Open-access neuroimaging datasets
- **scikit-learn** – Machine learning models
- **NumPy** – Numerical computing
- **Google Colab** – Execution environment

---

## 🔄 Methodology

### 1. Data Loading
- EEG data loaded using **MNE-BIDS**
- BIDS-compliant structure ensures reproducibility

### 2. Preprocessing
- Band-pass filtering (1–40 Hz)
- Average re-referencing

### 3. Epoching
- Continuous EEG segmented into **fixed-length overlapping windows**
- Window-based approach suitable for resting-state data

### 4. Feature Extraction
- Power Spectral Density (PSD) computed using Welch’s method
- Frequency band power extracted for:
  - Theta (4–8 Hz)
  - Alpha (8–13 Hz)
  - Beta (13–30 Hz)

### 5. Machine Learning
- Feature normalization
- Supervised classification using:
  - Support Vector Machine (SVM)
- Model evaluation using train–test split

---

## 📊 Results
- Successfully built a complete EEG–ML pipeline
- Demonstrated feasibility of ML on resting-state EEG without event markers
- Results intended for **methodological demonstration**, not clinical inference

---

## ⚠️ Important Notes
- This project **does not perform medical diagnosis**
- Labels are used for **experimental and educational purposes only**
- Results should not be interpreted as clinical findings

---


---

## 🚀 Future Improvements
- Cross-subject classification
- Advanced feature extraction (CSP, connectivity metrics)
- Cross-validation strategies
- Deep learning models (e.g., EEGNet)
- Physiological analysis of alpha dominance

---

## 📜 References
- Gramfort et al., *MNE for EEG and MEG analysis*, NeuroImage
- OpenNeuro: https://openneuro.org
- scikit-learn documentation

---

## 🤝 Acknowledgments
Thanks to the **OpenNeuro** and **MNE-Python** communities for providing open tools and datasets that make reproducible neuroscience research possible.

---

## 👤 Author
**Abdullah bin Masood**  
Machine Learning & Neuroinformatics Enthusiast

---

⭐ If you find this project useful, feel free to star the repository!

