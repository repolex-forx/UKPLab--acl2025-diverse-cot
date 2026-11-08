# Repolex Knowledge Graph of UKPLab/acl2025-diverse-cot

RDF knowledge graph data for [UKPLab/acl2025-diverse-cot](https://github.com/UKPLab/acl2025-diverse-cot), parsed by [repolex](https://repolex.ai).

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
rlex download UKPLab/acl2025-diverse-cot
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── f1fa7e8e386ca3b7099f48ed73cc1e1dc792cc71
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── f1fa7e8e386ca3b7099f48ed73cc1e1dc792cc71
│           └── chunk-001.nq.gz
├── blob
│   ├── 070f77f20283773244e64cd2ca60c4de79da72e3.nq.gz
│   ├── 13a226f751ac5c36b45c97b8762f7a3aa35f5676.nq.gz
│   ├── 1fdb828f306a3d6ee8fb08ba802b0eb0f4bd2627.nq.gz
│   ├── 229edba242bb190698662cdce6bdacde9f0769fe.nq.gz
│   ├── 261eeb9e9f8b2b4b0d119366dda99c6fd7d35c64.nq.gz
│   ├── 2754bdf24077836f587955919eff068d23873f30.nq.gz
│   ├── 2a7a5a068927f2f8aa8104c1a09ea602787682d5.nq.gz
│   ├── 3001993a6d7c3dd4ee97858a508b52ccc5a1d5b1.nq.gz
│   ├── 43cff5f71e993b7358a04314fef277267bd8bed7.nq.gz
│   ├── 4ec9d3310aac81ba078c622fb7f96a7419f44de8.nq.gz
│   ├── 7f8263d93aeca1e414865138214aec2440f4d331.nq.gz
│   ├── 95c1663008c94f55e8fbb3701b5d160168468db0.nq.gz
│   ├── 969a1680886ace31b1ef3cc27f5084d6e62b2305.nq.gz
│   ├── 9af30a049386b43cdfd5884d4f8b8907043ad2d7.nq.gz
│   ├── 9b3703a912d40f58fb0fb57d20742e53d9fe7671.nq.gz
│   ├── 9ec0c5cd4825cf30bea07c097c3187784133e04a.nq.gz
│   ├── a55eff4940f608ffc4ab3ca15148ee75bb2bc1fc.nq.gz
│   ├── a9afa90b1a7a3a217325c2501516190808ba55fa.nq.gz
│   ├── bf2581766d25a7685fa11956b42992e847d903ba.nq.gz
│   ├── c08a79032592be8f5e7318991b0242323389469d.nq.gz
│   ├── c6718de5c5ae59d2c22141a147f5afba41af9cbb.nq.gz
│   ├── cb425eb6edbb34466de43af5d6277b66854efe49.nq.gz
│   ├── d101602612cb8f241432642ca51988d0d0442ff6.nq.gz
│   ├── d62fc66df4b9acdd5381753fde4173a5775b1ddf.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── ed3a9d377ba3c30e6eb8b2a35e08e8dc814a0725.nq.gz
│   ├── f290733e33cbdc31e6ae488651dfed76d92dd6c5.nq.gz
│   └── f3041423d3fc1748d98fd13aba285a4d310c57fb.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── f1fa7e8e386ca3b7099f48ed73cc1e1dc792cc71.nq.gz
├── issue
│   └── issue.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 35 files
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

[UKPLab/acl2025-diverse-cot](https://github.com/UKPLab/acl2025-diverse-cot)

---
*Parsed on 2026-11-08 by [repolex](https://repolex.ai)*
