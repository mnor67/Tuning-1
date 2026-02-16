This project demonstrates threshold tuning and backtesting for an Anti-Money Laundering (AML) Transaction Monitoring system using a synthetic transaction dataset.
The objective is to show how different transaction amount thresholds impact:
Alert volume
Detection of laundering activity
Operational efficiency (false positives vs true positives)
This mirrors real-world AML tuning practices used by banks and financial institutions.

Source: Kaggle – Synthetic Transaction Monitoring Dataset (AML)
Records: ~9.5 million transactions
Key Columns:
Amount – Transaction value
Is_laundering – Ground truth label
1 = confirmed laundering
0 = normal transaction
Payment_type, Sender_bank_location, Receiver_bank_location, etc.
⚠️ Note: In real AML operations, laundering labels are not known upfront.
They are included here strictly for backtesting and learning purposes.
Methodology
1️⃣ Percentile-Based Threshold Selection
Thresholds were derived using transaction amount percentiles:
90th percentile
95th percentile
99th percentile
This approach reflects common AML practices where rules are tuned based on data distribution.
