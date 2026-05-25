# Task 1 - Selection and Research

## Selected regulated entity

The regulated entity selected for this assignment is **HSBC Holdings plc**, with specific operational relevance to **HSBC Bank USA** and **The Hongkong and Shanghai Banking Corporation Limited**. HSBC is suitable because it is a globally active banking group with material operations in both the United States and Hong Kong. That makes it a credible test case for a jurisdiction-aware RegTech product rather than a single-country compliance checklist.

HSBC's public reporting identifies Hong Kong as one of its core markets, while HSBC USA operates through a separately reported US banking presence. This creates a realistic setting for a compliance tool that must support one group-level risk function while respecting different local legal and supervisory expectations.

## Selected domain

The domain selected is **AI-assisted credit scoring and credit decision governance**.

This domain is appropriate for the assignment because the same technical activity - using a model to estimate credit risk and support loan approvals - creates different compliance questions in different jurisdictions.

In the United States, the tool must be especially attentive to fair lending obligations, adverse-action notice requirements, and the risk that a complex algorithm cannot produce sufficiently specific reasons for denial. In Hong Kong, the tool must be attentive to the HKMA's high-level principles on artificial intelligence, proportional governance, human oversight, accountability, consumer credit data handling, and privacy-oriented AI governance.

## Why US vs Hong Kong creates real regulatory divergence

The key design tension is that the United States places a relatively explicit legal burden on the lender to explain adverse credit decisions under ECOA and Regulation B, including where complex algorithms or AI models are used. The CFPB has emphasized that complexity does not excuse a creditor from giving specific principal reasons for adverse action.

Hong Kong's framework is less centered on a US-style adverse-action notice rule. The more relevant compliance logic is supervisory and governance-oriented: authorized institutions are expected to adopt AI in a risk-based, proportionate manner; maintain board and senior management accountability; validate models; preserve human oversight; monitor outcomes; and handle personal and consumer credit data properly.

Therefore, a jurisdiction-aware tool should not merely display two labels, "US" and "HK." It should change the compliance output:

- In **US mode**, the tool generates adverse-action reason codes, tests approval-rate disparity, and flags potential fair lending concerns.
- In **Hong Kong mode**, the tool emphasizes AI governance controls, privacy and consumer credit data considerations, human review triggers, proportionality, and ongoing monitoring.

## Selected tool concept

The proposed tool is **HSBC CreditLens**, a jurisdiction-aware compliance dashboard for AI-assisted credit scoring. It takes credit model outputs, applicant attributes, model drivers, and fairness metrics as inputs. It then applies a jurisdiction configuration layer to decide which regulatory tests, thresholds, explanations, and governance evidence are required.

## Core research references

- HSBC Holdings plc, Annual Report and Accounts 2025: https://www.hsbc.com/investors/results-and-announcements/annual-report
- HSBC USA investor relations and corporate information: https://www.about.us.hsbc.com/investor-relations/hsbc-usa
- CFPB Circular 2022-03 on adverse-action notices and complex algorithms: https://www.consumerfinance.gov/compliance/circulars/circular-2022-03-adverse-action-notification-requirements-in-connection-with-credit-decisions-based-on-complex-algorithms/
- CFPB news release on AI credit denials: https://www.consumerfinance.gov/about-us/newsroom/cfpb-issues-guidance-on-credit-denials-by-lenders-using-artificial-intelligence/
- HKMA High-level Principles on Artificial Intelligence: https://www.hkma.gov.hk/media/eng/doc/key-information/guidelines-and-circular/2019/20191101e1.pdf
- HKMA personal credit consumer information: https://www.hkma.gov.hk/eng/smart-consumers/personal-credit
- PCPD Guidance on the Ethical Development and Use of Artificial Intelligence: https://www.pcpd.org.hk/english/resources_centre/publications/files/guidance_ethical_e.pdf
