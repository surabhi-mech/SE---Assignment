================================================================
       SOFTWARE ENGINEERING ASSIGNMENT
       SDLC Model Selection
================================================================
Course: Software Engineering
Topic: SDLC Model Selection
Project Selected: Banking System
Model Selected: Waterfall Model
Submitted by: Surabhi Mech
Roll No.: 230710007063
Date: 25/04/2026
================================================================


================================================================
1. INTRODUCTION
================================================================

A Banking System is a large-scale, mission-critical software
application used by banks to manage customer accounts, process
transactions, handle loans, and ensure secure financial
operations. Examples include core banking systems used by
State Bank of India (SBI), HDFC Bank, ICICI Bank, etc.

This system typically includes the following modules:

  - Customer account management (savings, current, fixed deposit)
  - Fund transfer and transaction processing
  - Loan and EMI management
  - ATM and online banking integration
  - Admin panel for bank employees
  - Audit and compliance reporting

A Banking System must be extremely secure, well-documented,
and fully tested before going live. Even a single bug can
result in financial loss or legal consequences. Therefore,
a model that supports careful, phase-by-phase development
with zero room for mid-project changes is required.


================================================================
2. SELECTED SDLC MODEL
================================================================

Selected Model: Waterfall Model

The Waterfall Model is a linear and sequential SDLC model
where development flows downward through fixed phases, just
like a waterfall. Each phase must be fully completed and
approved before moving to the next phase. There is no going
back once a phase is complete.

The six phases of the Waterfall Model as applied to the
Banking System are:

  +----------------------------------------------------------+
  |  PHASE 1: REQUIREMENTS ANALYSIS                          |
  |  Gather banking rules, RBI regulations, legal            |
  |  compliance, and user needs                              |
  |  Output: Software Requirements Specification (SRS)       |
  +----------------------------------------------------------+
                          |
                          v
  +----------------------------------------------------------+
  |  PHASE 2: SYSTEM DESIGN                                  |
  |  Database schema, security architecture, UI/UX           |
  |  wireframes, module design                               |
  |  Output: High-level and low-level design documents       |
  +----------------------------------------------------------+
                          |
                          v
  +----------------------------------------------------------+
  |  PHASE 3: IMPLEMENTATION (CODING)                        |
  |  Code all modules: accounts, loans, transactions,        |
  |  authentication, admin panel                             |
  |  Output: Fully coded banking application                 |
  +----------------------------------------------------------+
                          |
                          v
  +----------------------------------------------------------+
  |  PHASE 4: TESTING AND VERIFICATION                       |
  |  Security audits, load testing, penetration testing,     |
  |  User Acceptance Testing (UAT)                           |
  |  Output: Test reports, bug fixes, approved system        |
  +----------------------------------------------------------+
                          |
                          v
  +----------------------------------------------------------+
  |  PHASE 5: DEPLOYMENT                                     |
  |  Full system rollout to all bank branches, ATMs,         |
  |  and online portals                                      |
  |  Output: Live banking system accessible to customers     |
  +----------------------------------------------------------+
                          |
                          v
  +----------------------------------------------------------+
  |  PHASE 6: MAINTENANCE                                    |
  |  Bug fixes, security patches, regulatory compliance      |
  |  updates, performance tuning                             |
  |  Output: Updated, stable, and compliant banking system   |
  +----------------------------------------------------------+

NOTE: Each phase must be fully completed and approved before
the next phase begins. No going back. Sequential flow only.


================================================================
3. JUSTIFICATION
================================================================

The Waterfall Model is the most suitable choice for a Banking
System due to the following reasons:

----------------------------------------------------------------
3.1 REQUIREMENT STABILITY
----------------------------------------------------------------

Banking systems operate under strict government regulations,
RBI guidelines, and legal frameworks. These requirements are
well-defined, documented, and do not change during
development. Since Waterfall requires all requirements to be
finalized before development begins, it is a perfect fit for
banking where requirements are stable and fixed from the start.

Example: Features like interest calculation rates, KYC norms,
and transaction limits are defined by law and cannot change
mid-project.

