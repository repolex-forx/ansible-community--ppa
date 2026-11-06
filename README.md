# Repolex Knowledge Graph of ansible-community/ppa

RDF knowledge graph data for [ansible-community/ppa](https://github.com/ansible-community/ppa), parsed by [repolex](https://repolex.ai).

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
rlex download ansible-community/ppa
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 1e60de5624392831225ee1de26979699f52c02ae
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 1e60de5624392831225ee1de26979699f52c02ae
│           └── chunk-001.nq.gz
├── blob
│   ├── 1a107c05fe67585374c1256db831b4e0ceac24a9.nq.gz
│   ├── 20f7d571c79fe06defe840ce785b7f7e9fe33b99.nq.gz
│   ├── 6399c0a544d777c134e5b5a11ca0cec4bc5005bb.nq.gz
│   ├── 7b527c2663895984936fac2de0a5c4265c5cd9cd.nq.gz
│   ├── 90d40550bcaa4d5864f570d7ec93cddc941a6efd.nq.gz
│   ├── ae58d8cd74c70a5f2b1cf462d81de13ebdcf3156.nq.gz
│   ├── b4d90790223b95552556ea895ac541a489a7379d.nq.gz
│   ├── d93883bbc9f29107abc330787dedfa5aec9214d6.nq.gz
│   ├── eccba2f7e3dc1754cfcaee0f5a9907487ac89c26.nq.gz
│   ├── f288702d2fa16d3cdf0035b15a9fcbc552cd88e7.nq.gz
│   ├── f4edda47b4c1873a9baad2d44da341f34aa75179.nq.gz
│   └── fc7f46c683f5e8b612eb0be1f7b31c4d4128d978.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 1e60de5624392831225ee1de26979699f52c02ae.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 20 files
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

[ansible-community/ppa](https://github.com/ansible-community/ppa)

---
*Parsed on 2026-11-06 by [repolex](https://repolex.ai)*
