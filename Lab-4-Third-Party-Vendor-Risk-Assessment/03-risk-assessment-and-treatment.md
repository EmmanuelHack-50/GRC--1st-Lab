# Vendor Risk Assessment — Results & Treatment Plan

## Executive summary
This tabletop assessment compares three fictional EU vendors using the same 12-question questionnaire. Scores measure **control weakness**, not a vendor's overall inherent business criticality. Service criticality and data exposure must be assessed separately before a real onboarding decision.

| Vendor | Country | Service | Score | Percentage | Rating |
|---|---|---|---:|---:|---|
| BalticPay UAB | Lithuania | Payment processing | 6/36 | 16.7% | Low |
| RhineCloud GmbH | Germany | Cloud hosting | 14/36 | 38.9% | Moderate |
| IberiaLogistics SL | Spain | Logistics SaaS | 23/36 | 63.9% | High |

**Calculation:** percentage = total response score ÷ 36 × 100. Ratings: 0–24% Low; 25–49% Moderate; 50–74% High; 75–100% Critical.

## Vendor findings

### V1 — BalticPay UAB (fictional; Lithuania)
**Rating: Low (6/36; 16.7%)**

**Strengths:** Privileged/remote MFA, encryption, change controls, subcontractor disclosure, and scoped assurance are reported as implemented.

**Gaps to validate:** Data access mapping, vulnerability metrics, incident-notification wording, recovery-test evidence, deletion/exit evidence, and upstream outage testing.

**Treatment:** Conditional approval for the defined service, subject to validating current assurance scope, agreeing an incident-notification SLA, and documenting recovery/exit evidence. Reassess annually and after a material incident or service change.

### V2 — RhineCloud GmbH (fictional; Germany)
**Rating: Moderate (14/36; 38.9%)**

**Strengths:** Encryption is reported as enabled; core governance and operational processes exist.

**Key gaps:** Overdue vulnerability tracking, incomplete recovery testing for critical workloads, inconsistent change-test records, and limited evidence of upstream dependency exercises.

**Treatment:** Conditional approval only after the business owner accepts the residual risk. Request a dated remediation plan, evidence of vulnerability SLA monitoring, a recovery test covering critical workloads, and confirmation of assurance-report scope. Track actions monthly until closed.

### V3 — IberiaLogistics SL (fictional; Spain)
**Rating: High (23/36; 63.9%)**

**Strengths:** Some encryption and data-deletion commitments are reported; this is not enough to offset the material control gaps.

**Key gaps:** Inconsistent MFA for remote administration, weak vulnerability-remediation evidence, no evidenced recovery test for the critical service, informal incident response, and incomplete subcontractor oversight. These weaknesses may amplify a compromise or outage across the supply chain.

**Treatment:** Escalate to the service owner and GRC/security lead. Do not onboard for sensitive or business-critical processing until minimum controls are evidenced or an explicitly approved, time-bound exception with compensating controls is in place. Require MFA coverage, vulnerability remediation SLAs, tested recovery, an incident-notification commitment, and a current subcontractor inventory before approval.

## Risk register

| ID | Risk statement | Vendor | Likelihood | Impact | Priority / treatment |
|---|---|---|---|---|---|
| R1 | Inadequate vulnerability remediation could allow exploitation of a supplier-hosted service and affect connected business operations. | RhineCloud GmbH | Medium | High | High priority: remediation SLA, overdue-finding reporting, evidence review |
| R2 | Incomplete recovery testing could prolong an outage in a critical cloud dependency. | RhineCloud GmbH | Medium | High | High priority: test critical workloads and document recovery results |
| R3 | Weak remote-admin MFA and vulnerability controls could enable unauthorized access to the logistics SaaS service. | IberiaLogistics SL | High | High | Escalate; remediate before sensitive onboarding |
| R4 | Unclear incident notification and incomplete subcontractor oversight could delay response to a supplier or fourth-party incident. | IberiaLogistics SL | Medium | High | Contractual notification SLA, named subprocessors, periodic reviews |
| R5 | Limited evidence of upstream dependency resilience could cause a disruption to cascade through the supply chain. | All vendors (different maturity) | Medium | Medium–High | Maintain dependency mapping and test realistic outage scenarios |

Likelihood and impact above are qualitative exercise judgments, not calculated from the questionnaire score. A real risk register should define rating criteria and assign an accountable owner and due date.

## Prioritized remediation tracker

| Priority | Vendor | Action | Evidence of closure | Target |
|---|---|---|---|---|
| 1 | IberiaLogistics SL | Enforce MFA for all remote and privileged access; document exceptions | Configuration evidence and exception register | Before sensitive onboarding |
| 2 | IberiaLogistics SL | Define vulnerability severity and remediation SLAs; track overdue items | Approved procedure and remediation report | Within 30 days |
| 3 | IberiaLogistics SL | Test recovery for the critical service and document recovery objectives | Test report, issues, and corrective actions | Within 45 days |
| 4 | IberiaLogistics SL | Formalize incident response, customer notification, and subcontractor inventory | Approved plan, contract clause, subprocessor register | Within 30 days |
| 5 | RhineCloud GmbH | Test recovery for all critical workloads and evidence vulnerability tracking | Test results and remediation dashboard | Within 60 days |
| 6 | RhineCloud GmbH | Confirm assurance scope and conduct upstream dependency exercise | Scope mapping and exercise report | Within 60 days |
| 7 | BalticPay UAB | Validate assurance scope, notification SLA, recovery and exit evidence | Evidence pack and signed contract terms | Before renewal |

Targets are illustrative planning assumptions and should be agreed with vendors and risk owners. The risk owner should document acceptance where remediation is deferred.

## Decision principles
1. **Questionnaire score is a signal, not the decision.** Combine it with inherent risk, business criticality, data sensitivity, connectivity, and concentration risk.
2. **Validate evidence.** Self-attested responses should not be treated as verified control effectiveness.
3. **Contract for resilience.** Address incident notification, audit/evidence rights, subcontracting, continuity, data return/deletion, and exit support.
4. **Monitor the supply chain.** Reassess at renewal, after major service changes, and after relevant incidents; identify critical fourth parties.
5. **Record accountability.** Assign an owner, due date, closure evidence, and formal approval for accepted residual risk.

## Framework alignment (high-level)
- **ISO/IEC 27001:2022:** supplier relationships and information security in supplier agreements; assess applicable controls in the organization's Statement of Applicability.
- **NIST CSF 2.0:** Govern (GV.SC supply-chain risk management), Identify, Protect, Detect, Respond, Recover.
- **GDPR:** where personal data processing is involved, assess controller/processor roles, Article 28 contractual requirements, security measures, and relevant transfer/subprocessor considerations with appropriate legal review.

This is an educational simulation, not legal advice, a compliance determination, or a claim that any real organization was assessed.
