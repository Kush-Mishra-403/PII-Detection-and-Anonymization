# PII Detection and Anonymization in Financial Documents
A scalable framework integrating hybrid rule-based NLP and Machine Learning approaches for detecting and anonymizing Personally Identifiable Information (PII) in financial documents. Achieves high precision, recall, and accuracy while preserving document readability.

## Overview
This project proposes a hybrid method combining pattern-based detection with a custom-trained spaCy NER model for robust PII detection and anonymization. It handles sensitive fields like names, phone numbers, emails, addresses, SSNs, credit card numbers, URLs, and company names across structured and unstructured financial texts.

## Features
---

### PII Types Detected:
1. Person Names
2. Email Addresses
3. Phone Numbers (various international formats)
4. Home and Office Addresses (single-line and multi-line formats)
5. Social Security Numbers (SSNs) (different valid structures)
6. Credit Card Numbers (Visa, MasterCard, JCB formats)
7. Company/Organization Names
8. Website URLs

---

---

### Data Handling:
The model has been Trained and Evaluated on **both Synthetic and Real-World Financial Documents** to ensure practical robustness.

| Data Type | Details |
|:----------|:--------|
| **Synthetic Training and Testing Data** | Generated using finance-related templates with embedded fake PII using Faker library. Types include: <br> - Audit Reports <br> - Compliance Reports <br> - Transaction Reports <br> - Tax Reports <br> - Invoices <br> - Customer Conversations and Feedbacks <br> - Bank Reports <br> - Bank Statements |
| **Real-World Testing Data** | Real financial documents containing naturally occurring PII. Documents include: <br> - Bank of America Audit Report <br> - Amazon Vendor Invoice <br> - CPB Software Vendor Invoice |

🔗 ** Synthetic Dataset Link:** [Mendeley Data Repository](https://doi.org/10.17632/tzrjx692jy)

---

---

### Model:

- **Architecture:** A lightweight, custom-trained spaCy NER model optimized for the financial domain.
- **Training Approach:** 
  - Combined rule-based preprocessing and automatic span annotation for efficient data labeling.
  - Iterative model training with controlled dropout and mini-batch strategy for better generalization.
- **Anonymization Placeholders Used:**
  - `[NAME REDACTED]`
  - `[EMAIL REDACTED]`
  - `[PHONE NUMBER REDACTED]`
  - `[ADDRESS REDACTED]`
  - `[SSN REDACTED]`
  - `[CREDIT CARD REDACTED]`
  - `[COMPANY NAME REDACTED]`
  - `[URL REDACTED]`
  
Detected PII entities are replaced with these placeholders to anonymize sensitive information while preserving document readability.

---

---

## 📈 Evaluation Metrics

The model has been rigorously evaluated on both synthetic and real-world data:

| Dataset                         | Precision | Recall | F1-Score | Accuracy |
|:---------------------------------|:---------:|:------:|:--------:|:--------:|
| Synthetic Financial Documents   | 94.7%     | 89.4%  | 91.1%    | 89.4%    |
| Real-World Financial Documents   | ~93%      |  -     |   -      | ~93%     |

Metrics have been computed based on entity-level detection, ensuring high reliability even in complex financial document layouts.

---

---

## License and Usage Terms

### 1. The source code is provided under a **Custom Academic License**.

### 2. Permitted Use:
Strictly for research and educational purposes with **adequate permission** from the owner.

### 3. Prohibited Use:
Commercial use, redistribution, or modification without **prior written consent** is strictly prohibited.

### 4. Attribution Required:
If you publish work or create derivatives based on this repository, you must **appropriately cite** this GitHub repository and the associated research study.

### 5. Strict Copyright Enforcement:
Any use of the code, datasets, or other resources from this repository without **adequate citation** and **prior permission** from the owner will be treated as a **copyright violation**.
Such unauthorized use will result in **immediate copyright strikes**, **takedown notices**, and **legal action** if necessary.

---


