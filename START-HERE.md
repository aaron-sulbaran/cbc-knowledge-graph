# The build prompt

Copy everything inside the box below and paste it into Claude.

- **Claude Code or Claude Desktop (Cowork / Code tab):** open an empty folder first, then paste. Claude builds the whole thing on your computer.
- **claude.ai in the browser:** make a new Project, paste this into the Project instructions, then upload your notes as files. Claude keeps the wiki for you in chat and gives you each page to save.

Already downloaded this repo? Skip the prompt. Open the folder in Claude, drop something into `inbox/`, and say "sort my inbox".

```text
Set up a personal knowledge graph (a second brain) in this folder, based on Andrej Karpathy's LLM wiki pattern. You are its maintainer: I drop things in, you file, link and keep it tidy.

Create this structure:
- inbox/      where I drop anything (notes, links, PDFs, transcripts). Add a README.md saying "Drop anything here, then tell Claude: sort my inbox."
- raw/        sorted originals. You move files here from the inbox and never edit them again.
- wiki/       pages you write, kept flat (no subfolders). One page per person, project, idea, or event.
- wiki/index.md   a catalog with one line per page: "- [[page-name]]: one-line hook"
- wiki/log.md     a history with one line per action: "- YYYY-MM-DD | action | what happened"
- CLAUDE.md   these rules, so every future session follows them.

Rules:
1. Never edit files in raw/.
2. Check wiki/index.md and update an existing page before creating a new one.
3. Every new page gets an index line; every action gets a log line.
4. Pages have frontmatter (type, updated, sources), a 2 to 3 sentence summary, Notes with a source cited for each fact, and a Related section of [[links]].
5. Link generously with [[page-name]] so the notes form a graph. File names are lowercase-with-dashes.

Workflows (save each as .claude/skills/<name>/SKILL.md if you can, and list them in CLAUDE.md):
- sort: move every inbox item to raw/ as YYYY-MM-DD-short-name, then ingest each one.
- ingest: read one raw file, write a short source summary page, create or update 3 to 8 linked pages, update the index and log, and flag contradictions instead of overwriting.
- search: answer my question by reading the index first, then only the pages you need, citing each claim; say plainly when the wiki does not know; offer to save good answers as new pages.
- tidy: fix broken links, orphan pages, duplicates and missing index lines; list conflicts for me; never touch raw/.

When the structure exists, tell me in three lines what you built, then ask me for the first thing to drop in the inbox.
```

## What to try first

1. Drop a set of lecture notes, an article, or a voice memo transcript into `inbox/`.
2. Say: **sort my inbox**
3. Ask: **what do I know about [topic]?**
4. Open the folder in Obsidian (free) and press the graph button. Those dots and lines are your knowledge graph.
