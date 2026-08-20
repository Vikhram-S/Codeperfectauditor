# CodePerfect Auditor — Project Documentation

> **AI Engineering Intern (Agentic AI Track)** · Jatayu Hackathon 2026 · Virtusa Consulting Services Pvt Ltd
> Team **Hightower** · March – May 2026

---

## ⚠️ About this repository

This repository documents a project built during a **client-affiliated hackathon internship** at Virtusa Consulting Services Pvt Ltd. The source code is proprietary to Virtusa and is **not included here**.

This repo instead contains:
- The problem statement and system design as proposed and built by our team
- A description of my individual technical contributions
- Architecture diagrams (recreated, not copied from internal decks)
- The evaluation approach and outcomes

If you're reviewing this as part of an application or interview, I'm happy to walk through the design decisions, trade-offs, and my specific role in the system directly.

---

## Project Summary

**CodePerfect Auditor** is an agentic AI system for healthcare revenue-integrity auditing. It reconciles clinical documentation against billed ICD-10/CPT codes and surfaces coding discrepancies through a traceable, evidence-linked audit trail — turning a reactive, manual coding-audit process into a pre-submission, explainable validation step.

Built for the Virtusa Jatayu Hackathon 2026 (Agentic AI track), the submission was selected as one of two teams from our college to advance in the competition.

| | |
|---|---|
| **Team name** | Hightower |
| **Team members** | Vikhram S, Gowtham P G, Rekha S, Sivanandhi N |
| **Timeline** | Hackathon build: within a fixed competitive window, Mar–May 2026 |
| **Track** | Agentic AI |
| **Domain** | Healthcare Revenue Cycle Management (RCM) |

See [`docs/ARCHITECTURE.md`](docs/ARCHITECTURE.md) for the system design and [`docs/MY_CONTRIBUTION.md`](docs/MY_CONTRIBUTION.md) for what I personally built.

---

## Problem Statement

Hospitals lose significant revenue due to inaccurate medical coding, missed comorbidities, and compliance risk from accidental upcoding. Manual coding audits are slow, error-prone, and reactive — they catch problems *after* claims are submitted, not before.

**Goal:** an agentic AI auditor that autonomously validates and corrects ICD-10 & CPT codes *before* claim submission, with every flagged discrepancy backed by an exact citation to the source clinical note.

## System Overview

The system is composed of three cooperating agents:

1. **Clinical Reader Agent** — extracts diagnoses and procedures from surgical/clinical notes (NLP-based ingestion)
2. **Coding Logic Agent** — generates ICD-10 and CPT codes from the extracted clinical entities
3. **Auditor Agent** — compares AI-generated codes against human-entered codes, flags discrepancies, and links each flag to the exact sentence in the clinical record that justifies it

This produces an **explainable audit trail**: every discrepancy is traceable to specific evidence, rather than a black-box flag.

Full diagram: [`docs/ARCHITECTURE.md`](docs/ARCHITECTURE.md)

## Outcome

- Selected as 1 of 2 teams from our college to represent in the Jatayu Hackathon 2026 Agentic AI track
- Delivered a working demo (FastAPI backend, Streamlit interface) within the hackathon timeline
- Internship formalized as a remote AI Engineering Intern role with weekly SME review sessions

## Links

- Service/experience certificate available on request
- [Vikhram S — profile](https://vikhram-s.github.io/)
