# 00 — Intake | RAG for CER Literature Review

## Topic
Understand **RAG mechanisms** and map them to **CER / Literature Review** input→output requirements; then run a small RAG flow in **Dify**, and evaluate whether the outputs can transfer to a **local script pipeline**.

## Why (problem to solve)
- CER / Literature Review needs repeatable: **retrieve → cite → summarize → structured output**.
- We need to know which pieces are “platform features” vs “portable design” so we can later implement locally.

## Baseline (current)
- You already know the high-level pipeline idea, but want clarity on:
  - how retrieval works (embedding / chunking / ranking)
  - how to verify quality (citations, recall/precision)
  - what Dify can export/replicate locally

## Today acceptance criteria (DoD)
- Explain RAG in 1 minute (with the 4 canonical steps)
- Build 1 Dify RAG workflow and test with 3 queries
- Produce a small “portability report”: what can be replicated locally (data + prompts + evaluation)

## Constraints
- Timebox: 60–90 minutes total
- Prefer minimal moving parts: 1 corpus, 1 index, 1 prompt template
