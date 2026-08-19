# Day 3 — AI Customer-Support Assistant

## Problem

Design a production-grade AI customer-support assistant that answers from
approved knowledge, accesses live customer state safely, performs only
authorized actions, preserves conversational context, and transfers ownership
to a human when automated resolution is not justified.

## System design

- [AI Customer-Support Assistant System Design](./ai-customer-support-assistant/ai-customer-support-assistant-system-design.pdf)

## Topics covered

- Support-task decomposition and risk-based routing
- Knowledge ingestion, chunking, hybrid retrieval, and reranking
- Evidence-grounded generation and citation validation
- Typed tool calling, authorization, confirmation, and idempotency
- Conversation memory and state management
- Confidence, clarification, abstention, and human handoff
- Training data, labels, models, losses, and calibration
- Offline, trace-level, online, and business evaluation
- Scalability, latency, cost, reliability, security, and observability

## Key takeaway

The model may propose an answer or action, but deterministic services must own
identity, authorization, policy decisions, state changes, and execution. A
well-structured human handoff is a successful outcome whenever the available
evidence or authority is insufficient.
