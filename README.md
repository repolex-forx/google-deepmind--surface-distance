# Repolex Knowledge Graph of google-deepmind/surface-distance

RDF knowledge graph data for [google-deepmind/surface-distance](https://github.com/google-deepmind/surface-distance), parsed by [repolex](https://repolex.ai).

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
rlex download google-deepmind/surface-distance
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 1f805cea446805e559badc80dd27f34175e4173d
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 1f805cea446805e559badc80dd27f34175e4173d
│           └── chunk-001.nq.gz
├── blob
│   ├── 03692d025d0bda8f89bb2b9a0e02820a912fa3a1.nq.gz
│   ├── 067b9d617b7fa2094e8903db70961110e1599098.nq.gz
│   ├── 0d11d7d60f001be2fa9813a3c4c4dce4d45634b3.nq.gz
│   ├── 8e74e95791cb1de44bf81550be9b33d5a9a83276.nq.gz
│   ├── 9d1ccb5ea361c8e84e9db13254bbd6688c5d63c5.nq.gz
│   ├── d645695673349e3947e8e5ae42332d0ac3164cd7.nq.gz
│   ├── dc762cdd671efc9ab4ebcfac397c3a03a4e1b728.nq.gz
│   ├── ed38e2154fefabf380c5dc309806ac33b806f7c4.nq.gz
│   └── f74356dcd643073270e8defe573f09ce4886ab51.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 1f805cea446805e559badc80dd27f34175e4173d.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 17 files
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

[google-deepmind/surface-distance](https://github.com/google-deepmind/surface-distance)

---
*Parsed on 2026-11-06 by [repolex](https://repolex.ai)*
