# Asset Growth Anomaly Replication & Extension

This repository replicates and extends the asset growth anomaly first documented by **Cooper, Gulen, and Schill (2008)** in *“Asset Growth and the Cross-Section of Stock Returns”*.  
We examine whether firms with high asset growth earn lower subsequent stock returns than firms with low asset growth, and we test a modification of the original strategy design.

## 📌 Project Overview
- **Replication period**: 1962–2024 (out-of-sample evidence beyond the original 1968–2003 study).
- **Core finding**: Firms with low asset growth (Decile 1) significantly outperform high asset growth firms (Decile 10).
- **Traditional strategy**: Long Decile 1 / Short Decile 10 → delivers ~1.06% monthly alpha, 15% annualized.
- **Modified strategy**: Long Decile 1 / Short Decile 5 → delivers higher alpha (~1.79% monthly), lower drawdowns, and better Sharpe ratio.

## 📂 Repository Structure
```
.
├── notebooks/
│   └── Asset_growth_Replication_Final.ipynb   # main replication analysis
├── paper/
│   └── QAMFinalWriteUp_C2G10.pdf              # full academic-style writeup
├── data/                                      # (gitignored) raw/processed data
├── requirements.txt                           # Python dependencies
├── README.md                                  # this file
└── .gitignore
```

## ⚙️ Methodology
- **Data sources**: Compustat Fundamentals Annual, CRSP Monthly, CRSP–Compustat Link Table.
- **Portfolio construction**:
  - Rank firms into deciles each June by asset growth.
  - Form value-weighted portfolios (held July–June).
  - Evaluate long–short strategies with and without modified shorting rule.
- **Performance evaluation**: Summary statistics, Fama–French 3-factor regressions, Fama–MacBeth cross-sectional regressions.

## 🚀 Results Summary
- Asset growth anomaly persists through 2024, even post-publication.
- Traditional strategy remains profitable, but:
  - **Modified Long(1)/Short(5)** delivers superior risk-adjusted returns, with ~78% improvement in Sharpe ratio.
- Robust across bull/bear markets and after transaction cost adjustments.

## 📦 Installation
```bash
git clone https://github.com/siddy1999/asset-growth-anomaly-replication.git
cd asset-growth-anomaly-replication
pip install -r requirements.txt
```

## ▶️ Usage
Run the notebook:
```bash
jupyter lab notebooks/Asset_growth_Replication_Final.ipynb
```

## 📑 Reference
- Cooper, Michael J., Huseyin Gulen, and Michael J. Schill. “Asset Growth and the Cross-Section of Stock Returns.” *Journal of Finance* 63, no. 4 (2008): 1609–1651.

---

### Maintainers
- Siddhant Kumar (siddy1999)

### License
MIT
