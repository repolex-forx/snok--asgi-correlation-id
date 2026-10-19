# Repolex Knowledge Graph of snok/asgi-correlation-id

RDF knowledge graph data for [snok/asgi-correlation-id](https://github.com/snok/asgi-correlation-id), parsed by [repolex](https://repolex.ai).

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
rlex download snok/asgi-correlation-id
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 76b61b6325b2a0b29ee96dc1fbf00e2c7de15393
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 76b61b6325b2a0b29ee96dc1fbf00e2c7de15393
│           └── chunk-001.nq.gz
├── blob
│   ├── 04ca749e7e2c0b9df1ff341f62030e88096cdf8b.nq.gz
│   ├── 0dbe0a44a087eec96dd77581c7d14abe4a34610d.nq.gz
│   ├── 1a1b39dac9a741008b70f3882bbc63ab809beae8.nq.gz
│   ├── 1b741828fc51ced4bb4977b0e393658e15daa1b6.nq.gz
│   ├── 489d70e41a4ad475d331209cfb463ae31e2f5ad5.nq.gz
│   ├── 559db7131d1afeaf2f445d48f7713ef3389689ce.nq.gz
│   ├── 695f8a4d9119f5e7ae9f50f1951dac7a2c123b99.nq.gz
│   ├── 89f7c828aa201e137026b6bf67dbba9440091c13.nq.gz
│   ├── 8ca0598b81cd3ad23a5f4a95e3350835b609b978.nq.gz
│   ├── 9d206cfb48de73b237948eaec4728e5d2beec76b.nq.gz
│   ├── 9d90624253587a33feff65b96f8d33e831888514.nq.gz
│   ├── a24fc0f4b953fd60476302f1477cd77da561ed10.nq.gz
│   ├── af83fcdc1e69b5643abfa0c6b03d1eb813394697.nq.gz
│   ├── c8a582a64cf47b064c51f041402ceacfc78a97a5.nq.gz
│   ├── c8b65476b4e9007a62e1ffcddac9d248814da098.nq.gz
│   ├── d5f9027cfb9724176cf1e425abafafb9f9adeb88.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── fad90a930ee5caf05066bd88d1b65ad511d444cb.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 76b61b6325b2a0b29ee96dc1fbf00e2c7de15393.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 26 files
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

[snok/asgi-correlation-id](https://github.com/snok/asgi-correlation-id)

---
*Parsed on 2026-10-19 by [repolex](https://repolex.ai)*
