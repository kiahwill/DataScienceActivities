# Taiwan Bankruptcy Financial Ratio Analysis

A Python-based exploratory data analysis (EDA) project comparing bankrupt and non-bankrupt companies using key financial ratios from the Taiwan Bankruptcy Prediction dataset. This project focuses on identifying financial patterns associated with corporate failure through descriptive statistics and visual analysis.

## Overview

The objective of this project is to analyze and compare financial health indicators between bankrupt and healthy firms. It provides insights that can support bankruptcy prediction, financial risk assessment, and feature selection for machine learning models.

## Dataset

- **Dataset**: Taiwan Bankruptcy Prediction
- **Target Column**: `Bankrupt?`
  - `0` → Non-Bankrupt
  - `1` → Bankrupt
- **Features**: Financial ratios derived from corporate financial statements

> **Note**: Financial ratios may contain extreme values and skewed distributions.

## Financial Ratios Analyzed

The following key financial ratios are examined:

- **ROA (C) before interest and depreciation** - Profitability measure
- **Net Income to Total Assets** - Overall profitability indicator
- **Liability to Equity** - Leverage ratio
- **Interest Coverage Ratio** (Interest expense to EBIT) - Debt-servicing ability

These ratios capture profitability, leverage, and debt-servicing ability, which are critical indicators of financial distress.

## Tech Stack

- Python 3
- pandas
- numpy
- matplotlib

**Recommended environment**: Google Colab or Jupyter Notebook

## Analysis Steps

1. Load and clean the dataset
2. Inspect data structure and missing values
3. Split data into bankrupt and non-bankrupt groups
4. Compute group-wise averages and percentage differences
5. Visualize distributions using boxplots
6. Compare mean values using bar charts
7. Generate summary statistics

## Visualizations

The analysis includes:

- Boxplots comparing financial ratio distributions
- Bar charts showing average ratio differences
- Tabular summaries of means and standard deviations

## Key Findings

- Bankrupt firms show **significantly lower profitability**
- Leverage ratios are **notably higher** among bankrupt companies
- Interest coverage is **substantially weaker** for bankrupt firms
- Overlapping distributions indicate the need for multivariate or machine-learning-based models

## How to Run

### Installation

```bash
pip install pandas numpy matplotlib
```

### Execution

1. Clone or download this repository
2. Update the dataset path if needed:

```python
df = pd.read_csv("path/to/taiwan_bankruptcy.csv")
```

3. Run all cells to reproduce the analysis and visualizations

## Use Cases

- Academic research and thesis work
- Financial risk analysis
- Feature exploration for machine learning models
- Educational demonstrations

## Future Improvements

- [ ] Statistical significance testing (t-test, Mann–Whitney U)
- [ ] Effect size calculation (Cohen's d)
- [ ] Outlier treatment (winsorization)
- [ ] Machine learning models for bankruptcy prediction
- [ ] Comparison with classical models (e.g., Altman Z-Score)

## License

This project is for educational and research purposes.

---

**Contributions and feedback are welcome!**
