# Karpathy LLM Wiki - Starter Vault

A ready-to-use Obsidian vault template for the LLM-maintained wiki pattern Andrej Karpathy described. Based on his tweet and gist. Walks with any Claude Code session from day one.

Full walkthrough: [Stride video #0006]

## What you get

- `CLAUDE.md` at the vault root. The schema file that turns Claude Code into a disciplined wiki librarian across every session. Every rule is already written.
- `raw/` for your source material. Drop anything in here: articles, papers, transcripts, screenshots, pasted notes.
- `wiki/` with a starter master index, an empty log file, and three example pages so the model has shape references for its first few ingests.
- `output/` for query results and lint reports.

## 2-minute setup

1. **Download Obsidian** from [obsidian.md](https://obsidian.md) if you do not already have it.
2. **Unzip this template** anywhere on your machine.
3. **Open the folder as a vault.** In Obsidian, click "Open folder as vault" and select the unzipped template folder.
4. **Install Claude Code** if you do not already have it. Instructions at [claude.com/claude-code](https://claude.com/product/claude-code).
5. **Open a terminal inside the vault folder.** On Mac, right-click the folder and choose "New Terminal at Folder". On Windows, open Terminal and `cd` into the path. In VS Code, `File > Open Folder` and use the integrated terminal.
6. **Run `claude`** to start a Claude Code session. It will automatically read `CLAUDE.md`.
7. **Drop your first source** into `raw/`. Any markdown file or article works.
8. **Type `compile`** in the Claude Code session. Watch Obsidian on the other half of your screen. The wiki will populate.

That is it. You now have a working LLM-maintained wiki.

## Recommended Obsidian plugins (optional)

- **Obsidian Web Clipper** - browser extension that converts web articles to markdown in one click. Configure it to drop notes into `raw/`.
- **Local Images Plus** - community plugin that downloads referenced images into the vault so the model can reference them locally.
- **Dataview** - if you want dynamic tables and queries over wiki frontmatter.

## Daily use

Four commands, all typed in Claude Code:

- `compile` - ingest anything new in `raw/` into the wiki.
- Ask a question - the model reads the index files, drills into the right articles, and answers.
- `lint` - health check. The model reports contradictions, gaps, and orphan pages without making changes.
- Fix specific issues - approve fixes from the lint report one at a time.

## When the pattern breaks down

The wiki pattern works well for solo operators and small teams up to about 500 articles. Past that, the index file stops being a reliable navigation layer and you need either multiple topic-specific vaults or a small search tool over the markdown files. You will probably not hit this ceiling for a while.

If the wiki ever feels slow or the model starts missing relevant articles, run `lint` and look for orphan pages and missing cross-links. That is almost always the fix.

## Credit

The pattern is Andrej Karpathy's. This template is Stride's implementation of it with every rule spelled out in `CLAUDE.md` so the model behaves consistently across sessions. Full walkthrough video: [link]

## Support

- Free community: [skool.com/stride-ai-academy-7057](https://www.skool.com/stride-ai-academy-7057)
- Premium academy: [skool.com/stride-ai-automation-academy-9690](https://www.skool.com/stride-ai-automation-academy-9690)
