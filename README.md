# Repolex Knowledge Graph of jazzband/django-postgres-utils

RDF knowledge graph data for [jazzband/django-postgres-utils](https://github.com/jazzband/django-postgres-utils), parsed by [repolex](https://repolex.ai).

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
rlex download jazzband/django-postgres-utils
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 886279ba1d0070c81a3488ae085fe44ee598df60
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 886279ba1d0070c81a3488ae085fe44ee598df60
│           └── chunk-001.nq.gz
├── blob
│   ├── 18b1921610c62e24605235734cce1bf9a50dd00a.nq.gz
│   ├── 19f83d612ab4d96b90d47729d3a362dfc416a62b.nq.gz
│   ├── 29a39727b890ea29d27285a32ab45e03c45989b4.nq.gz
│   ├── 2bbd8296900e54795c923461991f649ca251043c.nq.gz
│   ├── 3cbfd7f985e4d9ed7fc6f36d98c52f4f89c44015.nq.gz
│   ├── 47eb7c77b56ef7b8b649edad7a17ced9c1fda0b6.nq.gz
│   ├── 4d7c7f01d0dc0050c0d45da6a458e0d7245bd0de.nq.gz
│   ├── 4f3cf97f52ec46a7f2af981b80375eb1a2a02303.nq.gz
│   ├── 51379e62e7054773c85b0f9a18e095a9fcc47118.nq.gz
│   ├── 5192a882c4d9d4ba4198e11e9ccfadfacf5d60e7.nq.gz
│   ├── 53b056e10d8ecc7e2d098a8014131ea1c2832337.nq.gz
│   ├── 636d547769c08bd5f95e99679515beda53b44edb.nq.gz
│   ├── 6fb1057880dc1555f596ea8fd74d16be797ab803.nq.gz
│   ├── 7f9e535a658fb0922fe43219d440b5781b4b2401.nq.gz
│   ├── 869cbef78a41806cbfc2b25e7dc65a3ce35119c8.nq.gz
│   ├── 883e5a60e11dab2de4992a730abbdce0c9e35087.nq.gz
│   ├── 8a3da194eb5d337880dae56b2e9c0421cb28f1da.nq.gz
│   ├── 8a7311e3632565bd594411ff3049fdcf3d5ae7bd.nq.gz
│   ├── 9534b018135ed7d5caed6298980c55e8b1d2ec82.nq.gz
│   ├── 9806af7f75d4df43d4423000173059109f1b896d.nq.gz
│   ├── a092b016c37ff6b365a0acb1210a8ce8024f663d.nq.gz
│   ├── a0eceaf580bc5ab9647aa03728199de7c0299f4a.nq.gz
│   ├── ad4414ce96415a2410299650de5888ba865024f2.nq.gz
│   ├── b9a148887859c9365875d15ae6299aad40fae72c.nq.gz
│   ├── c4131fd10a6447f85889a6ce8a6786c6c087d80d.nq.gz
│   ├── c55a0a48875e605192c63088d3450f46bb8d0cb2.nq.gz
│   ├── ce3d0dcd87c28d2a33d2d1771c0259e6ea64c34f.nq.gz
│   ├── d03c7c79930820207a6c396d926216f5b20f4cba.nq.gz
│   ├── d0c3cbf1020d5c292abdedf27627c6abe25e2293.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── fea0d1d0147c95765aa18ac44a14779a8ff518e7.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 886279ba1d0070c81a3488ae085fe44ee598df60.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 39 files
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

[jazzband/django-postgres-utils](https://github.com/jazzband/django-postgres-utils)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
