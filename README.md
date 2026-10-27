# CBC Knowledge Graph: build your second brain with Claude

A starter knowledge graph from Texas Claude Builder Club. Think of it as a second brain: you drop things in; Claude sorts them, writes linked notes, and answers questions from them. Open it in Obsidian and the links become a knowledge graph you can see.

It follows Andrej Karpathy's [LLM wiki pattern](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f): you curate, the AI does the bookkeeping.

Using an AI agent to set this up for you? Point it at [AGENTS.md](AGENTS.md).

---

## Step by step (about 10 minutes)

Pick the path that matches what you have. Path A is the full experience.

### Path A: Claude Code or Claude Desktop (recommended)

**1. Get the files.** Choose one:

- **With a GitHub account (best, gives you your own private copy):** at the top of this page click **Use this template**, then **Create a new repository**. Name it, set it to **Private**, click **Create repository**. Then on your new repo click the green **Code** button and **Download ZIP** (or `git clone` it if you use git).
- **Without a GitHub account:** click the green **Code** button, then **Download ZIP**.

Unzip it. **Mac:** double-click the ZIP. **Windows:** right-click the ZIP, choose **Extract All** (do not work inside the ZIP preview).

**2. Open the folder in Claude.**

- **Claude Desktop:** open the app, go to the **Code** tab (or **Cowork**), and choose the folder you just unzipped.
- **Terminal:** `cd` into the folder and run `claude`.

**3. Sort the sample note.** There is already one note in `inbox/`. Type:

> sort my inbox

Claude moves the note to `raw/`, writes linked pages in `wiki/`, and updates `wiki/index.md` and `wiki/log.md`. Allow file edits when it asks.

**4. Ask it something.** Type:

> what do I know about Texas Claude Builder Club?

It answers from your wiki and cites the pages it used.

**5. See the graph.** Install [Obsidian](https://obsidian.md) (free). Choose **Open folder as vault** and pick the same folder. Press **Cmd+G** (Mac) or **Ctrl+G** (Windows) for graph view. Each dot is a page; each line is a link.

**6. Make it yours.** Drop your own lecture notes, articles, PDFs or transcripts into `inbox/` and say **sort my inbox** again.

### Path B: claude.ai in the browser only

1. Open [START-HERE.md](START-HERE.md) and copy the prompt in the box.
2. On claude.ai, create a new **Project**. Paste the prompt into the Project **instructions**.
3. Upload a few notes or PDFs to the Project, then say **sort these into my wiki**.
4. Claude replies with the pages as markdown. Save them as `.md` files in a folder on your computer if you want the graph in Obsidian.

This works on any plan, but Claude cannot write files for you, so Path A is better once you have it.

### Path C: build it from scratch with the prompt

1. Make an empty folder and open it in Claude Code or Claude Desktop.
2. Paste the prompt from [START-HERE.md](START-HERE.md).
3. Claude creates the folders and rules. Continue from Path A, step 3.

---

## Everyday use

| You say | Claude does |
|---|---|
| "sort my inbox" | moves everything from `inbox/` into `raw/`, writes and links wiki pages |
| "ingest raw/some-file.md" | turns one source into linked pages |
| "what do I know about X?" | answers from your wiki, citing pages |
| "tidy up" | fixes broken links, orphan pages, duplicates |

The rules live in [CLAUDE.md](CLAUDE.md). The four workflows live in `.claude/skills/` (sort-inbox, ingest, search, tidy).

## Folders

```
inbox/   drop anything here, no sorting needed
raw/     sorted originals (Claude never edits them)
wiki/    Claude's linked pages, plus index.md (the map) and log.md (the history)
```

## Why bother

- **Personal:** class notes and readings that link themselves together, searchable by asking.
- **Long projects:** the repo remembers decisions, so Claude never starts from zero.
- **Teams and hackathons:** one shared repo everyone's Claude reads and writes. See the team rules in [AGENTS.md](AGENTS.md).

## Troubleshooting

- **Claude does not seem to know the workflows:** say "read CLAUDE.md and follow the sort workflow".
- **Graph view is empty or has one dot:** run "sort my inbox" first; the links appear after pages exist.
- **Windows cannot open the folder in Claude:** you are probably inside the ZIP preview. Right-click the ZIP, Extract All, and open the extracted folder.
- **Want it private on GitHub:** use **Use this template** and choose Private. A Fork of a public repo cannot be private.

Keep Thinking.
