# Risk Assessment Narrative

## 1. Assessment context

Northstar Cloud Analytics is modeled as a SaaS company preparing to mature its information security governance program.

The assessment asks a practical GRC question:

> **Which information-security risks deserve management attention first, why, who owns them, and what should be done about them?**

The exercise is not a vulnerability scan. It is a governance-oriented risk assessment using documented assumptions and a repeatable scoring method.

## 2. Asset identification

The first step was to identify assets that support important business functions.

| Asset | Business value | Primary security concern | Owner |
|---|---|---|---|
| Customer Data Store | Customer service and analytics | Confidentiality / integrity | Data Owner |
| Production API | Customer-facing service | Authorization / availability | Engineering |
| Cloud IAM | Administrative access | Privilege compromise | Security / IAM |
| Backups | Recovery capability | Recoverability | Infrastructure |
| CI/CD Pipeline | Software delivery | Supply-chain integrity | Engineering |
| Employee Endpoints | Workforce productivity and access | Credential/data compromise | IT |
| Third-Party SaaS | Business operations | Supplier dependency | GRC / Procurement |
| Logging Platform | Detection and evidence | Visibility / tampering | Security Operations |
| Security Awareness | Human security layer | Phishing / social engineering | GRC / People |
| Incident Response | Security resilience | Response delay | Security / GRC |
| Production Availability | Customer service | Outage / capacity | Infrastructure |
| Data Retention | Governance and privacy | Excessive data exposure | Data Governance |

## 3. Threat and vulnerability analysis

The assessment connects realistic threat sources to conditions that could allow a threat event to succeed.

Examples:

- **Threat:** stolen administrator credentials  
  **Condition:** privileged accounts without strong phishing-resistant MFA or timely access review  
  **Potential impact:** unauthorized infrastructure changes or customer-data access

- **Threat:** external attacker  
  **Condition:** API authorization weakness  
  **Potential impact:** unauthorized access to customer information

- **Threat:** ransomware  
  **Condition:** backups that are reachable using production credentials  
  **Potential impact:** inability to restore critical services

- **Threat:** malicious or compromised software dependency  
  **Condition:** weak CI/CD controls or exposed deployment credentials  
  **Potential impact:** malicious code reaching production

- **Threat:** phishing/social engineering  
  **Condition:** inconsistent security awareness and reporting behavior  
  **Potential impact:** credential compromise and unauthorized access

NIST SP 800-30 describes this process as considering threat sources, threat events, vulnerabilities, likelihood and adverse impact when determining risk.

## 4. Likelihood assessment

Likelihood considers how plausible successful exploitation is under the assumed environment.

A score of 4 does **not** mean that an event will happen. It means the scenario is considered likely enough to require active treatment.

Factors considered:

- Exposure to the internet
- Privilege level of the affected asset
- Attractiveness of the target
- Existing control maturity
- Human dependency
- Ease of exploitation
- Frequency of the threat
- Detectability and response capability

## 5. Impact assessment

Impact considers consequences to:

- Customer confidentiality
- Data integrity
- Service availability
- Business operations
- Contractual obligations
- Regulatory exposure
- Reputation
- Incident response and recovery effort

The scoring is deliberately business-oriented. A GRC practitioner should be able to explain why a risk matters to the organization, not only why it matters technically.

## 6. Inherent risk

Inherent risk represents the risk before considering the effect of planned additional controls.

Example:

**RA-003 — Cloud IAM**

- Likelihood: 4
- Impact: 5
- Inherent score: 20
- Rating: High

The reason is straightforward: compromise of a privileged cloud identity can create a broad blast radius across production systems and sensitive data.

## 7. Risk treatment

Treatment actions were selected to reduce either likelihood or impact.

For example, RA-003 proposes:

- Phishing-resistant MFA for administrators
- Privileged access management / just-in-time access
- Regular access recertification
- Privileged activity alerting

The objective is not to claim that these controls eliminate the risk. The objective is to reduce the probability and/or consequences of a successful compromise.

## 8. Residual risk

Residual risk is the remaining risk after the planned treatment is assumed to be implemented effectively.

Example:

**RA-003 — Cloud IAM**

- Inherent: 20 / High
- Residual likelihood: 2
- Residual impact: 5
- Residual score: 10 / Medium

The impact remains high because a successful privileged-account compromise could still be severe. The main reduction is expected to come from lowering the likelihood of compromise and misuse.

This distinction is important in GRC: a control does not necessarily reduce the potential impact of an event; it may primarily reduce its likelihood.

## 9. Risk register management

Each risk has:

- Unique risk ID
- Asset
- Information/value at risk
- Threat source
- Risk statement
- Relevant control families
- Likelihood
- Impact
- Inherent score/rating
- Treatment action
- Risk owner
- Response decision
- Residual likelihood
- Residual impact
- Residual score/rating
- Target date
- Status

This structure makes the register useful for management reporting and audit follow-up rather than being a static spreadsheet.

## 10. Example management decision

If the organization has a risk appetite of Medium or below, a residual High risk should normally require additional treatment or documented acceptance by the appropriate authority.

For example:

> **RA-001 — Customer Data Store:** residual risk remains Medium after the planned access-control improvements. The risk owner should confirm implementation and provide evidence before the risk is considered effectively treated.

The authorizing decision should be made by the appropriate business/security authority, not by the analyst performing the assessment.

## 11. Assessment limitations

This is a portfolio simulation.

The assessment does not include:

- Interviews with system owners
- Production configuration review
- Vulnerability scan results
- Penetration-testing evidence
- Actual incident history
- Vendor contracts
- Actual audit findings
- Verified control operating effectiveness

Therefore, the ratings are **reasonable assessment assumptions**, not claims about a real production environment.

## 12. GRC takeaway

The main lesson from this lab is that risk assessment is not simply “finding vulnerabilities.”

A useful GRC assessment connects:

**Business asset → threat → vulnerability/condition → likelihood → impact → risk → control → treatment → residual risk → owner → evidence → monitoring**

That chain is what allows technical security findings to become management decisions.
