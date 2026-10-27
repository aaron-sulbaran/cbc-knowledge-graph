# Build your second brain with Claude

A starter knowledge base from Texas Claude Builder Club. You drop things in; Claude sorts them, writes linked notes, and answers questions from them. Open it in Obsidian and the links become a knowledge graph you can see.

It follows Andrej Karpathy's [LLM wiki pattern](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f): you curate, the AI does the bookkeeping.

## Get it (pick one)

1. **Just the prompt:** open [START-HERE.md](START-HERE.md), copy the prompt, paste it into Claude. Works anywhere.
2. **Your own private copy (recommended):** click **Use this template**, then **Create a new repository**, and set it to **Private**. Your notes stay yours. (A fork of a public repo cannot be private, so use the template button, not Fork.)
3. **No GitHub account:** green **Code** button, then **Download ZIP**, then unzip it (Windows: right-click, Extract All).

## Use it

| You say | Claude does |
|---|---|
| "sort my inbox" | moves everything from `inbox/` into `raw/`, writes and links wiki pages |
| "what do I know about X?" | answers from your wiki, citing pages |
| "tidy up" | fixes broken links, orphans, duplicates |

The rules live in [CLAUDE.md](CLAUDE.md). The workflows live in `.claude/skills/`.

## Why bother

- **Personal:** class notes and readings that link themselves together, searchable by asking.
- **Long projects:** the repo remembers decisions, so Claude never starts from zero.
- **Teams and hackathons:** one shared repo everyone's Claude reads and writes. Give each person their own inbox folder to avoid collisions.

## Folders

```
inbox/   drop anything here
raw/     sorted originals (Claude never edits them)
wiki/    Claude's linked pages, plus index.md and log.md
```

Keep Thinking.
