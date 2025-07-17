# DeFI-Credit-Scoring-model
This model assigns a credit score (0–1000) to each wallet based on transaction behavior.
---

### 📄 Step 8: **analysis.md**

```markdown
# Score Distribution & Behavioral Insights

## Distribution:
- Most wallets scored between 600–800.
- Risky wallets (0–200) had:
  - High liquidation rates
  - Low repay ratios
- Trusted wallets (800–1000) showed:
  - High deposits
  - Strong repay/borrow behavior

## Notable Observations:
- Liquidated wallets frequently failed to repay.
- Some bots show rapid transactions with zero repays.

## Improvements:
- Include time-series patterns for behavior trends.
- Leverage on-chain identity verification for more features.
