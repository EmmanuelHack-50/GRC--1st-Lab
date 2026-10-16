# Lab 4 — Third-Party Vendor Risk Assessment
**Focus:** Supply-chain cybersecurity risk | **Framework lens:** ISO/IEC 27001:2022, NIST CSF 2.0, and risk-based third-party due diligence

## Scenario
A fictional EU-based digital services company is reviewing three vendors before renewing or approving services. Each vendor has a different role in the supply chain: payment processing, cloud hosting, and logistics software. The exercise demonstrates how vendor questionnaires can inform risk-based decisions; it is not a certification or a real vendor review.

## Objectives
- Assess security controls across a consistent questionnaire.
- Score responses using a transparent method.
- Compare inherent business exposure and control gaps.
- Recommend proportionate treatment, evidence requests, and follow-up.

## Files
- `01-vendor-risk-questionnaire.md` — questionnaire and scoring rubric.
- `02-vendor-responses-and-scoring.csv` — response scores and rationale by question.
- `03-risk-assessment-and-treatment.md` — results, risk ratings, and actions.
- `04-linkedin-post.md` — short LinkedIn post draft.

## Method
Twelve questions are scored from 0 to 3. The total possible score is 36. The percentage is `total score / 36 × 100`. Higher scores indicate greater control weakness and residual concern.

| Score % | Rating | Suggested decision |
|---:|---|---|
| 0–24% | Low | Proceed with routine monitoring, subject to evidence and contract checks |
| 25–49% | Moderate | Proceed conditionally; track gaps and agree remediation dates |
| 50–74% | High | Escalate for risk-owner approval; require remediation and compensating controls |
| 75–100% | Critical | Do not onboard / suspend sensitive processing until material risks are addressed |

This is a simplified learning model. A real assessment should also consider service criticality, data sensitivity, access, concentration risk, fourth parties, jurisdiction, contract terms, and evidence quality. A low questionnaire score does not automatically mean low overall business risk.

## Important assumptions
All companies, answers, and results are fictional. Scores are illustrative, based on assumed questionnaire responses—not independently verified evidence. This lab is for educational portfolio use only.
