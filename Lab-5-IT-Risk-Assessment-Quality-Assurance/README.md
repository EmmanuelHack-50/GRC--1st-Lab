# Lab 5 — IT Risk Assessment Quality Assurance

**Focus:** IT risk assessment review, quality assurance (QA), stakeholder engagement and continuous improvement  
**Environment:** Fictional EU-based digital services organization  
**Framework lens:** Internal IT Risk Assessment Standard, ISO/IEC 27001:2022, and NIST SP 800-30 Rev. 1  
**Lab type:** Practical Cybersecurity GRC portfolio simulation

> **Portfolio disclaimer:** The organization, people, systems, assessment records, evidence references and results in this lab are fictional and created for learning purposes. This is a simulated second-line/QA review, not an external audit, certification assessment or review of a real organization's controls.

## 1. Business scenario

Northstar Digital Services (NDS) is a fictional EU-based technology company providing a customer portal and managed digital services to business clients. Its GRC team has introduced a consistent IT risk assessment process. Before assessment outcomes are finalized and reported, the Quality Assurance function performs a risk-based review of selected assessments.

The QA reviewer is not expected to redo the assessor's work or own the underlying risks. The reviewer checks whether the assessment is complete, evidence-led, internally consistent, aligned with the organization's methodology and clear enough for a risk owner or management forum to make a decision.

For this exercise, three completed assessments are selected for QA sampling:

1. **Customer Portal — privileged access and identity management**
2. **Cloud Backup Service — backup resilience and recovery testing**
3. **Service Desk Platform — third-party access and supplier oversight**

The sample deliberately includes different levels of assessment quality so that the reviewer must distinguish documentation weaknesses from substantive risk concerns.

## 2. Objectives

By completing this lab, I demonstrate how to:

- Review selected IT risk assessments against defined internal requirements.
- Check scope, asset/service context, risk statements, likelihood, impact, control effectiveness, residual risk and treatment plans.
- Assess whether evidence is relevant, current, attributable and sufficient to support conclusions.
- Identify gaps, inconsistencies and unsupported assumptions.
- Agree proportionate corrective actions with assessors and service owners.
- Maintain traceable QA records and action ownership.
- Analyse recurring quality themes and recommend practical improvements.
- Prepare concise quality reporting for GRC management.

## 3. QA review criteria

The simulated internal standard uses the following review criteria. They are portfolio-defined criteria informed by established risk-management and information-security practices; they are not presented as verbatim ISO or NIST requirements.

| ID | QA criterion | What the reviewer checks |
|---|---|---|
| QA-01 | Scope and context | Service, owner, boundaries, dependencies and assessment date are clear. |
| QA-02 | Risk statement | Cause, risk event and business impact are understandable and specific. |
| QA-03 | Inherent risk | Likelihood and impact rationale is documented before considering controls. |
| QA-04 | Control assessment | Relevant controls are identified and implementation/effectiveness is not assumed. |
| QA-05 | Evidence quality | Evidence is identifiable, relevant, sufficiently current and supports the conclusion. |
| QA-06 | Residual risk | Residual rating follows the stated methodology and reflects control effectiveness. |
| QA-07 | Treatment plan | Actions are specific, measurable, assigned to an owner and time-bound. |
| QA-08 | Risk ownership | A named role accepts accountability; acceptance/escalation is documented where needed. |
| QA-09 | Traceability | Assessment version, reviewer, review date, comments and decisions are recorded. |
| QA-10 | Clarity and consistency | Ratings, narrative, register entries and recommendations do not contradict each other. |

### Review outcomes

- **Pass:** No material QA issue identified; minor editorial suggestions may remain.
- **Pass with observations:** Assessment is usable, but non-material improvements should be tracked.
- **Rework required:** One or more material gaps prevent reliable interpretation or decision-making.
- **Escalate:** A significant risk, evidence concern or unresolved disagreement requires management attention.

A QA finding is not automatically a new security risk. It may be a documentation, methodology, evidence or governance weakness that affects confidence in the assessment.

## 4. Review approach

1. Select a risk-based sample and record why each assessment was selected.
2. Confirm the assessment version, scope, service owner and assessor.
3. Review the assessment against QA-01 to QA-10.
4. Trace key conclusions to the evidence references supplied.
5. Check that risk ratings and treatment decisions follow the stated methodology.
6. Record findings with clear rationale and severity.
7. Discuss factual gaps with the assessor and service owner.
8. Agree an action, accountable owner and target date.
9. Record the response, closure evidence and QA disposition.
10. Aggregate recurring themes for quality reporting.

### Evidence quality questions

- Does the evidence actually support the control conclusion?
- Is the evidence relevant to the system and assessment period?
- Is the source identifiable and is the reference traceable?
- Does the evidence demonstrate operation, or only the existence of a policy?
- Are limitations or assumptions clearly stated?

## 5. Simulated QA results

