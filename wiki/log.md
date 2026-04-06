# Operation Log

Append-only record of every operation performed on this wiki. The LLM writes one line per operation. The human reads it to understand what happened when.

## Format

```
## [YYYY-MM-DD HH:MM] operation | short description | files touched
```

Valid operations: `ingest`, `query`, `lint`, `fix`, `file-back`, `restructure`.

## How to query the log

```bash
grep "^## \[" log.md | tail -20     # last 20 operations
grep "ingest" log.md                 # all ingests
grep "2026-04" log.md                # all operations from April 2026
```

## Entries

*Empty. The LLM will append entries here during every operation.*
