## Distribution Summary — Key Observations

### BALANCE
> **Meaning:** The amount of money a customer currently owes on their credit card (unpaid balance).
- Strongly **right-skewed** — the majority of customers maintain a **low balance** (close to zero), while a small subset carries very high unpaid balances.
- Presence of heavy outliers at the upper end suggests a group of **high-debt revolvers** who rely on credit heavily.

### BALANCE_FREQUENCY
> **Meaning:** How often the balance is updated — a score from 0 to 1 (1 = updated every month).
- Shows a clear **bimodal pattern** — most values cluster near **0 or 1**, indicating customers either update their balance almost every month (frequent users) or rarely at all (inactive users).
- Very few customers fall in the middle range, confirming a distinct behavioral divide.

### PURCHASES
> **Meaning:** Total amount spent on purchases made using the credit card.
- Strongly **right-skewed** with a large spike at **zero** — a significant portion of customers make **no purchases** at all.
- A long right tail shows a small group of high-spending customers, likely prime candidates for rewards or premium segments.

### ONEOFF_PURCHASES
> **Meaning:** Total amount spent on single large purchases (one-time transactions, not split into installments).
- Extremely **right-skewed** with the majority at **zero** — most customers do not make large one-off (single) purchases.
- The heavy tail represents occasional big spenders, possibly buying high-value items infrequently.

### INSTALLMENTS_PURCHASES
> **Meaning:** Total amount spent on purchases paid in installments (EMI / split payments).
- **Right-skewed** with a large zero-concentration — many customers avoid installment buying.
- A moderate tail suggests a segment that **prefers EMI-style purchases**, likely for larger goods.

### CASH_ADVANCE
> **Meaning:** Amount of cash withdrawn in advance using the credit card (like a short-term loan).
- Severely **right-skewed** with most customers at **zero** — the majority never take cash advances.
- Extreme outliers in the upper tail represent **high-risk customers** who routinely use the credit card as a cash source, incurring high fees.

### PURCHASES_FREQUENCY
> **Meaning:** How regularly purchases are made — a score from 0 to 1 (1 = purchases made every month).
- **Bimodal** — strong peaks at both **0** (never purchase) and **1** (purchase every month), with relatively few customers in between.
- This cleanly separates **active purchasers** from **inactive cardholders**.

### ONEOFF_PURCHASES_FREQUENCY
> **Meaning:** How often one-off (single large) purchases are made — a score from 0 to 1.
- **Right-skewed with a dominant zero peak** — most customers never make one-off purchases in a given month.
- A secondary bump near 1.0 indicates a small group of consistent single-purchase users.

### PURCHASES_INSTALLMENTS_FREQUENCY
> **Meaning:** How often installment purchases are made — a score from 0 to 1.
- **Bimodal** — customers are split between those who **never** use installments and those who use them **regularly every month**.
- Indicates a clear preference-based segmentation opportunity.

### CASH_ADVANCE_FREQUENCY
> **Meaning:** How often cash advances are taken — a score from 0 to 1.
- Heavily **right-skewed** — most customers have a frequency of **zero**, meaning cash advances are rare behavior.
- Small but consistent non-zero values highlight a niche **cash-dependent segment**.

### CASH_ADVANCE_TRX
> **Meaning:** Number of individual cash advance transactions made.
- **Right-skewed count variable** — most customers have **zero transactions**, confirming cash advance is not mainstream behavior.
- Outliers with high transaction counts are likely **high-risk or financially stressed** customers.

### PURCHASES_TRX
> **Meaning:** Number of individual purchase transactions made.
- **Right-skewed** but with a smoother distribution than cash advance — some customers are moderately active.
- A long tail of high transaction counts suggests a **frequent buyer segment** that could benefit from loyalty programs.

### CREDIT_LIMIT
> **Meaning:** The maximum credit amount the bank has approved for the customer.
- **Right-skewed** with visible **spikes at round numbers** (e.g., 1000, 2000, 5000) due to discretized limit assignments by banks.
- Most customers have moderate limits; very few have extremely high limits.

### PAYMENTS
> **Meaning:** Total amount paid by the customer to the bank (repayments made).
- Strongly **right-skewed** — most payments are small, but outliers show customers making very large repayments, possibly those with high balances.
- Distribution mirrors BALANCE, consistent with customers paying proportionally to what they owe.

### MINIMUM_PAYMENTS
> **Meaning:** The minimum required payment amount due each month (set by the bank).
- Strongly **right-skewed** — most customers pay small minimum amounts, but a tail of high values reflects customers with very large outstanding debts.
- Had **313 missing values**, imputed with the column mean — meaning the distribution is slightly compressed around the mean after imputation.

### PRC_FULL_PAYMENT
> **Meaning:** Percentage of months where the customer paid the full outstanding balance (0 = never, 1 = always).
- Heavily **right-skewed with a dominant zero peak** — the vast majority of customers **never pay their full balance**, carrying debt forward each month.
- A small cluster near **1.0** represents disciplined **transactor customers** who consistently pay off their balance in full.

### TENURE
> **Meaning:** Number of months the customer has held the credit card account.
- Strongly **left-skewed (negatively skewed)** — the overwhelming majority of customers have a tenure of **12 months** (the maximum in the dataset).
- Very few customers have short tenures, indicating this dataset largely captures **established, long-term cardholders**.