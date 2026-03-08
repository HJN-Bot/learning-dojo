# 04 — Publish (1-page reusable note) | RAG for CER Literature Review

## 3 core points
1) RAG is an **evidence selection system** (chunking + retrieval + reranking) more than an LLM trick.
2) For Literature Review, the key product is **structured outputs with citations** (chunk IDs + quotes).
3) Portability from Dify → local scripts requires recording: **chunking config, embedding model, retrieval strategy, and output schema**.

## 1 analogy
RAG = “open-book exam”: the model can only answer well if you hand it the right pages.

## 1 worked example (CER LR)
Input: a folder of papers → Output: a table of 10 claims, each with (evidence quote + source).

## 1 pitfall
“Citations” that are just file names/URLs without exact quoted evidence are not reliable.

## Next 3 actions (<=30min each)
1) Decide LR output schema v0 (fields + example JSON) and lock it.
2) In Dify, configure chunking (size/overlap) and run 3 queries; save results.
3) Write a local script plan: ingestion → embeddings → retrieval → structured output (no UI).
