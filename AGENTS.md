# For AI agents

You are setting up or maintaining a knowledge graph (the owner's second brain) for a person who may not code. CLAUDE.md holds the rules; follow it exactly. This file tells you how to get started.

## If the person asks you to set this up

1. Check the folder. You should see `inbox/`, `raw/`, `wiki/index.md`, `wiki/log.md`, `CLAUDE.md`, and `.claude/skills/` with `sort-inbox`, `ingest`, `search`, `tidy`.
2. If anything is missing, create it exactly as described in the prompt inside `START-HERE.md`. Do not invent extra folders.
3. Read `CLAUDE.md` in full before touching any file.
4. If `inbox/` has items other than `README.md`, run the sort workflow (`.claude/skills/sort-inbox/SKILL.md`), which ingests each item.
5. Report in plain language, in five lines or fewer: what you set up, which pages you created, and the next thing they can try ("drop a lecture into inbox/ and say sort my inbox", or "ask: what do I know about X?").
6. Tell them how to see the graph: open the folder in Obsidian with "Open folder as vault", then press Cmd+G or Ctrl+G.

## If you cannot load skills

Read the matching `.claude/skills/<name>/SKILL.md` file and follow its numbered steps by hand.

## Shared repos (teams, hackathons)

- Pull before you start and commit after each workflow, one commit per ingest, with a message like `ingest: raw/2026-10-27-kickoff-notes.md`.
- Each person drops files in their own `inbox/<name>/` folder so two people never sort the same item.
- Before rewriting a page someone else wrote, add your facts under `## Notes` instead of replacing theirs.
- Keep `wiki/index.md` and `wiki/log.md` append-only; if a merge conflict appears in them, keep both sides.
