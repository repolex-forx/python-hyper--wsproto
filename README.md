# Repolex Knowledge Graph of python-hyper/wsproto

RDF knowledge graph data for [python-hyper/wsproto](https://github.com/python-hyper/wsproto), parsed by [repolex](https://repolex.ai).

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
rlex download python-hyper/wsproto
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 5e0685d0740ec30716897442f336de1118f5f40a
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 5e0685d0740ec30716897442f336de1118f5f40a
│           └── chunk-001.nq.gz
├── blob
│   ├── 0063d21fe889e5bc7bac2a41285c83684c3ee8ad.nq.gz
│   ├── 1092bf085ed4310adfd18388f98f28c648ba7381.nq.gz
│   ├── 10e3e7f89db0fe954ef2bf4bdb5551e8ff6e45c5.nq.gz
│   ├── 1d6d3ed13096e754bcefd59a119ca0be3a011770.nq.gz
│   ├── 21d5f33b9a284a9a2a53b2d496fe0b280843b52f.nq.gz
│   ├── 288276d54406aad9e159ea3d06b35fdcbedf0cc0.nq.gz
│   ├── 3979ab5f48bf4ecc0a796951c5c7cf5d4e9c0d59.nq.gz
│   ├── 39c2ef80c7980da4431c8a7bb2d26af88ad8f464.nq.gz
│   ├── 414084c8e455f2640887fb8d617db2b3d22f8546.nq.gz
│   ├── 44973043fa88ef3d232905391aa72bc894a9fc0d.nq.gz
│   ├── 46900f729adf251367cfb519a57184a7ba90c288.nq.gz
│   ├── 4916084cbcb4c4cf54ac2be3a9f6f7b1af5dc29a.nq.gz
│   ├── 5443348fc388f50d504ecb2a938a27d7cc422756.nq.gz
│   ├── 5a7e812b038fcb2e4ff7e05a14ffe07fb4f78022.nq.gz
│   ├── 6247f7e231716482115f34084ac61030743e0715.nq.gz
│   ├── 7ac1eaa11e54060a3d0026858033fc4cd0d79cd1.nq.gz
│   ├── 7d097cc3d20515780c7ef036dec2174105defffb.nq.gz
│   ├── 92921dcce8014c046dd20e9e04409e2b1590380f.nq.gz
│   ├── 9474654e9af76989359f6112220d77ee5444c5e1.nq.gz
│   ├── aa01a1818a595754d8e1af5290939215e8fe8859.nq.gz
│   ├── ab390b8bb010e5cc55d6f68ad40d0cd640dbf42c.nq.gz
│   ├── b452d9207d0323b9b3aea24f252282c22821674a.nq.gz
│   ├── b52b73dd4fda66e96ca786db51df9ec77ceb4f67.nq.gz
│   ├── b8a93f00ccdc7e4f5e38b3a95566e1f129480e5c.nq.gz
│   ├── bdc9c2132f084d81f1f592ad18717a14deee7d9c.nq.gz
│   ├── cc1078475a34f8ca1920708c751adccd32df63e6.nq.gz
│   ├── d0c3cbf1020d5c292abdedf27627c6abe25e2293.nq.gz
│   ├── d1bbdbceba39cd0b1b19adea860150b2865ca722.nq.gz
│   ├── db2472009c60acc72ca2f6f065bb4b674dc66746.nq.gz
│   ├── dd81b7c37ccf7f367cbbc10bcd8f3e992cc612d9.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── ec2461f4304e8042ec875811f461ff734bc84182.nq.gz
│   ├── f2d8a634c5c20c6cd24989af2c257ba8f37b5748.nq.gz
│   ├── f3d487febbc68b09b222ce1874482f93bde4517b.nq.gz
│   ├── f5642f79f21d872f010979dcf6f0c4a415acc19d.nq.gz
│   ├── f8cbff7e1c5434a87a5d00257be8f9c293bc7c2a.nq.gz
│   ├── fa55bc567f97a3fe682a7ee73ecbb713ebe44e61.nq.gz
│   └── fe46003569fde64035387ad796f3025f0ec450d1.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 5e0685d0740ec30716897442f336de1118f5f40a.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 46 files
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

[python-hyper/wsproto](https://github.com/python-hyper/wsproto)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
