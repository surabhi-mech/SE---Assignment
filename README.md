# Software Engineering Assignment
## SDLC Model Selection

| | |
|---|---|
| **Course** | Software Engineering |
| **Topic** | SDLC Model Selection |
| **Project Selected** | Banking System |
| **Model Selected** | Waterfall Model |
| **Submitted by** | Surabhi Mech |
| **Roll No.** | 230710007063 |
| **Date** | 25/04/2026 |

---

## 1. Introduction

A **Banking System** is a large-scale, mission-critical software application used by banks to manage customer accounts, process transactions, handle loans, and ensure secure financial operations. Examples include core banking systems used by State Bank of India (SBI), HDFC Bank, ICICI Bank, etc.

This system typically includes the following modules:

- Customer account management (savings, current, fixed deposit)
- Fund transfer and transaction processing
- Loan and EMI management
- ATM and online banking integration
- Admin panel for bank employees
- Audit and compliance reporting

A Banking System must be extremely secure, well-documented, and fully tested before going live. Even a single bug can result in financial loss or legal consequences. Therefore, a model that supports careful, phase-by-phase development with zero room for mid-project changes is required.

---

## 2. Selected SDLC Model

### ✅ Waterfall Model

The Waterfall Model is a linear and sequential SDLC model where development flows downward through fixed phases, just like a waterfall. Each phase must be fully completed and approved before moving to the next phase. There is no going back once a phase is complete.

The six phases of the Waterfall Model as applied to the Banking System are:

| Phase | Activity in Banking System | Output |
|---|---|---|
| Phase 1: Requirements | Gather banking rules, RBI regulations, legal compliance, user needs | Software Requirements Specification (SRS) |
| Phase 2: System Design | Database schema, security architecture, UI/UX wireframes, module design | High-level and low-level design documents |
| Phase 3: Implementation | Code all modules — accounts, loans, transactions, authentication, admin panel | Fully coded banking application |
| Phase 4: Testing | Security audits, load testing, penetration testing, UAT | Test reports, bug fixes, approved system |
| Phase 5: Deployment | Full system rollout to all bank branches, ATMs, and online portals | Live banking system accessible to customers |
| Phase 6: Maintenance | Bug fixes, security patches, regulatory compliance updates | Updated, stable, and compliant banking system |

---

## 3. Justification

### 3.1 Requirement Stability

Banking systems operate under strict government regulations, RBI guidelines, and legal frameworks. These requirements are well-defined, documented, and do not change during development. Since Waterfall requires all requirements to be finalized before development begins, it is a perfect fit for banking where requirements are stable and fixed from the start.

**What is gathered during the Requirements phase:**

- **Functional Requirements:** User registration, login, authentication, account management, fund transfers (NEFT, RTGS, IMPS, UPI), loan management, ATM integration, admin panel, statement generation
- **Non-Functional Requirements:** Security (end-to-end encryption, 2FA), Performance (thousands of simultaneous transactions), Availability (99.99% uptime), Compliance (RBI guidelines, ISO 27001, PCI-DSS)
- **Regulatory Requirements:** KYC norms, AML rules, Data privacy laws (IT Act), RBI circulars, Audit trail for every transaction

> Output: A formal **Software Requirements Specification (SRS)** document, reviewed, approved, and signed off by all stakeholders. Once signed, requirements are **frozen** — no changes allowed.

### 3.2 Risk Level

Banking software is a safety-critical system. Errors in financial transactions can cause massive financial loss, legal liability, and loss of customer trust. The Waterfall Model reduces this risk by ensuring that each phase is thoroughly reviewed and verified before the next one begins.

| Risk | Impact |
|---|---|
| Data migration failure | Customer accounts corrupted or lost |
| Integration failure | ATMs and UPI payments stop working |
| Security gap | Financial fraud or data breach |
| Server overload | System crashes under real user traffic |
| Rollback needed | Old system must be kept ready as backup |

### 3.3 Complexity

A Banking System is highly complex, involving many interconnected modules — frontend, backend, database, and third-party integrations (ATM networks, payment gateways, government databases like Aadhaar and PAN). The Waterfall Model handles this complexity by breaking it into well-defined phases, allowing teams to focus on one phase at a time without confusion or overlap.

### 3.4 User Involvement

In a Banking System, the client (bank management) provides all requirements at the beginning. After that, they are not expected to be involved during development — which is exactly how Waterfall works. The client reviews the final product only at the end, which suits a formal banking environment where continuous client interaction during development is not practical.

### 3.5 Flexibility

