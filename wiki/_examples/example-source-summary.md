# Karpathy Tweet - LLM Knowledge Bases

**Source:** raw/karpathy-llm-knowledge-bases-tweet.md
**Type:** Social media post
**Posted:** 2026-04-03
**Author:** Andrej Karpathy
**URL:** https://x.com/karpathy/status/2039805659525644595

A Twitter/X post where Karpathy describes his personal workflow for using LLMs to build and maintain persistent knowledge bases. The post triggered significant discussion and several follow-up implementations in the community.

## Summary

Karpathy explains that a large fraction of his recent LLM token usage has shifted from writing code to organizing knowledge. He indexes source documents into a `raw/` directory, then uses an LLM to incrementally compile a wiki of markdown files containing summaries, backlinks, and categorized concept articles. Obsidian serves as the read-only IDE while the LLM handles all writing. At approximately 100 articles and 400,000 words, he found that traditional RAG infrastructure was unnecessary because the LLM auto-maintains index files and brief summaries that allow targeted file reads at small scale.

He also describes four operations (ingest, query, lint, and output) and mentions vibe-coding small CLI tools on top of the wiki such as a naive search engine. He closes by suggesting there is room for a real product in this space rather than a collection of scripts.

## Key Takeaways

- LLM knowledge bases are a practical alternative to vector RAG for personal research at sub-500-article scale.
- Obsidian acts as the IDE frontend. The LLM writes and maintains the wiki. The human rarely edits wiki files directly.
- Four operations cover the full lifecycle: ingest (compile raw sources into wiki pages), query (3 to 4 targeted file reads), lint (periodic health checks), and output (rendering results back as wiki articles).
- At 100 articles and 400K words the pattern still runs smoothly without embeddings or a vector database.
- Output artifacts like slide decks or comparison tables can be filed back into the wiki as new pages so explorations compound.
- Karpathy built small CLI tools on top of the wiki including a search engine for larger-scale queries.

## Notable quotes

The LLM has been pretty good about auto-maintaining index files and brief summaries of all the documents and it reads all the important related data fairly easily at this small scale.

I think there is room here for an incredible new product instead of a hacky collection of scripts.

## Related

- [[entities/andrej-karpathy|Andrej Karpathy]]
- [[llm-wiki-pattern/_index|LLM Wiki Pattern]]
- [[llm-wiki-pattern/ingest-operation|Ingest Operation]]
- [[llm-wiki-pattern/query-operation|Query Operation]]
- [[llm-wiki-pattern/lint-operation|Lint Operation]]
- [[concepts/compounding-knowledge-base|Compounding Knowledge Base]]

## Open Questions

- Which specific search engine tool does Karpathy use on top of the wiki at larger scale?
- How does he handle contradictions between newer and older sources in practice?
- What does his `CLAUDE.md` schema file actually contain?
