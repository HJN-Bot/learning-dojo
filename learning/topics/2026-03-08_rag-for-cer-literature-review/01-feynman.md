# 01 — Feynman Explain | RAG for CER Literature Review

## Kid version (<=120 words)
RAG is like doing homework with a smart librarian. Before the AI answers, it first **looks up** the best pages from your documents, then it **uses those pages** to write the answer. That makes answers more grounded and less made-up.

## Engineer version (<=200 words)
RAG = **Retrieve-Augment-Generate**. A typical pipeline:
1) **Ingest**: split docs into chunks; compute embeddings; store in a vector DB + metadata.
2) **Retrieve**: for a query, embed it; do vector similarity search; optionally hybrid (BM25+vector); re-rank.
3) **Augment**: assemble a context window from top-k chunks with citations/IDs.
4) **Generate**: LLM produces output constrained by the retrieved context; optionally structured JSON.

For Literature Review, RAG’s job is not “write everything” but “select evidence with citations” → then synthesize.

## Boundaries / counterexamples (<=200 words)
- RAG fails when **chunking is wrong** (too big/too small), or when retrieval returns irrelevant chunks.
- Citations can be misleading if you don’t enforce “quote the source text” or store stable chunk IDs.
- If your task needs deep reasoning across many documents, RAG may need: query decomposition, multi-hop retrieval, or iterative refinement.
- Some “Dify good results” may come from hidden platform defaults (chunkers, rerankers). If you don’t record configs, transfer to local scripts will degrade.
