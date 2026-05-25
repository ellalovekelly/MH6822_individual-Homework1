# Task 3 - Model Card and Governance Stub

## Model name

HSBC CreditLens synthetic credit scoring demonstrator

## Intended use

The model estimates 12-month probability of default for synthetic consumer credit applicants. It is used only to demonstrate a jurisdiction-aware compliance monitoring tool. It is not a production HSBC model and must not be used for real credit decisions.

## Data

The dataset contains 6,000 synthetic credit applicants across US and Hong Kong modes. Features include income, debt-to-income ratio, credit utilization, credit history length, recent delinquencies, recent inquiries, age, employment stability, and existing customer status. A synthetic protected-group variable is included for fairness testing.

## Model type

Logistic regression with standardized numeric features. Logistic regression was selected because the assignment focuses on jurisdiction-aware compliance logic rather than predictive performance. A transparent baseline model is easier to explain to senior management and easier to connect to adverse-action reasons.

## Performance

In the generated run, the model AUC is approximately **0.671** and the overall approval rate is approximately **26.4%**.

## Fairness metrics

The tool monitors approval-rate disparity, adverse impact ratio, false-positive rate gap, and equal opportunity difference by protected group.

- US adverse impact ratio: **0.57**
- Hong Kong adverse impact ratio: **0.54**

These metrics are not legal conclusions. They are screening indicators that determine whether the model requires review.

## Jurisdiction configuration

In US mode, the tool emphasizes ECOA / Regulation B explainability and fair lending screening. It produces sample adverse-action reasons for denied applicants and flags potential disparate impact where the adverse impact ratio falls below the chosen threshold.

In Hong Kong mode, the tool emphasizes HKMA AI governance principles, proportionality, human oversight, privacy impact assessment, consumer credit data governance, and ongoing monitoring.

## Known limitations

- The data is synthetic and does not represent HSBC customers.
- The protected-group variable is simulated.
- The model is intentionally simple.
- The fairness thresholds are demonstrative and would require legal, compliance, and risk committee approval before production use.
- The tool does not determine whether a credit decision is lawful.
- The tool does not replace human judgement, legal advice, model validation, or regulator engagement.

## Monitoring plan

- Monthly fairness metric recalculation by jurisdiction.
- Quarterly model performance review.
- Drift alert if approval rates or predicted probability distributions shift materially.
- Human review for near-threshold denials and cases with unclear adverse-action reasons.
- Rule-version audit trail whenever jurisdiction parameters are updated.
