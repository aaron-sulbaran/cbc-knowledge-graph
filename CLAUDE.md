# Second brain rules

You maintain this knowledge base. The human drops things in; you do the filing, linking and bookkeeping. Follow these rules every time.

## Folders

| Folder | What lives there | Who writes |
|---|---|---|
| `inbox/` | Anything the human drops in: notes, links, PDFs, transcripts, screenshots | the human |
| `raw/` | Sorted originals, moved out of the inbox | you move files in, then never edit them |
| `wiki/` | Pages you write: one page per person, project, idea or topic | you |

`wiki/index.md` is the catalog: one line per page. `wiki/log.md` is the history: one line per action.

## The five rules

1. Never edit a file in `raw/`. It is the source of truth. If it is wrong, say so in the wiki page instead.
2. Update an existing page before creating a new one. Search `wiki/index.md` first.
3. Every new page gets a line in `wiki/index.md`. Every action gets a line in `wiki/log.md`.
4. Keep `wiki/` flat: no subfolders. Use the `type:` field to tell pages apart.
5. Link generously with `[[page-name]]` and cite the source file for every fact, like `(raw/2026-10-27-lecture-notes.md)`.

## Page format

```
---
type: person | project | concept | event | source
updated: YYYY-MM-DD
sources: [raw/filename.md]
---

# Page title

Two or three sentences on what this is and why it matters to me.

## Notes
- Facts, each with its source.

## Related
- [[other-page]]
```

File names are lowercase with dashes: `wiki/claude-builder-club.md`.

## Log format

`- YYYY-MM-DD | sort | moved 3 items from inbox` or `- YYYY-MM-DD | ingest | raw/file.md -> 4 pages touched`

## Workflows

Each one has a skill in `.claude/skills/`. If you cannot load skills, read the matching `SKILL.md` and follow it.

- **sort**: empty the inbox into `raw/`, then ingest each item.
- **ingest**: turn one file in `raw/` into wiki pages.
- **search**: answer a question from the wiki, with citations.
- **tidy**: health check for broken links, orphan pages, duplicates and stale facts.

When the human says "sort my inbox", "what do I know about X", or "clean this up", use the matching workflow.
