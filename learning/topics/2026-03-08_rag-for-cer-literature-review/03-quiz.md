# 03 — Knowledge Check | RAG for CER Literature Review

## MCQ (3)
1) Which step most directly controls *what evidence enters the prompt*?
   A. Generation prompt  B. Retrieval top-k  C. Temperature  D. Streaming

2) If your RAG answers are irrelevant, the *first* thing to inspect is:
   A. LLM model size  B. Chunking + retrieval results  C. UI styling  D. GPU drivers

3) “Good citations” means:
   A. The answer includes any URL
   B. The answer includes stable chunk IDs + quoted supporting text
   C. The answer sounds confident
   D. The answer is short

## Short answer (2)
1) In 5–7 lines, describe the minimal RAG pipeline you will implement in Dify for LR.
2) What are 2 portability risks when moving from Dify → local scripts?

## Practice (<=20min)
### Task
Run a tiny RAG in **Dify** and produce a portability checklist.

### Steps
- Create a knowledge base with 1–3 PDFs (or a small markdown corpus).
- Ask 3 queries:
  1) “Give me 3 bullets summary with citations.”
  2) “List 5 key terms and cite where they appear.”
  3) “Extract a structured JSON: {claim, evidence_quote, source_id}×3.”

### Output
- Screenshot or copy-paste of 3 answers + citations
- A 10-line portability checklist

### Done definition
- You can point to retrieved evidence, not just model output.