What is gathered during Requirements phase:

  Functional Requirements (what the system must do):
  - User registration, login, and authentication
  - Account management (savings, current, fixed deposit)
  - Fund transfers (NEFT, RTGS, IMPS, UPI)
  - Loan application and EMI management
  - ATM integration and card management
  - Admin panel for bank employees
  - Statement generation and download

  Non-Functional Requirements (how well it must perform):
  - Security: end-to-end encryption, two-factor authentication
  - Performance: handle thousands of simultaneous transactions
  - Availability: 99.99% uptime (banking cannot go down)
  - Scalability: must handle growth in users over time
  - Compliance: RBI guidelines, ISO 27001, PCI-DSS standards

  Regulatory and Legal Requirements:
  - KYC (Know Your Customer) norms
  - AML (Anti-Money Laundering) rules
  - Data privacy laws (IT Act, GDPR if applicable)
  - RBI circulars on digital banking
  - Audit trail: every transaction must be logged

  Output of this phase:
  A formal document called the Software Requirements
  Specification (SRS) is produced, reviewed, approved,
  and signed off by all stakeholders. Once signed,
  requirements are frozen and no changes are allowed.

----------------------------------------------------------------
3.2 RISK LEVEL
----------------------------------------------------------------

Banking software is a safety-critical system. Errors in
financial transactions can cause massive financial loss,
legal liability, and loss of customer trust. The Waterfall
Model reduces this risk by ensuring that each phase is
thoroughly reviewed and verified before the next one begins.

Key risks in a Banking System and their impact:

  - Data migration failure  -> Customer accounts corrupted
  - Integration failure     -> ATMs and UPI payments stop
  - Security gap            -> Financial fraud or data breach
  - Server overload         -> System crashes under real traffic
  - Rollback needed         -> Old system must be kept as backup

Bugs are caught early in the testing phase rather than after
deployment, which is far cheaper and safer to fix.

----------------------------------------------------------------
3.3 COMPLEXITY
----------------------------------------------------------------

A Banking System is highly complex, involving many
interconnected modules:

  - Frontend (UI/UX for customers)
  - Backend (business logic and transaction processing)
  - Database (accounts, users, transactions, loans)
  - Third-party integrations (ATM networks, payment gateways,
    government databases like Aadhaar and PAN)

Managing all of this in one go would be overwhelming. The
Waterfall Model handles this complexity by breaking it into
well-defined phases, allowing teams to focus on one phase
at a time without confusion or overlap.

----------------------------------------------------------------
3.4 USER INVOLVEMENT
----------------------------------------------------------------

In a Banking System, the client (bank management) provides
all requirements at the beginning. After that, they are not
expected to be involved during development, which is exactly
how Waterfall works.

Stakeholders involved in the Requirements phase:

  - Bank management       : Define business goals
  - Bank employees        : Explain day-to-day operations
  - IT/Technical team     : Assess technical feasibility
  - Legal/Compliance team : Ensure regulations are included
  - System analysts       : Document all requirements
  - End users/Customers   : Provide usability input

The client reviews the final product at the end, which suits
a formal banking environment where continuous client
interaction during development is not practical.

----------------------------------------------------------------
3.5 FLEXIBILITY
----------------------------------------------------------------

A Banking System does NOT need to be flexible. In fact, too
much flexibility is dangerous in banking software. The
Waterfall Model's low flexibility is actually an advantage
here because it:

  - Enforces strict control over the development process
  - Ensures every feature is planned well in advance
  - Prevents scope creep that could introduce security risks
  - Maintains thorough documentation at every stage

Summary of justification factors:

  Factor               | Rating | Reason
  ---------------------|--------|--------------------------------
  Requirement Stability| HIGH   | Fixed by law and regulation
  Risk Level           | LOW    | Each phase fully verified
  Complexity           | HIGH   | Managed phase by phase
  User Involvement     | LOW    | Only at start and end
  Flexibility          | LOW    | Advantage in regulated systems


================================================================
4. COMPARISON WITH OTHER MODELS
================================================================

----------------------------------------------------------------
WHY NOT AGILE?
----------------------------------------------------------------

