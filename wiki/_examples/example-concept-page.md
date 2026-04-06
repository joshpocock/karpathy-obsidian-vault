# Compounding Knowledge Base

**Source:** raw/karpathy-llm-knowledge-bases-tweet.md, raw/karpathy-gist-llm-wiki.md

The central insight behind the LLM wiki pattern. A knowledge base that grows richer with every source added and every question asked, rather than starting from scratch on each query.

## Why it matters

Standard RAG retrieves relevant chunks from raw documents at query time and synthesizes an answer from them. Nothing is built up. The same subtle question asked twice causes the model to re-derive the answer twice. The knowledge never accumulates outside of the individual chat session.

The compounding pattern is different. Each ingested source is processed once into structured wiki pages with cross-links. Each query can be filed back into the wiki as a new article. The wiki becomes a persistent artifact that gets smarter over time.

## Mechanics

- Sources are read once and compiled into multiple wiki pages during ingest.
- Good queries return answers that can be promoted into the wiki as new articles.
- Cross-links are maintained automatically by the LLM, so related concepts get stronger connections as more sources are added.
- Contradictions found during lint passes get resolved and the resolution is preserved.

## Key Takeaways

- The wiki is a persistent, append-and-refine artifact. Chat sessions are ephemeral.
- Queries are not just retrieval. They are opportunities to synthesize new knowledge and file it back.
- The maintenance burden that kills every human-authored wiki is handled by the LLM at near-zero cost.
- Compounding only works if every ingest and every file-back follows the schema consistently. That is the job of `CLAUDE.md`.

## Related

- [[llm-wiki-pattern/_index|LLM Wiki Pattern]]
- [[llm-wiki-pattern/ingest-operation|Ingest Operation]]
- [[llm-wiki-pattern/query-operation|Query Operation]]
- [[llm-wiki-pattern/file-back|Filing Outputs Back into the Wiki]]
- [[retrieval/vector-rag|Vector RAG]]
- [[entities/andrej-karpathy|Andrej Karpathy]]

## Open Questions

- Does the compounding benefit plateau at a certain wiki size, or does it continue indefinitely?
- What is the right cadence for file-back operations, automatic or human-triggered?
