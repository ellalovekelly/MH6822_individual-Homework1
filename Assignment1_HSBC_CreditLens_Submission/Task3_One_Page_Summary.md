# Task 3 - One Page Summary

## Plain-language summary

This project designs and partially implements **HSBC CreditLens**, a jurisdiction-aware compliance tool for AI-assisted credit scoring at HSBC. The tool is built around a simple idea: the same credit model output can create different compliance obligations depending on where it is used.

The prototype uses synthetic credit applicant data for the United States and Hong Kong. A logistic regression model estimates each applicant's probability of default. The notebook then converts the model output into approval decisions, fairness metrics, sample adverse-action explanations, and governance alerts.

## Why this is jurisdiction-aware

In **US mode**, the tool focuses on fair lending and adverse-action explainability. It checks whether approval rates differ between groups, calculates the adverse impact ratio, and generates specific model-driven reasons for denial. This reflects the US emphasis under ECOA and Regulation B that creditors must provide specific principal reasons for adverse actions, even when complex algorithms are used.

In **Hong Kong mode**, the tool focuses on AI governance and consumer credit data controls. It checks fairness outcomes but frames the output as governance evidence: model validation, proportional human oversight, privacy impact assessment, and ongoing monitoring. This reflects the HKMA's high-level principles on AI and Hong Kong's consumer credit data environment.

## Quantitative component

The prototype monitors:

- approval rate by protected group
- adverse impact ratio
- false positive rate gap
- equal opportunity difference
- model drift sensitivity

In the generated run, the model AUC is approximately **0.671**. The US adverse impact ratio is **0.57**, while the Hong Kong adverse impact ratio is **0.54**. These values are not legal conclusions. They are monitoring signals.

## What the tool solves

A memo or spreadsheet can describe regulatory differences, but it cannot reliably apply them to changing model outputs. HSBC CreditLens makes the regulatory divergence operational. It stores jurisdiction-specific thresholds and output requirements in a configuration layer, applies those rules to model results, and produces evidence that senior management can review.

## What the tool does not do

The tool does not approve or reject real customers. It does not provide legal advice. It does not prove that HSBC is compliant. It does not eliminate the need for model validation, legal review, or human judgement. These boundaries are intentional because AI compliance involves legal, ethical, and business judgement that should remain accountable to people.
