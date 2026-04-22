# Repolex Knowledge Graph of dryrust/clientele.rs

RDF knowledge graph data for [dryrust/clientele.rs](https://github.com/dryrust/clientele.rs), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [lexq](https://github.com/repolex-ai/lexq) query tool using [uv](https://docs.astral.sh/uv/getting-started/installation/).

If you have uv installed, just copy/paste this into your terminal:

```bash
uv tool install git+https://github.com/repolex-ai/lexq
```

This installs lexq onto your system, in your user context. Verify the install:

```bash
lexq --help
```

**lexq is designed to be used primarily by LLMs in a terminal.** Start up your favorite LLM and ask it to use the lexq tool. It's that easy!

To load this repo's data:

```bash
lexq download dryrust/clientele.rs
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 18a9d41f329119836131c590ec8710bdddc65862
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 18a9d41f329119836131c590ec8710bdddc65862.nq.gz
│   └── repolex
│       └── 18a9d41f329119836131c590ec8710bdddc65862
│           └── chunk-001.nq.gz
├── blob
│   ├── 0cfdfe7ead12369a332fb5be762b50830e93c367.nq.gz
│   ├── 13edb27f8341a15f7ef6805243c5be8572913129.nq.gz
│   ├── 1e7ca88b96ba21913aeed5ee68e234a9868cebdb.nq.gz
│   ├── 1f9f3eb7b008cf8b62d9e4584fea34176c849993.nq.gz
│   ├── 280fb8d04170d32ee9c5f1537fb204382a2602ff.nq.gz
│   ├── 3103d428e8a8b43f3d41d71774dee44857d6f288.nq.gz
│   ├── 5f5cf896c81688e4360b37f1bcda92f7bc6f7423.nq.gz
│   ├── 6192e6925dff3083df053cf84f5ca8a604f39489.nq.gz
│   ├── 6472060b2ac2ab00599cbbb670a3e4fe6fe0be32.nq.gz
│   ├── 667843220966d5b3fc41ad157f74d482178d3134.nq.gz
│   ├── 686e51e6d7cb801635347e1ad44749194ebc1a92.nq.gz
│   ├── 75e3b65f99b29f48ab230e3eab3de8d0b7a9229f.nq.gz
│   ├── 775b37f2025b0b0c44365b5ed0671d9f24131855.nq.gz
│   ├── 8ee22c050d49c1d63a3180d8f684f93b475f6af8.nq.gz
│   ├── a6fa4de3931924bb68781002b0ed540e2aa34970.nq.gz
│   ├── a718674ce58c2cb835775828c8a323d259c0848c.nq.gz
│   ├── aab5c707f23280be852a84681bb0b4c2fbca51f5.nq.gz
│   ├── af9908b08f4b33c32a0080af73f53bc0fa0cdce4.nq.gz
│   ├── c0bc4db04a094ec78ebc117cac0f4aeb8013b24c.nq.gz
│   ├── c1657c5d4344729828321cb24d01640b782bd524.nq.gz
│   ├── c7504b17b600cacd0a72d17b05bb8dae214c4791.nq.gz
│   ├── c7da62105d15b8a07a2e5fa399230557ad29f918.nq.gz
│   ├── d5ee7c5f1f0a7b210bfbddae2711bb0f6e88bc11.nq.gz
│   ├── e3e57a8ce4ccbf74759a6df8fa4a3980ff1c9209.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── efb98088164f5786b17e83ed384971fc3c74f93c.nq.gz
│   ├── f18f9a26707881dec0025409f0c76e174d69a574.nq.gz
│   ├── f6759fe53be8431d8a7555b8decccaf5d12e9392.nq.gz
│   ├── f81d1c59e7fb1837179f3390df8b31771814685d.nq.gz
│   └── fb52ac96e70cc013b86e94a29b4c3873ade1f179.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 18a9d41f329119836131c590ec8710bdddc65862.nq.gz
├── filetree
│   └── 18a9d41f329119836131c590ec8710bdddc65862.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

14 directories, 39 files
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

## Source repository

[dryrust/clientele.rs](https://github.com/dryrust/clientele.rs)

---
*Parsed on 2026-04-22 by [repolex](https://repolex.ai)*
