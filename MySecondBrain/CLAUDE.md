# AI Trends Wiki — Project Specification

## Overview

Personal knowledge base for tracking AI trends and innovations. The system maintains a persistent wiki that synthesizes information from diverse sources — YouTube transcriptions, articles, documents, Telegram channel exports. Knowledge accumulates over time; the wiki grows richer with every ingested source.

**Key principle:** The wiki is a living, compounding artifact. Cross-references are pre-built, contradictions are flagged, synthesis reflects everything processed. The LLM does all maintenance work.

## Architecture

### Three Layers

1. **Raw Sources** (`/raw/`)
   - Immutable collection of source documents
   - YouTube transcriptions, articles, documents, Telegram exports
   - Bilingual: Russian and English
   - Never modified by the LLM

2. **Wiki** (`/wiki/`)
   - LLM-generated markdown files
   - Entity pages, concept pages, summaries, comparisons, trend analysis
   - LLM owns this layer entirely

3. **Schema** (this file)
   - Defines wiki structure, conventions, workflows
   - Evolved collaboratively over time

### Special Files

- **`/wiki/index.md`** — Content catalog: all wiki pages with one-line summaries, organized by category
- **`/wiki/log.md`** — Append-only chronological record of all operations (ingests, queries, lints)

## Source Handling Rules

### Multi-Part Documents

Documents with `_part1` and `_part2` (or `_part3`, etc.) in the filename are **parts of a single source**. They must be:
1. Merged into a single text before processing
2. Treated as one source with one summary page
3. Logged as single ingest entry

### Language Handling

- Primary language of source is preserved in page frontmatter (`lang: ru` or `lang: en`)
- Russian and English sources are cross-referenced when they cover the same topics
- All wiki content is in Russian (user's primary language) with English terms preserved in brackets where appropriate

## Wiki Structure

```
wiki/
├── index.md
├── log.md
├── concepts/          # AI concepts, technologies, methods
│   ├── transformer.md
│   ├── rag.md
│   └── ...
├── entities/         # Companies, products, people
│   ├── anthropic.md
│   ├── openai.md
│   └── ...
├── sources/          # Processed source summaries
│   ├── youtube_transcription_...md
│   ├── article_...md
│   └── telegram_...md
├── trends/           # Trend analysis and comparisons
│   ├── llm_comparison.md
│   ├── multimodal_analysis.md
│   └── ...
└── synthesis/         # High-level overview and thesis
    └── overview.md
```

## Page Format

Each wiki page includes YAML frontmatter:

```yaml
---
title: Title
type: concept | entity | source | trend | synthesis
tags: [tag1, tag2]
lang: en | ru
created: 2026-04-20
sources: [source_file_1.md, source_file_2.md]  # only for synthesized pages
---
```

## Workflows

### Ingest

When you add a new source to `/raw/` and ask to process it:

1. **Detect multi-part** — If filename contains `_partN`, merge all parts into single text
2. **Read and analyze** — Extract key information, identify topics, entities, claims
3. **Create source page** — Write summary in `/wiki/sources/`
4. **Update index** — Add new page to index.md
5. **Update relevant pages** — Add cross-references to existing concept/entity pages
6. **Log entry** — Append to log.md with timestamp and source name

A single source may touch 10-15 wiki pages.

### Query

When you ask a question:

1. Read `index.md` to find relevant pages
2. Read those pages
3. Synthesize answer with citations
4. If answer has lasting value (comparison, analysis, discovery) — save it as a wiki page

### Lint

Periodically ask me to health-check the wiki:

- Contradictions between pages
- Stale claims superseded by new sources
- Orphan pages (no inbound links)
- Missing cross-references
- Data gaps that could be filled with web search

## Source Directories

```
raw/
├── youtube/          # YouTube transcriptions
├── articles/         # Articles and blog posts
├── documents/        # PDFs, reports, papers
└── telegram/         # Telegram channel exports
```

## Conventions

- Page titles: English terms in brackets when Russian title doesn't exist `[Transformer] модель`
- Use `[[page-name]]` for internal wiki links
- All dates in ISO format: 2026-04-20
- Source references: `[source: filename]` at end of claims
- Contradictions: flagged with `> [!warning]` blockquote

## Naming

- Source files: preserve original names, add date prefix if needed for sorting
- Wiki pages: lowercase with underscores: `transformer_model.md`
- Multi-part sources: use base name without part suffix: `telegram_channel_name.md`

## Log Format

```
## [2026-04-20] ingest | Source Title
- Type: youtube/transcription
- Topics: [topic1, topic2]
- New pages: page1.md, page2.md
- Updated pages: page3.md, page4.md
```

## Tools

- **qmd** — Local search engine for markdown files (optional, for larger wikis)
- **Obsidian** — Recommended viewer for graph view and bidirectional links
- **Git** — Version control for the wiki (implicit)

## Usage

- Keep `/raw/` organized by source type
- Process sources one at a time for best integration
- Review wiki pages in Obsidian to verify quality
- Ask lint questions to keep wiki healthy

---

This schema is a starting point. It evolves as we discover what works for this specific domain.