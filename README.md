# Repolex Knowledge Graph of plotly/chart-studio-dash-template

RDF knowledge graph data for [plotly/chart-studio-dash-template](https://github.com/plotly/chart-studio-dash-template), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [rlex](https://github.com/repolex-ai/rlex) query tool:

```bash
cargo install --git https://github.com/repolex-ai/rlex
```

Verify the install:

```bash
rlex --help
```

**rlex is designed to be used primarily by LLMs in a terminal.** Start up your favorite AI assistant and ask it to use rlex. It handles the SPARQL — you just ask questions in plain English.

To load this repo's data:

```bash
rlex download plotly/chart-studio-dash-template
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── f6d92a3d4fb4f59b7d6558a199e90e67fd683b6f
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── f6d92a3d4fb4f59b7d6558a199e90e67fd683b6f
│           └── chunk-001.nq.gz
├── blob
│   ├── 14e76ee7768132a899ad1e3723700c7d92e3507a.nq.gz
│   ├── 318e35b472e6eda48451ae8113a193ce8a3bd56c.nq.gz
│   ├── 94226c25ec547f207d78a64411a514df632f70b8.nq.gz
│   ├── 9ca4f0b71e86bf856cd1b08e7b85460fde1da1df.nq.gz
│   └── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── f6d92a3d4fb4f59b7d6558a199e90e67fd683b6f.nq.gz
└── tag
    └── tag.nq.gz

11 directories, 11 files
```

| Directory | What it contains |
|-----------|-----------------|
| `blob/` | Per-file AST graphs, content-addressed by git blob SHA. Each file in the source repo gets its own graph. |
| `aggregate/ast/` | Combined AST graph per parsed commit. Merges all blob graphs for a snapshot of the entire codebase at that point. |
| `aggregate/lsp/` | Language Server Protocol enrichment: resolved symbols, definitions, references, and type information. |
| `aggregate/dataflow/` | Interprocedural data flow edges between functions and modules. |
| `aggregate/repolex/` | Combined graph (AST + LSP + dataflow) per commit. |
| `commit/` | Git commit metadata (author, date, message, parent links). |
| `branch/` | Branch metadata. |
| `tag/` | Tag metadata. |
| `filetree/` | File tree snapshots per commit (which files existed and their blob SHAs). |
| `audit/` | Code architecture and graph audit reports per commit. |

## Source repository

[plotly/chart-studio-dash-template](https://github.com/plotly/chart-studio-dash-template)

---
*Parsed on 2026-11-07 by [repolex](https://repolex.ai)*
