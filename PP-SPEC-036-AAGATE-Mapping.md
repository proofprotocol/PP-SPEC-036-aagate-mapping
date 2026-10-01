# PP-SPEC-036: Proof of Efficacy Mapping to AAGATE

| Field | Value |
|---|---|
| Status | DRAFT v0.1 |
| Author | Craig Ellrod, Nebulonium, Inc. (dba HACKERverse®) |
| Date | October 1, 2026 |
| License | CC BY 4.0 |
| Maps to | AAGATE |
| Series | Proof Protocol Framework Mapping Specifications |

---

## 1. Purpose

This specification defines how AAGATE threat, attack, test, or control context can be bound to Proof Protocol evidence and efficacy results.

The external framework remains authoritative for its own terminology, identifiers, requirements, and architecture. This document defines a **Proof Protocol mapping** and does not supersede or modify AAGATE.

## 2. Scope

AAGATE supplies structured agentic-AI security context that can identify what should be exercised or evaluated. Proof Protocol supplies the independent evidence model used to determine what happened and whether a selected control performed as claimed.

Independent witnessing and evidence-capture implementation are defined elsewhere in the Proof Protocol specification family.

## 3. Core Question

Proof of efficacy asks:

> **Was there a control, and did it work?**

A control's existence, configuration, activation, and efficacy are separate facts. An upstream framework can identify a threat or expected safeguard without itself establishing the efficacy of a deployed control.

## 4. Metric Definitions

For a defined adversarial corpus, Proof Protocol records each test outcome as **blocked**, **detected**, **missed**, or **INVALID**.

Relevant metrics include:

- containment rate;
- detection rate;
- miss rate;
- false-positive rate against paired benign cases;
- robustness against bypass, suppression, manipulation, or evasion;
- version-level results; and
- INVALID status when required evidence is incomplete or broken.

Target thresholds are engagement- and risk-specific and are not imposed by this mapping.

## 5. Evidence Produced

A mapped evaluation can produce:

- **Proof records** binding test case, control, system/version, verdict, timestamp, and evidence references;
- **ProofStamp™** trusted timestamps bound to evidence/verdict objects;
- **ProofBundle™** packages containing proof records, metrics, corpus manifests, and environment context;
- **ProofRegister™** records for issued proof artifacts; and
- corpus and environment manifests sufficient to identify the tested conditions.

## 6. Mapping to AAGATE

AAGATE concepts are inputs to the test-definition layer rather than dependencies of the Proof Protocol evidence architecture.

| AAGATE input | Proof Protocol treatment | Resulting evidence |
|---|---|---|
| Threat or attack definition | Bind the identified condition to one or more reproducible test cases. | Corpus manifest; proof record |
| Attack sequence or scenario | Execute the relevant sequence against the system/control under test. | Execution evidence; verdict |
| Expected control or mitigation | Record the control claim separately from observed behavior. | Control descriptor; proof record |
| Detection expectation | Measure whether the tested condition was identified. | Detection result |
| Prevention/containment expectation | Measure whether the tested condition reached the protected target or objective. | Containment result; target evidence |
| Bypass/evasion condition | Exercise adversarial variants designed to defeat the control. | Robustness evidence |
| Agent/system context | Bind system, model, policy, identity, tools, dependencies, and version where material. | Environment descriptor |
| Outcome condition | Obtain downstream target, SIEM, vendor, application, or equivalent evidence when necessary to establish efficacy. | Outcome evidence |

## 7. Interoperability Rules

1. The AAGATE identifier/version and relevant mapped element SHOULD be recorded when available.
2. AAGATE terminology and identifiers MUST NOT be silently redefined by this specification.
3. A control firing does not by itself prove that the protected target was protected.
4. Where efficacy depends on a downstream outcome, target-side or equivalent evidence SHOULD complete the evidence round trip.
5. Missing required evidence MUST yield **INVALID**, not PASS.
6. Material changes to the tested system, model, control, policy, identity, environment, or corpus SHOULD trigger versioned retesting where they can affect the result.

## 8. Framework-Agnostic Architecture

> **Threat frameworks are pluggable inputs to Proof Protocol. Proof Protocol is framework-agnostic.**

External frameworks can identify **what to test**: threats, vulnerabilities, controls, design assertions, identity claims, or risk conditions. Proof Protocol independently establishes **whether the control worked and what evidence proves that result**.

No external framework is required for Proof Protocol to operate. A Proof Protocol implementation MAY use AAGATE, MAESTRO, MITRE ATLAS, OWASP, AIVSS, a proprietary threat model, another recognized framework, or no external framework at all when the test condition is otherwise sufficiently defined.

Adding, replacing, muting, or removing a framework mapping does not alter the Proof Protocol architecture, evidence model, Proof of Efficacy determination, ProofBundle™, ProofStamp™, ProofRegister™, or independent corroboration requirements.

A framework mapping therefore establishes **interoperability**, not architectural dependency.

## 9. Relationship to Proof Protocol

This mapping is part of the Proof Protocol specification family maintained by Nebulonium, Inc.

The relationship is intentionally asymmetric:

> **AAGATE supplies threat and test context. Proof Protocol supplies the evidence model for determining whether a selected control performed as claimed.**

No affiliation, endorsement, certification, or sponsorship by AAGATE's maintainers is implied.

## 10. Source Framework, Attribution, and License

AAGATE is an external framework/project. Its source materials retain their original ownership and licensing. The AAGATE code/materials identified for this mapping are distributed under the **MIT License** where that upstream license applies.

This Proof Protocol mapping is independently authored and licensed under **CC BY 4.0**. It references upstream concepts for interoperability and does not relicense AAGATE material.

Framework names and trademarks remain the property of their respective owners.

## 11. Versioning

This mapping is versioned independently of AAGATE. A material upstream change SHOULD result in a mapping review and, where necessary, a new PP-SPEC-036 version identifying the AAGATE version or revision mapped.

---

*Proof Protocol · proofprotocol.io · CC BY 4.0*
