# Credit-Risk Delinquency Modelling in Microfinance

Python implementation accompanying the working paper:

**“Quantifying socio-temporal effects of loan delinquency drivers in microfinance”**
arXiv: https://arxiv.org/abs/2410.13100

This repository provides a reproducible implementation of statistical and machine-learning workflows for modelling borrower repayment behaviour, delinquency transitions, latent heterogeneity, and next-state prediction in microfinance loan portfolios (but can easily be extended to any lending portfolio).

The code is based on synthetic data generated within the notebook to protect the confidentiality of the original borrower-level data while preserving the structure needed to reproduce the modelling and numerical experiments.

---

## Project overview

The project studies how borrower characteristics, repayment history, loan behaviour, and socio-temporal factors relate to loan delinquency dynamics. It combines interpretable statistical modelling with predictive machine-learning methods to support credit-risk analysis and data-driven decision-making in microfinance operations.

The notebook covers:

* simulation of synthetic borrower-level longitudinal loan data;
* construction of borrower repayment states and transition outcomes;
* discrete-time credit-risk modelling using logit-link formulations;
* frailty and latent-heterogeneity extensions;
* numerical integration using Gauss-Hermite quadrature;
* model estimation, validation, and comparison;
* machine-learning benchmarks for transition prediction;
* class-imbalance evaluation;
* implementation of an optimised MCC-based multistate classification strategy.

---

## Why this matters

Credit-risk analytics in microfinance often involves noisy borrower histories, repeated loans, irregular repayment behaviour, class imbalance, and heterogeneous borrower risk. This project illustrates how statistical modelling and machine learning can be combined to:

* understand repayment and delinquency transitions;
* quantify borrower-level heterogeneity;
* compare interpretable statistical models with predictive ML methods;
* evaluate model robustness under class imbalance;
* support portfolio monitoring and operational decision-making.

Although the code is research-oriented, the workflow is relevant to practical credit-risk analytics tasks such as arrears modelling, borrower segmentation, transition prediction, portfolio monitoring, and model validation.

---

## Repository contents

```text
.
├── Chapter_2_codes_final.ipynb   # Main notebook containing simulation, modelling, estimation and experiments
├── README.md                     # Project documentation
└── Readme.txt                    # Legacy short description
```

Recommended future structure:

```text
.
├── notebooks/
│   └── credit_risk_delinquency_modelling.ipynb
├── README.md
├── requirements.txt
└── LICENSE
```

---

## Methods implemented

The notebook includes implementations of:

* discrete-time logistic credit-risk models;
* random-intercept frailty models;
* time-dependent frailty extensions;
* marginal likelihood estimation using Gauss-Hermite quadrature;
* logistic regression benchmarks;
* tree-based predictive models including random forests;
* multistate transition prediction;
* Matthews Correlation Coefficient based threshold optimisation;
* validation workflows using holdout/temporal separation and robustness checks.

---

## Synthetic data and confidentiality

The original data used in the research is confidential and cannot be shared publicly.

To make the implementation reproducible, the notebook generates synthetic datasets directly in Python. These synthetic datasets are designed to mimic the structure required for the modelling workflow, including borrower-level histories, loan-level records, repayment states, transition outcomes, and covariates.

The synthetic data should not be interpreted as real borrower information and should not be used for operational credit decisions.

---

## How to run

1. Clone the repository:

```bash
git clone https://github.com/cedricak/Modeling-credit-risk-delinquency-in-MFI.git
cd Modeling-credit-risk-delinquency-in-MFI
```

2. Create and activate a Python environment:

```bash
python -m venv .venv
source .venv/bin/activate      # macOS/Linux
# .venv\Scripts\activate       # Windows
```

3. Install the main dependencies:

```bash
pip install numpy pandas scipy scikit-learn statsmodels matplotlib plotly joblib
```

Depending on the exact notebook section being run, additional packages may be required.

4. Open the notebook:

```bash
jupyter notebook Chapter_2_codes_final.ipynb
```

---

## Main outputs

The notebook produces:

* simulated borrower-level and loan-level datasets;
* fitted statistical credit-risk models;
* marginal likelihood calculations for frailty models;
* predictive model comparisons;
* transition prediction outputs;
* classification performance metrics;
* MCC-based threshold optimisation results;
* numerical experiments supporting the paper.

---

## Paper reference

Cedric H. A. Koffi, Viani Biatat Djeundje, and Olivier Menoukeu Pamen.
**Quantifying socio-temporal effects of loan delinquency drivers in microfinance.**
arXiv:2410.13100, Quantitative Finance > Risk Management.
https://arxiv.org/abs/2410.13100

---

## Notes

This repository is intended for reproducibility, research transparency, and demonstration of applied credit-risk modelling workflows. It is not a production credit-decisioning system.

The modelling ideas and implementation are most relevant to:

* credit-risk modelling;
* borrower behaviour analytics;
* delinquency and arrears modelling;
* multistate transition prediction;
* portfolio risk monitoring;
* model validation under class imbalance;
* responsible lending analytics.

---

## Author

Cedric H. A. Koffi
PhD Mathematics, University of Liverpool
GitHub: https://github.com/cedricak
LinkedIn: https://www.linkedin.com/in/abekah-h-cedric-koffi-604409b9
