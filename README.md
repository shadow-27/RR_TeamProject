# 🟦 RR_TeamProject

![Python](https://img.shields.io/badge/Python-3.10%2B-blue)
![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20Linux%20%7C%20macOS-green)
![Status](https://img.shields.io/badge/Status-Active-brightgreen)

---

## 🚀 Project Setup & Reproducibility

### 1️⃣ Clone the Repository
```bash
git clone <repo-url>
cd RR_TeamProject
```

### 2️⃣ Set Up a Virtual Environment
**Windows (PowerShell):**
```bash
python -m venv venv
.\venv\Scripts\Activate
```
**macOS/Linux:**
```bash
python3 -m venv venv
source venv/bin/activate
```

### 3️⃣ Install Required Libraries
```bash
pip install -r requirements.txt
```
If `requirements.txt` does not exist:
```bash
pip install numpy pandas matplotlib yfinance scipy IPython quarto
```

### 4️⃣ Run the Notebook
Open `Var_ES.ipynb` in Jupyter Notebook or VS Code and run all cells.

---

## 📦 Required Libraries

The following libraries are required and should be installed in your environment:

- `numpy`
- `pandas`
- `matplotlib`
- `yfinance`
- `scipy`
- `IPython` (for `display` and `Markdown` in Jupyter)
- `quarto` (for rendering the Quarto document)

## 📊 Data
- The notebook fetches data automatically from Yahoo Finance. No manual data download is required.

## 📁 Project Structure
```
RR_TeamProject/
├── Var_ES.ipynb           # Main analysis notebook
├── requirements.txt       # List of dependencies
└── README.md              # Project documentation
├── Var_ES.qmd             # Quarto documentation
├── Var_ES_files/          # Directory for any additional data files (if needed)
└── Var_ES.html            # HTML output of the Quarto document
```

---

## 📚 Project Overview

This project estimates and compares **Value at Risk (VaR)** and **Expected Shortfall (ES)** for a diversified financial portfolio using three risk assessment methodologies:

- 🟠 **Historical Simulation**: Uses actual historical returns to estimate risk.
- 🟢 **Parametric Method (Variance-Covariance)**: Assumes normality, uses mean & std deviation.
- 🟣 **Monte Carlo Simulation**: Simulates returns using estimated parameters.

### 🎯 Objective
Provide a robust, comparative analysis of portfolio risk using different VaR and ES estimation techniques, highlighting the strengths and limitations of each method for better risk management.

### 🔍 What is Compared?
- VaR and ES values for the same portfolio and data period, using all three methods.
- The impact of assumptions (e.g., normality) and methodology (historical vs. simulated) on risk estimates.
- Results are summarized in a table and visualized for clear comparison.

### 🏁 Results & Conclusion
- **Results:** All three methods yield similar VaR values (around -1.1% at 95% confidence), but ES values show that extreme losses can be higher, especially in historical data.
- **Conclusion:** The close alignment of VaR and ES across methods suggests a stable risk profile. ES is a more conservative and informative risk measure, especially for tail risk. Using multiple methods provides a more comprehensive view of risk, and regular monitoring is recommended.

**Data Source:**  
Stock market data for Apple (AAPL), Microsoft (MSFT), and Google (GOOG) from Yahoo Finance.

**Notebook:**  
All analysis and code are in `Var_ES.ipynb`.

---

## 📝 Notes
- Ensure you have Python 3.10 or higher installed.
- For best reproducibility, use the provided virtual environment and install exact library versions if a `requirements.txt` is available.
- If you encounter issues with data download, check your internet connection and ensure the `yfinance` library is installed.

## 📬 Contact
For questions or contributions, please open an issue or contact the project maintainer.
