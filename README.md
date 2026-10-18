# Repolex Knowledge Graph of borntyping/python-colorlog

RDF knowledge graph data for [borntyping/python-colorlog](https://github.com/borntyping/python-colorlog), parsed by [repolex](https://repolex.ai).

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
rlex download borntyping/python-colorlog
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 868b53d31d3a0d7bfd1d96585dfba4627009073f
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 868b53d31d3a0d7bfd1d96585dfba4627009073f
│           └── chunk-001.nq.gz
├── blob
│   ├── 0104707432e70d5bdc8c0ff617ccc59b9b40068f.nq.gz
│   ├── 124c84b43f86f4764fe745b9e92f3e32209df3ea.nq.gz
│   ├── 185b947353fbd973728018e78ed4751d9129f083.nq.gz
│   ├── 20bbb9698a3cdf348998e8b9158f893fea6c6287.nq.gz
│   ├── 277fb84085ce59f08566e843ba62e2acb62bd37c.nq.gz
│   ├── 332dcf40c80d67a2b114d4875a6016e630c3fac6.nq.gz
│   ├── 3892b90186db48449178b705af17bf3e69298a99.nq.gz
│   ├── 4be7b7f414d36423d9956ba67a03651aed4b5436.nq.gz
│   ├── 52ccec8e6a8ca0dbaf8a25a6d7601b0f73de7af1.nq.gz
│   ├── 54e383d1bf24e799fd9afe9ed0444d711b859543.nq.gz
│   ├── 55e0f3c2d976e6379d6aff776adab9d36cebbbda.nq.gz
│   ├── 58b285e15b1f501482378764aac19fc55eef3ac2.nq.gz
│   ├── 5bd75b83bed54c2645b2de8c58f0893b4ff503a4.nq.gz
│   ├── 5f09469ecf8f2f7fe908ac798a797bf78eddf247.nq.gz
│   ├── 806075495b1bd68da4eccb6a60caab327f862fe1.nq.gz
│   ├── 8ac11e17fb100d5f014032413268fb0f3f560915.nq.gz
│   ├── ab1f7059f89bd4904481c2e044244b5856469894.nq.gz
│   ├── b23e9f503d4cce04940416a6f635f4fb428f0afd.nq.gz
│   ├── ba9b4981732cb21f8c0a9c02c9f8a5301468fd6f.nq.gz
│   ├── c2e9a55589cf700404bb00ab171ba9204f4813e4.nq.gz
│   ├── d139a14e8b6572ca2432c00af6124a24701ca5f8.nq.gz
│   ├── d4b26ba7db7cbed2d4b9157e479636d2874fb0ed.nq.gz
│   ├── e05756fbac347d215d2f6732f00f2e9fab991381.nq.gz
│   ├── e339ebdae4503b6c1c64a9a2d796473e49771496.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── ea3476a81d5d79c1bf1ec5d2413dbbf990e3a3b7.nq.gz
│   ├── ef3747bad8bc502664a46c8971e1ac6962ac60a8.nq.gz
│   ├── f67d44ed891a5533e185fa7b8733a9560f376b3d.nq.gz
│   └── fb123b8bbe1985ef58c86eec996b8b100261ae71.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 868b53d31d3a0d7bfd1d96585dfba4627009073f.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 37 files
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

[borntyping/python-colorlog](https://github.com/borntyping/python-colorlog)

---
*Parsed on 2026-10-18 by [repolex](https://repolex.ai)*