The Agile Model works in short sprints with frequent
deliveries and constant client involvement. While this works
well for startups and web apps, it is unsuitable for a
Banking System because:

  - Agile allows frequent requirement changes, which is
    dangerous in a regulated banking environment
  - Agile lacks thorough documentation, but banking systems
    require complete audit trails
  - Partial deliveries (deploying accounts module without
    transactions) are unacceptable in banking
  - Security audits cannot be done properly sprint-by-sprint

----------------------------------------------------------------
WHY NOT SPIRAL?
----------------------------------------------------------------

The Spiral Model is designed for high-risk, research-oriented
projects with repeated cycles of planning and risk analysis.
It is unsuitable for a Banking System because:

  - Banking requirements are already well-understood, so
    repeated risk analysis cycles are unnecessary
  - The Spiral Model adds overhead and cost for a project
    with stable and well-defined requirements
  - It is typically used for large government or defense
    projects, not commercial banking software

----------------------------------------------------------------
COMPARISON TABLE
----------------------------------------------------------------

  Criterion           | Waterfall  | Agile      | Spiral
  --------------------|------------|------------|------------
  Requirement change  | Not allowed| Frequent   | Allowed
  Documentation       | Very thorough| Minimal  | Moderate
  User feedback       | Start/end  | Every sprint| Every cycle
  Security focus      | Full test  | Distributed| Risk-driven
  Suitable for banking| YES        | NO         | NO
  Partial delivery    | Not done   | Common     | Per cycle


================================================================
5. DIAGRAM OF THE WATERFALL MODEL
================================================================

The following diagram shows the sequential flow of the
Waterfall Model as applied to the Banking System:

  +----------------------------------------------------------+
  |   PHASE 1: REQUIREMENTS ANALYSIS                         |
  |   Gather banking rules, regulations, user needs          |
  +----------------------------------------------------------+
                          |
                          v  (approved and frozen)
  +----------------------------------------------------------+
  |   PHASE 2: SYSTEM DESIGN                                 |
  |   Architecture, DB schema, security design               |
  +----------------------------------------------------------+
                          |
                          v  (design signed off)
  +----------------------------------------------------------+
  |   PHASE 3: IMPLEMENTATION                                |
  |   Coding: accounts, loans, transactions                  |
  +----------------------------------------------------------+
                          |
                          v  (code complete)
  +----------------------------------------------------------+
  |   PHASE 4: TESTING                                       |
  |   Security audits, load tests, UAT                       |
  +----------------------------------------------------------+
                          |
                          v  (all tests passed)
  +----------------------------------------------------------+
  |   PHASE 5: DEPLOYMENT                                    |
  |   Full rollout to all bank branches                      |
  +----------------------------------------------------------+
                          |
                          v  (system live)
  +----------------------------------------------------------+
  |   PHASE 6: MAINTENANCE                                   |
  |   Bug fixes, compliance updates, security patches        |
  +----------------------------------------------------------+

Deployment involves:
  - Environment setup (servers, firewalls, load balancers)
  - Data migration from old system to new system
  - System integration (ATMs, UPI, NEFT, RTGS, Aadhaar)
  - Staff training for bank employees
  - Pilot rollout (1-2 branches first, then full rollout)
  - Go-live monitoring (24/7 operations team)

NOTE: Each phase must be fully completed before the next
begins. No going back. Sequential, top-down flow only.


================================================================
6. CONCLUSION
================================================================

After carefully analyzing all the important factors:

  - Requirement stability
  - Risk level
  - Complexity
  - User involvement
  - Flexibility

It is clear that the Waterfall Model is the most suitable
SDLC model for developing a Banking System.

The Banking System requires a structured, disciplined, and
thoroughly documented development process. It cannot afford
mid-project changes, partial deliveries, or undocumented
decisions. The Waterfall Model addresses all of these needs
perfectly by enforcing a strict sequential process where
each phase is verified before the next begins.

Other models like Agile and Spiral were considered but found
unsuitable due to their flexibility, lack of documentation
discipline, and iterative delivery approach, all of which
are inappropriate for a safety-critical, regulation-bound
banking environment.

Therefore, it can be confidently concluded that the
Waterfall Model is the best and most appropriate SDLC model
for a Banking System.

================================================================
                      End of Assignment
================================================================
