# Repolex Knowledge Graph of twisted/filepath

RDF knowledge graph data for [twisted/filepath](https://github.com/twisted/filepath), parsed by [repolex](https://repolex.ai).

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
rlex download twisted/filepath
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 920f6bb38622b49b9afa89a86de818ee8f6daa94
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 920f6bb38622b49b9afa89a86de818ee8f6daa94
│           └── chunk-001.nq.gz
├── blob
│   ├── 059c07c4f031505bd87732bcdc4ab00cecd12b44.nq.gz
│   ├── 10a1c8dbdcdffa019dacfb08ce001c6529220e52.nq.gz
│   ├── 257c6fff8c1b5c835a0c3e8a478dc4af294a9fa3.nq.gz
│   ├── 259553681fb42ee4f42ef7dbd6610ff5968bd92a.nq.gz
│   ├── 2bfb9ef89215d352182f94278dbdc9940938d957.nq.gz
│   ├── 303c409efeba8fa89fcba98af6e2117fbf0dfb8e.nq.gz
│   ├── 3143a0bafe3caaa02abc10c6a85831bde24d227f.nq.gz
│   ├── 362c301ef0821e52954acea36d36dec9564a1e6b.nq.gz
│   ├── 4e7a544cf92103a057d7e967e63f5b5205faf3b5.nq.gz
│   ├── 6a375672ab63953f8b41ed48b77bb3fd5313ac38.nq.gz
│   ├── 72bba8246c39b149718b71e3a0da14f2fb76c236.nq.gz
│   ├── 78845c9559341e5654d090dcf4c7d260af191437.nq.gz
│   ├── 7ce8c126ab717705812dcaa76b871181bb173f8e.nq.gz
│   ├── 80d655b434e16280ec323e0ab644c89533524303.nq.gz
│   ├── 9a88cafecc6b31d9315301b74187cc3803a40400.nq.gz
│   ├── a8fc93609677df76e58464cecbcb561d4a4ef895.nq.gz
│   ├── cc2f060de7d6b0f8fd64c59ab0f8b6716d4afe32.nq.gz
│   ├── d6e926e97c4c5e3c44a801d08701feca03e83b10.nq.gz
│   ├── e2f643dbf92ec488a5b327f2a05609302d30b784.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── ebaf03c9645dbc8bfb8631ab59c5800f775f59d7.nq.gz
│   └── f431e76beda0e59e694df454154aad74a3b25f53.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 920f6bb38622b49b9afa89a86de818ee8f6daa94.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 30 files
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

[twisted/filepath](https://github.com/twisted/filepath)

---
*Parsed on 2026-10-15 by [repolex](https://repolex.ai)*
