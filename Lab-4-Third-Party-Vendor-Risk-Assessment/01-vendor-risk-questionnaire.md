# Third-Party Vendor Risk Questionnaire

**Scenario:** A fictional EU digital services company is assessing suppliers that may process data, support operations, or connect to internal systems.

## Instructions for the vendor
Answer each question with the current state of your control. Provide evidence where requested (for example, a policy, test summary, certificate scope, or incident procedure). Do not include secrets, credentials, or personal data in evidence submitted for assessment.

## Questionnaire

| ID | Domain | Assessment question | Example evidence to request |
|---|---|---|---|
| Q1 | Governance | Is an accountable person responsible for information security, with approved security policies reviewed at least annually? | Security policy, role/ownership statement |
| Q2 | Asset & data management | Do you classify customer data and restrict access based on business need? | Data-flow diagram, access-control standard |
| Q3 | Identity & access | Is MFA enforced for privileged and remote access, with access reviewed periodically? | MFA policy/configuration evidence, access-review record |
| Q4 | Vulnerability management | Are vulnerabilities tracked, risk-ranked, and remediated within defined timelines? | Vulnerability management policy, redacted remediation metrics |
| Q5 | Secure development / change | Are changes tested and approved, and is software or infrastructure protected against common weaknesses? | Change procedure, test evidence |
| Q6 | Encryption | Is sensitive data encrypted in transit and at rest using appropriate, maintained configurations? | Encryption standard, architecture summary |
| Q7 | Incident response | Is there a documented incident-response process and a contractual process to notify customers promptly? | Incident plan, notification SLA |
| Q8 | Business continuity | Are backups, recovery procedures, and continuity plans tested at a frequency proportionate to service criticality? | BCP/DR summary, latest test outcome |
| Q9 | Subcontractors / fourth parties | Are material subcontractors identified, assessed, monitored, and disclosed when they can affect the service or data? | Subprocessor list, due-diligence procedure |
| Q10 | Compliance & assurance | Can you provide relevant independent assurance or equivalent evidence, and address applicable legal/contractual requirements? | Current audit report/certificate scope, compliance mapping |
| Q11 | Data lifecycle & exit | Are retention, secure deletion, data return, and termination assistance defined contractually and operationally? | Retention/deletion standard, sample exit clause |
| Q12 | Supply-chain resilience | Do you monitor supplier dependencies and have a plan for a critical upstream supplier outage or compromise? | Dependency register, resilience test or scenario exercise |

## Scoring rubric

Score each answer from **0 to 3**:

- **0 — Effective:** Control is implemented and supported by current, relevant evidence.
- **1 — Minor gap:** Control is largely implemented; limited gap with low expected impact.
- **2 — Partial:** Control is inconsistently implemented, weakly evidenced, or has a material gap.
- **3 — Major gap / absent:** Control is missing, ineffective, or no credible evidence is available.

For this exercise, each question has equal weight. Total score ranges from 0 to 36. Calculate `(total score ÷ 36) × 100`; a higher percentage means greater control weakness. Ratings: 0–24% Low; 25–49% Moderate; 50–74% High; 75–100% Critical.

## Due-diligence notes
- Validate important answers against evidence rather than relying on self-attestation.
- Request only proportionate evidence and redact sensitive details.
- Assess the service actually being purchased, data categories, access paths, criticality, and subcontractor dependencies.
- Reassess after material changes, incidents, contract renewal, or a significant change in risk.
- Record the accountable risk owner and obtain formal acceptance for risks that will not be remediated.
