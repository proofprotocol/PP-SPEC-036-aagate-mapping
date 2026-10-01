# PP-SPEC-036: Proof of Efficacy Mapping to AAGATE

**Status:** DRAFT v0.1  
**Author:** Craig Ellrod / Nebulonium, Inc. / HACKERverse®  
**License:** CC BY 4.0

**Normative specification:** [`PP-SPEC-036-AAGATE-Mapping.md`](./PP-SPEC-036-AAGATE-Mapping.md)

## Purpose

This repository defines a Proof Protocol mapping between AAGATE and Proof Protocol evidence, efficacy, and proof semantics.

AAGATE is treated as a pluggable source of agentic-AI threat and testing context. Proof Protocol remains framework-agnostic and independently determines whether a selected control performed as claimed.

## Repository contents

- `PP-SPEC-036-AAGATE-Mapping.md` — normative mapping specification
- `README.md` — repository overview
- `LICENSE` — license for original Proof Protocol material
- `CONTRIBUTING.md` — contribution guidance
- `CITATION.cff` — citation metadata

## Architectural principle

> **Threat frameworks are pluggable inputs to Proof Protocol. Proof Protocol is framework-agnostic.**

External frameworks describe what may be tested. Proof Protocol independently establishes whether a control worked and what evidence proves the result.

## Ownership and external-framework notice

The mapping, analysis, structure, terminology, and Proof Protocol extensions in this repository are original Proof Protocol material unless otherwise noted.

AAGATE names, identifiers, source materials, and other upstream intellectual property remain with their respective owners. Mapping establishes interoperability, not dependency, endorsement, or transfer of ownership.
