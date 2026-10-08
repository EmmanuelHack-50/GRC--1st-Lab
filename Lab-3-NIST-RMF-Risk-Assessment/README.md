# Lab 3 — NIST RMF Cybersecurity Risk Assessment

**Scenario:** Northstar Cloud Analytics (fictional SaaS environment)  
**Assessment date:** 2026-10-08  
**Assessment type:** System-level cybersecurity risk assessment  
**Framework:** NIST Risk Management Framework (RMF), supported by NIST SP 800-30 Rev. 1  
**Status:** Portfolio / practical GRC exercise

> **Important:** Northstar Cloud Analytics is a fictional organization created for this portfolio lab. No real company, production system, customer data, or security incident was assessed.

## Objective

The objective of this lab was to perform a practical cybersecurity risk assessment for a fictional SaaS organization and produce a risk register that could support security governance, control prioritization, remediation tracking, and an eventual risk-acceptance decision.

The assessment follows the logic of the NIST RMF: **Prepare → Categorize → Select → Implement → Assess → Authorize → Monitor**. NIST describes RMF as a structured process for categorizing systems, selecting and implementing controls, assessing their effectiveness, making risk-based authorization decisions, and continuously monitoring risk.

For the detailed risk-analysis method, this lab uses NIST SP 800-30 Rev. 1, which describes risk as a combination of the likelihood of a threat exploiting a vulnerability and the resulting impact.

## Business scenario

Northstar Cloud Analytics is a fictional B2B SaaS provider. Its platform collects customer account information and business analytics data, exposes a public API, operates production workloads in a cloud environment, and relies on corporate identities, endpoints, third-party SaaS services, CI/CD, centralized logging, and backups.

The assessment assumes a small-to-medium technology organization that is formalizing its information security governance program and wants to improve audit readiness.

### Assessment boundaries

In scope:

- Customer data stores and analytics databases
- Production API and cloud workloads
- Cloud IAM and privileged access
- Backup infrastructure
- CI/CD and source-code management
- Employee endpoints
- Critical third-party SaaS dependencies
- Centralized logging
- Security awareness
- Incident response capability
- Production availability
- Data retention

Out of scope:

- Physical data-center controls owned entirely by cloud providers
- Detailed penetration-testing results
- Financial fraud risk
- HR-specific risks unrelated to information security
- Real customer or employee information

## NIST RMF application

| RMF step | How it was applied in this lab |
|---|---|
| Prepare | Defined the fictional business context, assessment scope, assumptions, stakeholders and risk criteria. |
| Categorize | Identified critical information types and assessed confidentiality, integrity and availability impact. |
| Select | Mapped major risks to representative NIST SP 800-53 control families. |
| Implement | Documented existing/assumed controls and proposed treatment actions. |
| Assess | Evaluated likelihood, impact, inherent risk, control gaps and residual risk. |
| Authorize | Produced a risk-based view that an authorizing official could use to decide whether residual risk is acceptable. |
| Monitor | Assigned owners, target dates and status so risks can be tracked as part of continuous monitoring. |

## System categorization

For this exercise, the overall system impact level is assessed as **HIGH** because a significant compromise of the SaaS platform could materially affect customers and business operations.

| Security objective | Impact | Rationale |
|---|---|---|
| Confidentiality | Moderate | Unauthorized disclosure of customer or business information could cause contractual, reputational and regulatory consequences. |
| Integrity | High | Unauthorized changes to application data, identity privileges or production systems could materially affect customers and business operations. |
| Availability | Moderate | Prolonged service disruption would materially affect customers, revenue and business operations. |
| **Overall** | **High** | The highest security objective impact drives the overall categorization for this portfolio exercise. |

## Risk scoring methodology

Likelihood and impact are scored from **1–5**.

**Risk score = Likelihood × Impact**

| Score | Rating | Suggested response |
|---:|---|---|
| 1–4 | Low | Manage through routine controls and monitoring. |
| 5–9 | Medium | Treat or formally accept with documented ownership and monitoring. |
| 10–15 | High | Prioritize remediation and management oversight. |
| 16–25 | Critical | Immediate management attention and accelerated treatment. |

These thresholds are portfolio-defined for this exercise; NIST does not prescribe a universal scoring matrix.

## Key findings

The assessment identified **12 risks**:

- **4 High inherent risks** driven primarily by privileged access, customer data exposure, application/API risk, and security awareness.
- **6 Medium inherent risks** involving endpoints, third parties, logging, availability and data retention.
- **2 additional High risks** related to backups and incident response.
- No risk was automatically treated as acceptable simply because a control existed; proposed controls were considered in terms of whether they would reduce likelihood or impact.
- The highest-priority themes are **identity and privileged access, customer-data protection, application security, resilience, and audit-quality evidence**.

## Risk treatment philosophy

The default response in this assessment is **Reduce/Mitigate**, because the identified risks are generally controllable through additional technical, administrative and governance measures.

Treatment decisions are deliberately written as actions rather than generic recommendations. For example:

> “Improve access control” is weak.

Whereas:

> “Introduce quarterly access recertification, phishing-resistant MFA for administrators, and privileged activity logging” is actionable, assignable and auditable.

## Deliverables

- [Risk Assessment Narrative](./risk-assessment.md)
- [Risk Register — CSV](./risk-register.csv)
- [Risk Register — Excel](./NIST_RMF_Risk_Register_Northstar_Cloud_Analytics.xlsx)

## What I would do next in a real environment

A real assessment would require evidence validation before final risk ratings were accepted. The next steps would include:

1. Validate asset ownership and business criticality with system owners.
2. Confirm actual vulnerabilities and threat scenarios using evidence.
3. Review existing policies, procedures and technical configurations.
4. Test whether selected controls are implemented and operating effectively.
5. Assign accountable risk owners.
6. Create remediation actions/POA&M items for accepted treatment plans.
7. Obtain documented risk acceptance for residual risks above the organization's tolerance.
8. Establish a monitoring cadence and reassessment triggers.

## References

- NIST SP 800-37 Rev. 2 — Risk Management Framework
- NIST SP 800-30 Rev. 1 — Guide for Conducting Risk Assessments
- NIST SP 800-53 — Security and Privacy Controls for Information Systems and Organizations

This lab is intended to demonstrate practical GRC reasoning, not to claim a formal NIST assessment or certification.
