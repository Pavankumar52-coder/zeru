# zeru

# Wallet Credit Scoring System

## Overview:

This project analyzes blockchain wallet transaction  behavior of DeFi and computes a credit score for each wallet based on its net transactional balance. The goal is to rank wallets from low to high creditworthiness using a reproducible and interpretable scoring method.

---

## Methodology:

- **Net Balance Scoring**: We compute the net sum of all transactions per wallet.
- **Score Transformation**:
  - Applied `log10` to reduce skew caused by huge values.
  - Normalized log values to a 0–1000 scale.

---

## Architecture & Flow:

1. **Data Ingestion**: Load JSON transaction data from zip.
2. **Flattening**: Normalize nested structure into a DataFrame.
3. **Processing**:
   - Convert string amounts to floats.
   - Aggregate transactions per wallet.
   - Log transform & normalize net balances.
4. **Scoring**:
   - Credit score scaled between 0–1000.

---

## Requirements:

- Python 3.x
- Pandas
- Numpy
- Matplotlib (for analysis)
- ast
---

## How to Run:

You can use `credit_scoring.ipynb` directly in Google Colab or Jupyter Notebook.

Upload `user-wallet-transactions.json.zip`, run the notebook, and scores will be computed and analyzed.