| Assessment | QA outcome | Main observation |
|---|---|---|
| Customer Portal | Rework required | Residual risk was rated Medium despite incomplete privileged-access evidence and no documented rationale for control effectiveness. |
| Cloud Backup Service | Pass with observations | Recovery test evidence was referenced, but the evidence period and service scope needed clarification. |
| Service Desk Platform | Rework required | Supplier access review was described as complete, but no dated review record or accountable approver was referenced. |

These are simulated results based on the fictional records in this lab, not verified findings about a real environment.

## 6. Key QA findings and agreed next steps

### Finding QA-01 — Unsupported residual risk rationale
**Assessment:** Customer Portal  
**Issue:** The assessment records privileged access controls as effective, but the evidence reference does not demonstrate that all privileged accounts were reviewed during the assessment period. The residual risk rationale is therefore not sufficiently supported.

**Agreed action:** The assessor will obtain a dated privileged-access review record, confirm scope and exceptions with the service owner, and reassess control effectiveness and residual risk. If evidence cannot be obtained, the limitation must be recorded and the rating reconsidered.

### Finding QA-02 — Evidence scope and period unclear
**Assessment:** Cloud Backup Service  
**Issue:** A recovery test is referenced, but the assessment does not make clear whether the test covered the service's critical workloads or whether the results remain representative of the current environment.

**Agreed action:** The service owner will confirm the workload scope, test date, outcome and outstanding recovery actions. The assessor will update the evidence reference and clarify any limitations.

### Finding QA-03 — Supplier access review not traceable
**Assessment:** Service Desk Platform  
**Issue:** The assessment states that supplier access is reviewed periodically, but no dated review record, population or approver is referenced.

**Agreed action:** The assessor and service owner will provide the latest access-review record, identify exceptions and confirm the approval trail. Until evidence is available, the control conclusion must not be presented as independently substantiated.

## 7. QA reporting and recurring themes

The three-record sample indicates recurring weaknesses in:

- Evidence traceability and sufficiency.
- Rationale supporting control effectiveness.
- Consistency between control conclusions and residual risk ratings.
- Clear ownership and approval records.

### Recommended improvements

| Theme | Practical improvement | Expected benefit |
|---|---|---|
| Evidence quality | Introduce mandatory evidence reference, date, owner and scope fields. | More traceable assessments and easier review. |
| Risk-rating consistency | Add a short rationale field for likelihood, impact and residual risk. | Fewer unsupported ratings. |
| Treatment ownership | Require action owner, due date, status and closure evidence. | Clearer accountability. |
| Assessor guidance | Publish worked examples of strong and weak risk statements. | More consistent assessment quality. |
| QA calibration | Hold periodic reviewer sessions using anonymised sample cases. | More consistent QA decisions. |
| Reporting | Track QA outcomes and recurring finding categories monthly or quarterly. | Better visibility of process weaknesses. |

### Illustrative quality metrics

For this sample of three assessments:

- 2 of 3 assessments require rework.
- 1 of 3 passes with observations.
- 3 material QA findings are recorded.
- Evidence traceability is a recurring theme across the sample.

These figures describe the small fictional sample only. They should not be interpreted as a statistically representative team performance measure.

## 8. Roles and responsibilities

| Role | Responsibility |
|---|---|
| QA reviewer | Independently checks assessment quality, records findings and tracks disposition. |
| Risk assessor | Explains assessment rationale, corrects documentation and updates ratings where justified. |
| Service owner | Confirms service context, provides evidence and agrees practical actions. |
| Risk owner | Owns the underlying risk and makes or escalates risk treatment/acceptance decisions. |
| GRC manager | Reviews trends, resolves escalations and sponsors process improvements. |

The QA reviewer does not take ownership of the service risk or unilaterally accept residual risk.

## 9. Deliverables in this folder

- `README.md` — scenario, method, findings, reporting and lessons learned.
- `01-qa-review-checklist.md` — reusable review checklist and disposition guidance.
- `02-qa-review-log.csv` — sample QA records, findings, owners and follow-up.
- `03-quality-improvement-report.md` — recurring themes, metrics and improvement plan.
- `04-linkedin-post.md` — professional LinkedIn post draft.

## 10. What I learned

This exercise reinforced that a risk assessment is only as useful as the quality of the evidence, reasoning and ownership behind it. Quality assurance is not about finding fault with assessors; it is about making sure risk information is reliable enough to support sound decisions.

A good QA reviewer asks constructive questions, distinguishes missing documentation from genuine control weaknesses, records limitations honestly and works with stakeholders to agree realistic next steps.

## 11. References

- ISO/IEC 27001:2022 — Information security management systems — Requirements.
- ISO/IEC 27005:2022 — Guidance on managing information security risks.
- NIST SP 800-30 Rev. 1 — Guide for Conducting Risk Assessments.
- NIST Cybersecurity Framework 2.0 — Govern, Identify, Protect, Detect, Respond and Recover.

Use of these references is a framework lens for the simulation; this lab does not claim formal compliance, certification or an independently conducted audit.

---
**Portfolio note:** This is a fictional, self-directed practical exercise designed to demonstrate entry-level Cybersecurity GRC and IT risk assessment QA thinking.
