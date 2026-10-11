# Repolex Knowledge Graph of pytest-dev/pygments-pytest

RDF knowledge graph data for [pytest-dev/pygments-pytest](https://github.com/pytest-dev/pygments-pytest), parsed by [repolex](https://repolex.ai).

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
rlex download pytest-dev/pygments-pytest
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 91ed6b6211bfa3effdfc57c2b85608906298dc3c
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 91ed6b6211bfa3effdfc57c2b85608906298dc3c
│           └── chunk-001.nq.gz
├── blob
│   ├── 02695093389e145ec12628bdb1e76c14524e7053.nq.gz
│   ├── 09f5cffb0c1c23305c75e50061f662ce85e89a72.nq.gz
│   ├── 16a79a8f3e92f045209d05cc646cfc6665b08ae7.nq.gz
│   ├── 16b5cc26a94a3f2877c845b8582e2dcc237aa38d.nq.gz
│   ├── 18483232503156c190648b7285a49d8e699ad87a.nq.gz
│   ├── 3d93aefb2da505dba9c0114404cfaaeee5ad0d3f.nq.gz
│   ├── 4248ffc4e8e1f601bd44c74c085814574e10a4e6.nq.gz
│   ├── 4f8c448cee0e59698bc375827346166dc293e085.nq.gz
│   ├── 7bd926afce5f068d9843205dd6a781b0dc5d5768.nq.gz
│   ├── 7ec0f933100dac51f5743ae6be2e47579235bc53.nq.gz
│   ├── 98773dd6fb07fe7cd2f71b10f94edb2dcf2b9a62.nq.gz
│   ├── a2bdb83a92e77fa106a5e0b8dc9dfca6c0b5075d.nq.gz
│   ├── b7af5ef213084fe100c5bb755659ef68c14dae5b.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── f48244ad667bdbc14d90d382a5955e7d1b1765f6.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 91ed6b6211bfa3effdfc57c2b85608906298dc3c.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 23 files
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

[pytest-dev/pygments-pytest](https://github.com/pytest-dev/pygments-pytest)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
