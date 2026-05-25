# Task 2 - Values Audit

## 1. Mission statement and company profile

The hypothetical company is **RegLens Analytics**, an early-stage RegTech company building jurisdiction-aware model governance tools for banks. Its mission is:

> To help financial institutions use AI in credit decisions without hiding behind complexity, by turning model outputs into explainable, jurisdiction-specific governance evidence.

RegLens Analytics has 18 employees: data scientists, regulatory analysts, software engineers, and former second-line risk professionals. The company is at seed-to-Series-A stage. Its first target customers are internationally active banks with consumer credit products in more than one jurisdiction. The company is good at translating legal and supervisory expectations into machine-readable control logic, dashboards, and documentation.

The commercial aspiration is to reach USD 5-8 million in annual recurring revenue within three years by selling to compliance, model risk, and retail credit risk teams. The product is not intended to replace legal advice or credit officers. It is intended to reduce the gap between model development, compliance monitoring, and senior management accountability.

## 2. Whose perspective does the tool serve?

The primary paying client is the bank's Chief Compliance Officer or Chief Risk Officer. However, the tool is designed to serve three perspectives at once:

- **The bank**, which needs defensible evidence that its AI credit model is being monitored across jurisdictions.
- **The regulator**, which needs the bank to demonstrate that AI adoption has not weakened fairness, accountability, or explainability.
- **The consumer**, who bears the direct cost of opaque or unfair credit decisions.

There is a real tension between these perspectives. The bank may prefer a tool that minimizes regulatory findings and produces clean documentation. The consumer needs meaningful explanations and fair treatment, even where this may expose uncomfortable model weaknesses. The regulator needs the bank to demonstrate actual control, not just produce a binder of policies.

RegLens chooses to serve the paying bank, but only by making consumer and regulatory harms visible. This is partly commercial: banks have the ability to pay. It is also competency-driven: the company can build better monitoring tools than it can provide direct consumer advocacy. The ethical risk is that the product becomes a compliance shield. To reduce that risk, the tool deliberately includes failure-mode flags and "not fit for automated approval" outcomes.

## 3. Genuine risk or documenting compliance?

The tool is intended to measure genuine risk, not merely document compliance.

A specific design choice that reflects this is the inclusion of **drift-adjusted fairness testing**. The notebook simulates a deterioration in model outputs and recalculates the adverse impact ratio. This is not merely a required documentation step. It asks whether a model that looked acceptable during validation could become harmful when the applicant population changes or macroeconomic conditions shift.

A feature deliberately not included is automated legal sign-off. The tool does not declare that HSBC is legally compliant. It produces monitoring evidence and escalations for human review. That boundary matters because legal and ethical judgement cannot be fully outsourced to a dashboard.

## 4. Who bears the cost if the tool gets it wrong?

Several stakeholders can be harmed:

- **False positives in compliance monitoring**: HSBC may spend unnecessary time reviewing a model that is not actually discriminatory. This increases operational cost and can slow credit access.
- **False negatives in compliance monitoring**: consumers may be unfairly denied credit while the bank believes the model is acceptable. This is the most serious harm because it directly affects access to finance.
- **Incorrect adverse-action explanations in the US**: denied applicants may receive vague or misleading reasons, undermining their ability to improve their credit profile or challenge errors.
- **Weak governance flags in Hong Kong**: senior management may approve AI deployment without sufficient human oversight, privacy assessment, or outcome monitoring.
- **Jurisdictional misconﬁguration**: applying the US output template to Hong Kong, or the Hong Kong governance template to the US, may cause the bank to miss the local regulatory issue that matters most.

The consumer bears the greatest direct cost when the tool fails silently. HSBC bears supervisory, litigation, reputational, and remediation costs. Regulators bear the systemic cost if AI credit scoring becomes normalized without meaningful accountability.
