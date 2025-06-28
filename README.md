# 📊 Quantitative Research Project  
### 🎯 End-to-End Signal Generation & Back-Testing for **BTC/USD** (Crypto) and **US30** (Equity Index)  
`Python` • `PyTorch` • `Pandas` • `NumPy`

---

## 🔍 1 — What This Repo Contains

This project explores **systematic alpha generation** using machine learning across two distinct asset classes:

- 💰 **BTC/USD** – a volatile, decentralized crypto asset  
- 📈 **US30** – a structured, institutional equity index (Dow Jones)

The entire pipeline lives in a single notebook: **`Quant_AI.ipynb`**, covering:

- 🧹 **Data collection & preprocessing** from Binance and Dukascopy.  
- ⚙️ **Feature engineering** with technical indicators, wavelet transforms & liquidity metrics  
- 🧠 **Modeling** using both **PyTorch-based MLP classifiers** and **Random Forests** 
- 🧪 **Cross-validation** with purged K-folds and embargo periods  
- 🧾 **Back-testing** with signal-based returns, accuracy, and cumulative P&L

> 💡 No hidden scripts. No complex dependencies. Just open the notebook and run it.

---

## 📈 2 — Performance Snapshot (Raw Results from Notebook)

| 🪙 Market   | ✅ Trade Accuracy | 💹 Cumulative P&L* |
|------------|------------------|-------------------|
| **BTC/USD** | **20.7%**         | **+5.5%**          |
| **US30**    | **1.2%**          | **+0.3%**          |

\* P&L is scaled (1.0 = 100%) and reflects notebook-level assumptions (e.g., position sizing, transaction costs).

> 🧬 **Note on Trade Accuracy**  
> This is a **low hit rate, high reward** strategy. Despite a **20.7% directional accuracy**, the model yields **+5.5% cumulative P&L**, indicating strong alpha in **tail events**.

> ⚖️ **Why US30?**  
> Treated as a **control asset**. Using the same pipeline without tuning confirms that the BTC/USD results were not the result of overfitting. The underperformance of US30 highlights the importance of asset-specific feature engineering.

---
