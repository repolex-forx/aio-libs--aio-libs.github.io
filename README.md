# Repolex Knowledge Graph of aio-libs/aio-libs.github.io

RDF knowledge graph data for [aio-libs/aio-libs.github.io](https://github.com/aio-libs/aio-libs.github.io), parsed by [repolex](https://repolex.ai).

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
rlex download aio-libs/aio-libs.github.io
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 9a757da58945414c01c5b83be45ea7fca3efd570
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 9a757da58945414c01c5b83be45ea7fca3efd570
│           └── chunk-001.nq.gz
├── blob
│   ├── 06b167d671c576e05418923ca2dcc0b3d4ef53ec.nq.gz
│   ├── 0b3ebacb0bf7deea8ee9a68b7bfd20d10fc07be3.nq.gz
│   ├── 1ad21689737540eff5a3302dd8bfb208e451b9c5.nq.gz
│   ├── 22ed6809c751f8826e575ca0d5bcb70836667b69.nq.gz
│   ├── 238827eb2372e86dd5a41ebc96d22a274bc2f03d.nq.gz
│   ├── 308cf128257742f5748a31a27d2c245c8f445857.nq.gz
│   ├── 3314b3f2cfef22e7629011c93dec08634364458d.nq.gz
│   ├── 4a5d51c6e4c1dcb7fc6393e04023911b6552601d.nq.gz
│   ├── 518f807b9d76231c1fc3beebf418e688fcc67ffd.nq.gz
│   ├── 5da929f2371863ed71709a149a0027f116b55b6d.nq.gz
│   ├── 6d394e5d1a83d15ec88bcb5ae6312efa3bfa42a2.nq.gz
│   ├── 748aa882f8b9340547addc69cc436ff31a7be1eb.nq.gz
│   ├── 798b1f12baf05e99ba669633dcf755b7d79ca015.nq.gz
│   ├── 7ba5c04f7240b6d35aae2a7dd28a4d29d0a3d5ce.nq.gz
│   ├── 8064ae45f78437d8366ce6e97c96500b9fca666f.nq.gz
│   ├── 826d274d7f83814a93b3b5651df1998dc50d5c00.nq.gz
│   ├── 8410c60256ecb19727b52f79e41973ffac4787f3.nq.gz
│   ├── 85dfaa70237a7a8b5449b99b8baa6c34af4e5551.nq.gz
│   ├── a93e7c7c0559d4ff969b3a18b2a010cf949d0b8f.nq.gz
│   ├── aa1b7c6890ce12f157c74a9114afc87e6cdae9ef.nq.gz
│   ├── b579bb313db90cc5425095d23dba950aa6612dc3.nq.gz
│   ├── b9fb8a6e0f4a5ce99899eb97d872c6b90f4bb678.nq.gz
│   ├── c50dd77c4f8e55cba6d8c3653ebdb0f0ef52c01f.nq.gz
│   ├── cbdf9fe61300e144fdaab991cb8b65086ecb0684.nq.gz
│   ├── d1ca01f62eaf78f2b719f22184a5fddc76313376.nq.gz
│   ├── dc4e0da42182d8b97b75bc6d7052d24ff7c967c5.nq.gz
│   └── f9fc04f8e1a0afff30b8492a8a76f6518488d5c6.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 9a757da58945414c01c5b83be45ea7fca3efd570.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 35 files
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

[aio-libs/aio-libs.github.io](https://github.com/aio-libs/aio-libs.github.io)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
