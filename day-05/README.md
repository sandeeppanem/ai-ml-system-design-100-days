# Day 5 — LLM Evaluation Pipeline

## Problem

Design a production-grade evaluation pipeline that measures complete LLM
applications and their individual components, produces trustworthy evidence
for release decisions, and continuously turns production failures into
targeted regression coverage.

## System design

- [LLM Evaluation Pipeline System Design](./llm-evaluation-pipeline/llm-evaluation-pipeline-ml-system-design.pdf)

## Topics covered

- Evaluation formulation by application type and business outcome
- Base-model, component, application, trajectory, and product evaluation
- Versioned datasets, labels, slices, lineage, and contamination controls
- Deterministic checks, functional graders, learned evaluators, and LLM judges
- Human evaluation, grader calibration, disagreement, and adjudication
- RAG, agent, tool-use, memory, safety, and fallback evaluation
- Model, business, system, and safety metric families
- Statistical comparison, non-inferiority, confidence, and release decisions
- Distributed offline evaluation and continuous production monitoring
- Release gates, staged autonomy, scalability, cost, reliability, and security

## Key takeaway

Evaluation is a production feedback and release-control system, not a single
score or benchmark. Trustworthy decisions require explicit outcomes and harms,
representative datasets, calibrated graders, complete-system traces, hard
safety gates, and evidence that offline improvements translate into production
value.
