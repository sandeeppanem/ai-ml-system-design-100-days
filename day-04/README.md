# Day 4 — Production-Grade RAG Pipeline

## Problem

Design a production-grade retrieval-augmented generation pipeline that returns
useful answers only when current, authorized evidence supports them, while
meeting quality, freshness, security, latency, scalability, and cost
requirements.

## System design

- [Production-Grade RAG Pipeline System Design](./rag-pipeline/rag-pipeline-ml-system-design.pdf)

## Topics covered

- Choosing RAG versus fine-tuning, long-context prompting, APIs, and graphs
- Offline ingestion, canonical document contracts, lineage, and versioning
- Structure-aware chunking and specialized content representations
- Embeddings, hard-negative training data, and ranking losses
- Vector-store selection, ANN indexes, filters, and tenancy
- Query rewriting, dense and lexical retrieval, fusion, and reranking
- Prompt assembly, grounded generation, citations, and claim validation
- Retrieval and answer-quality evaluation, calibration, and abstention
- Conversational memory, caching, security, and data governance
- Online serving, scalability, latency, TTFT, cost, and graceful degradation

## Key takeaway

RAG is an evidence system before it is a generation system. Retrieval should
maximize recall, reranking and evidence assembly should improve precision and
sufficiency, and generation should explain only the evidence that deterministic
authorization and freshness controls permit the user to see.
