# 📊 Time-Series Modeling & Evaluation Sandbox  
### 🎯 Methodologically Correct Modeling of Dependent, Nonstationary Data  

`Python` • `NumPy` • `Pandas` • `SciPy` • `Statsmodels` • `scikit-learn` • `PyWavelets`

---

## 🔍 1 — What This Repo Contains

This project is a **research-oriented sandbox** for experimenting with **statistically principled modeling and evaluation of time-indexed data**. The emphasis is not on any specific application domain, but on **how to handle dependence, nonstationarity, event definition, labeling, and validation correctly**.

The entire pipeline lives in a single notebook: **`Quant_AI.ipynb`**, and implements:

- 🧹 **Data loading & preprocessing** for time-indexed data  
- 📉 **Stationarity & memory control** using log transforms and **fractional differencing (FFD)**  
- ⚡ **Event-based sampling** using **CUSUM filtering** to reduce redundancy in dense time series  
- 🏷️ **Leakage-aware labeling** with finite-horizon events and vertical barriers  
- 🧪 **Proper cross-validation** using **Purged K-Fold with an embargo** to avoid overlap-based leakage  
- 🧱 **Feature engineering** capturing:
  - volatility and scale structure  
  - frequency-domain structure (e.g., **wavelet energy**, **spectral entropy**)  
  - complexity and regime-like behavior (e.g., **Lempel–Ziv complexity**)  
- 🧠 **Baseline modeling** using Random Forests and simple neural networks  
- ⚙️ **Scalable computation** with multiprocessing for feature construction  

> 💡 The focus is **methodological correctness and experimental design**, not any specific application result.

---

## 🧠 2 — What This Project Emphasizes (Statistics-First)

This notebook is built around several **core statistical issues in time-series modeling**:

- 🧮 **Dependence & nonstationarity**
  - Fractional differencing to reduce long memory while preserving information  
  - Simple ADF-based diagnostics to guide differencing choices  

- ⏱️ **Event-driven representations**
  - CUSUM filters to convert dense time series into an information-driven event sequence  

- 🛡️ **Leakage-resistant evaluation**
  - **Purged cross-validation + embargo** to ensure labels that extend forward in time do not contaminate training data  

- 📐 **Feature construction for temporal structure**
  - Rolling, volatility, spectral, and complexity-based descriptors  

- ♻️ **Reproducible computational workflow**
  - Modular feature functions and parallel computation for large-scale experiments  

---

## 🧱 3 — High-Level Pipeline

1. 📥 Load and clean time-indexed data  
2. 📉 Apply stationarity and memory-control transforms (log, FFD)  
3. ⚡ Detect events using CUSUM filtering  
4. 🏷️ Define and label finite-horizon events  
5. 🧱 Construct rolling and structural features  
6. 🤖 Train baseline models  
7. 🧪 Evaluate using **purged cross-validation with embargo**

> 🔬 Models are intentionally simple. The focus is on **experimental design and statistical validity**, not model complexity.

---

## 🧭 4 — Possible Extensions

- 📊 Add probabilistic or Bayesian models  
- 📏 Add uncertainty quantification and calibration analysis  
- 🔄 Add diagnostics for distribution shift and structural change  
- 📚 Study theoretical properties of the sampling and labeling schemes
  
---
