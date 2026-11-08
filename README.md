# Repolex Knowledge Graph of modal-labs/quillman

RDF knowledge graph data for [modal-labs/quillman](https://github.com/modal-labs/quillman), parsed by [repolex](https://repolex.ai).

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
rlex download modal-labs/quillman
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 43f7532979084eba1b3d24408921b3511bcc85b2
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 43f7532979084eba1b3d24408921b3511bcc85b2
│           └── chunk-001.nq.gz
├── blob
│   ├── 15d2fa3dec2b8bda5f7c72b82801464caad9e1a3.nq.gz
│   ├── 2c896294cecff27c348f9dc0d77b20e5b688ef65.nq.gz
│   ├── 2c8a399956ddf37180a6bd6517449fa19ad8d1fb.nq.gz
│   ├── 312bf915dd0d3c5228aef3b55cf19a3b1e509d6b.nq.gz
│   ├── 34221302e7c2ac6768c141dd45872667f9b8b0c3.nq.gz
│   ├── 396074e650c89410f99022bd5fc323b3d8e58f29.nq.gz
│   ├── 431dda228b020d3f7cd84cc4d9d234e94070d0ba.nq.gz
│   ├── 44a740e975a84d757a76794d381c4f90112f6591.nq.gz
│   ├── 4eed631055d49cc5eb06a29a7f3d43898bd32e6c.nq.gz
│   ├── 571ae0147df309c93d7b2e24e2a2b3430de91d75.nq.gz
│   ├── 5be1bb276b9ba7731d8c64adeb5f42b9a7da479b.nq.gz
│   ├── 5e4a5f14002ad47f6b70159acde63fefcd0b41a5.nq.gz
│   ├── 6245e75bc73b341f28aa469520ec21cb2a7131ff.nq.gz
│   ├── 6c0c4bed3e72c8a1403f5ca0a58a69165cd854da.nq.gz
│   ├── 76cb6d42ae6f553720baa5843286fc18da19e776.nq.gz
│   ├── 7f6fe6aa47a31d7acbc48522d13e432e7abb1be9.nq.gz
│   ├── 8167c41b48c0c7e6148a44420026013e58d6615d.nq.gz
│   ├── 83a4689e387b4df325e40453fc196c141501bff2.nq.gz
│   ├── aaf11353604a3eac3528d740c876003641b305dd.nq.gz
│   ├── b535126f1239ab39bf7652647bd1722230c57801.nq.gz
│   ├── c3001fea2ed4d9b0b0378792d294c44fef9ebffb.nq.gz
│   ├── c3bf2791706c65b105fb4c78e18dcbf5f30badc9.nq.gz
│   ├── ca1ec9b7a431c41547688825534b30e064d8a32d.nq.gz
│   ├── ddfdd124e460a20357af2613ebfeeb5c7b0948a9.nq.gz
│   ├── e90aac231000c0338bf7d652187fd1badb354969.nq.gz
│   └── f2e4d530a539ca9b0cddd5ce0b2b7873e7ce04b6.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 43f7532979084eba1b3d24408921b3511bcc85b2.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 34 files
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

[modal-labs/quillman](https://github.com/modal-labs/quillman)

---
*Parsed on 2026-11-08 by [repolex](https://repolex.ai)*
