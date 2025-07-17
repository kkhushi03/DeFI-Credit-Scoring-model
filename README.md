# DeFI-Credit-Scoring-model

This project analyses on-chain transaction-level data from wallets interacting with the Aave V2 protocol on the Polygon network. It assigns a **credit score (0–1000)** to each wallet based on historical activity, using features like deposit frequency, borrow behaviour, and asset usage patterns.

## 🔍 Project Overview

- **Goal**: Build a data-driven credit scoring system for DeFi wallets using real Aave V2 activity logs.
- **Data Source**: MongoDB dump containing transactional data, including actions like deposits, borrows, repayments, and liquidations.
- **Protocol**: Aave V2 on Polygon
- **Scoring Range**: 0 (high risk) to 1000 (low risk)

---

## 📁 Dataset Structure

The transaction dataset includes the following columns:

| Column Name    | Description |
|----------------|-------------|
| `_id`          | MongoDB Object ID |
| `userWallet`   | Wallet address interacting with Aave |
| `network`      | Blockchain network (e.g., polygon) |
| `protocol`     | DeFi protocol name (aave_v2) |
| `txHash`       | Transaction hash |
| `logId`        | Log identifier |
| `timestamp`    | Unix timestamp of the transaction |
| `blockNumber`  | Blockchain block number |
| `action`       | Type of action (`deposit`, `borrow`, `repay`, etc..) |
| `actionData`   | Nested JSON object with details like amount, token, and type |
| `createdAt`, `updatedAt` | Timestamps for document creation and update |

---

## ⚙️ Tech Stack

- **Language**: Python 3
- **Libraries**: 
  - `pandas`, `matplotlib`, `seaborn`
  - `datetime`, `json`
- **Notebook**: Jupyter Notebook (`aave_credit_scoring.ipynb`)

---

## 🧮 Feature Engineering

Wallet-level features include:
- Total and average deposit amount
- Borrow-to-deposit ratio
- Frequency of actions (deposits, borrows, repayments)
- Time since last activity
- Presence of liquidation events

---

## 📊 Visualization

Graphs include:
- Distribution of credit scores
- Correlation between features
- Wallet activity timeline

Use `%matplotlib inline` in the notebook or `plt.show()` in Python scripts to visualize.

---

## 📌 How to Run

### 🔧 Setup
```bash
git clone https://github.com/kkhushi03/defi-credit-scoring-model.git
cd defi-Credit-scoring-model
pip install -r requirements.txt