A Banking System does **NOT** need to be flexible. In fact, too much flexibility is dangerous in banking software. The Waterfall Model's low flexibility is actually an advantage here because it enforces strict control over the development process, ensures every feature is planned in advance, and prevents scope creep that could introduce security vulnerabilities.

**Summary of justification factors:**

| Factor | Rating | Reason |
|---|---|---|
| Requirement Stability | HIGH | Fixed by law and regulation |
| Risk Level | LOW | Each phase fully verified before next |
| Complexity | HIGH | Managed phase by phase |
| User Involvement | LOW | Only at start and end |
| Flexibility | LOW | Advantage in a regulated environment |

---

## 4. Comparison with Other Models

| Criterion | Waterfall ✅ | Agile ❌ | Spiral ❌ |
|---|---|---|---|
| Requirement change | Not allowed (ideal) | Frequent changes | Allowed but complex |
| Documentation | Very thorough | Minimal | Moderate |
| User feedback | At start and end only | Every sprint | Every cycle |
| Security focus | Fully tested at once | Distributed testing | Risk-driven only |
| Suitable for banking | Yes | No | No |
| Partial delivery | Not done (correct) | Common practice | Done per cycle |

### ❌ Why Not Agile?

The Agile Model works in short sprints with frequent deliveries and constant client involvement. While this works well for startups and web apps, it is unsuitable for a Banking System because:

- Agile allows frequent requirement changes — dangerous in a regulated banking environment
- Agile lacks thorough documentation — banking systems require complete audit trails
- Partial deliveries (e.g., deploying accounts module without transactions) are unacceptable in banking
- Security audits cannot be done properly sprint-by-sprint

### ❌ Why Not Spiral?

The Spiral Model is designed for high-risk, research-oriented projects with repeated cycles of planning and risk analysis. It is unsuitable for a Banking System because:

- Banking requirements are already well-understood — no need for repeated risk analysis cycles
- The Spiral Model adds unnecessary overhead and cost for a project with stable requirements
- It is typically used for large government or defense projects, not commercial banking software

---

## 5. Diagram of the Waterfall Model

```
+----------------------------------------------------------+
|   PHASE 1: REQUIREMENTS ANALYSIS                         |
|   Gather banking rules, regulations, user needs          |
|   Output: SRS Document                                   |
+----------------------------------------------------------+
                        |
                        v  (approved and frozen)
+----------------------------------------------------------+
|   PHASE 2: SYSTEM DESIGN                                 |
|   Architecture, DB schema, security design               |
|   Output: High-level and low-level design documents      |
+----------------------------------------------------------+
                        |
                        v  (design signed off)
+----------------------------------------------------------+
|   PHASE 3: IMPLEMENTATION                                |
|   Coding: accounts, loans, transactions, auth            |
|   Output: Fully coded banking application                |
+----------------------------------------------------------+
                        |
                        v  (code complete)
+----------------------------------------------------------+
|   PHASE 4: TESTING                                       |
|   Security audits, load tests, UAT                       |
|   Output: Test reports, approved system                  |
+----------------------------------------------------------+
                        |
                        v  (all tests passed)
+----------------------------------------------------------+
|   PHASE 5: DEPLOYMENT                                    |
|   Full rollout to all bank branches and portals          |
|   Output: Live banking system                            |
+----------------------------------------------------------+
                        |
                        v  (system live)
+----------------------------------------------------------+
|   PHASE 6: MAINTENANCE                                   |
|   Bug fixes, compliance updates, security patches        |
|   Output: Updated and stable banking system              |
+----------------------------------------------------------+
```

> **Note:** Each phase must be fully completed and approved before the next phase begins. No going back — sequential, top-down flow only.

---

## 6. Conclusion

After carefully analyzing all the important factors — requirement stability, risk level, complexity, user involvement, and flexibility — it is clear that the **Waterfall Model** is the most suitable SDLC model for developing a **Banking System**.

The Banking System requires a structured, disciplined, and thoroughly documented development process. It cannot afford mid-project changes, partial deliveries, or undocumented decisions. The Waterfall Model addresses all of these needs perfectly by enforcing a strict sequential process where each phase is verified before the next begins.

Other models like **Agile** and **Spiral** were considered but found unsuitable due to their flexibility, lack of documentation discipline, and iterative delivery approach — all of which are inappropriate for a safety-critical, regulation-bound banking environment.

Therefore, it can be confidently concluded that the **Waterfall Model is the best and most appropriate SDLC model for a Banking System**.

---

*End of Assignment*
