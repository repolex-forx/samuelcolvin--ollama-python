# Repolex Knowledge Graph of samuelcolvin/ollama-python

RDF knowledge graph data for [samuelcolvin/ollama-python](https://github.com/samuelcolvin/ollama-python), parsed by [repolex](https://repolex.ai).

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
rlex download samuelcolvin/ollama-python
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 70dd0b7e639f5b6b39e15963521f1d4c6810464b
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 70dd0b7e639f5b6b39e15963521f1d4c6810464b
│           └── chunk-001.nq.gz
├── blob
│   ├── 0097af16412576a82f69cbc9be40d96cf2956f74.nq.gz
│   ├── 0bd2e01cf6b30f2daf72d8c616d7ac7af747b2ce.nq.gz
│   ├── 10b7dc76b5b4752ce7a5f2402a9dd9dbc51cd065.nq.gz
│   ├── 19c3fdc19208d0da478caa4a5b1b36d1616e89a9.nq.gz
│   ├── 1a2311dcf4e9514f6332613351605d221a312fe3.nq.gz
│   ├── 23d736a818d77057731ef05d32619c02b28438c0.nq.gz
│   ├── 2a30f8a2ff761a17949a089ca04b2847fe100dd2.nq.gz
│   ├── 2de17b4c04829a8b8ef61276223596c0b83cf21c.nq.gz
│   ├── 32d4525734aaa1b6b2c49ceccc07cacea7770380.nq.gz
│   ├── 34d5230afb66317b0f175ded8de79a67a74770d1.nq.gz
│   ├── 39775d6e6ce5c98ddebc18c5bdd7188471489371.nq.gz
│   ├── 3be80a769df5fdf941e1e01536fbab0c0883cf9f.nq.gz
│   ├── 44b3716b9ba42239447fd71dc892e098a70ea682.nq.gz
│   ├── 50d556859bfe3eb339f4e5a40770b2419412d13b.nq.gz
│   ├── 5af145eae04756ce95ff60498299f760063677cf.nq.gz
│   ├── 68bc17f9ff2104a9d7b6777058bb4c343ca72609.nq.gz
│   ├── 81a50d9adcb888caeebd9ecab2c4f0552310e974.nq.gz
│   ├── 8200ce3709aed4fd7f6a361819499d6e77d3c9ef.nq.gz
│   ├── 87fa8810b40971212fff524c59463e028de943f1.nq.gz
│   ├── 8a2db439abb9f2fdb86dce70cfa976d4932a9d75.nq.gz
│   ├── 8aff9f4615bfba4505a4139aa121c34a269fba71.nq.gz
│   ├── 8e3dc978a7ca8c53f56bbedc5b558116140fc02e.nq.gz
│   ├── 932355bf83f2fcdcfd903f4637123726970971b8.nq.gz
│   ├── 9dd9c264eff8adfb2ed733a02302775c2fa6047e.nq.gz
│   ├── 9fb1e3b22bcc169c77670066d9b6a7ba9ddfdabc.nq.gz
│   ├── aab2f2ed18d1125b4a93129ff158a0bea49f698f.nq.gz
│   ├── afafd2fc411f71472a48aab07b1c5f7d4fc29025.nq.gz
│   ├── b2c8dacc67be7d98f30982f7215842a29e6e6d3f.nq.gz
│   ├── b55fd4e1e10e3fabdaad284481e9715293294ec1.nq.gz
│   ├── b6ab33be19ba48b5ce3dd5f9f6ff6245bedaf02e.nq.gz
│   ├── c0b67c99783bef08d83843d7b9d1610aa2444c78.nq.gz
│   ├── c7bfb08039f2e63acba0b4baa03422f684c18059.nq.gz
│   ├── cb28ccdfdbea20d8dc23ff574d56b84bbdbcb6b9.nq.gz
│   ├── cccab01aeeb3d095a42e3e5352d0a5c1f5c7125a.nq.gz
│   ├── d4b5b1f3b4c01063023bb8dfdfa2bf11e1d015a5.nq.gz
│   ├── e24f2e9450ee50ac613361d97f44c70774bd474b.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── f461b937577a79dd7c1c0d43877ef92ae9f7448f.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 70dd0b7e639f5b6b39e15963521f1d4c6810464b.nq.gz
└── tag
    └── tag.nq.gz

11 directories, 44 files
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

[samuelcolvin/ollama-python](https://github.com/samuelcolvin/ollama-python)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
