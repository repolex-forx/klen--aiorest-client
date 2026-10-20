# Repolex Knowledge Graph of klen/aiorest-client

RDF knowledge graph data for [klen/aiorest-client](https://github.com/klen/aiorest-client), parsed by [repolex](https://repolex.ai).

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
rlex download klen/aiorest-client
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 01ecced2be9e6a0ee6f15348d10f901b6b65c3ed
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 01ecced2be9e6a0ee6f15348d10f901b6b65c3ed
│           └── chunk-001.nq.gz
├── blob
│   ├── 090e8144dc7559fe5ad533ad458e950f2ef733ae.nq.gz
│   ├── 250649964bbc36f4bec2942f69238aa6f7c02c1a.nq.gz
│   ├── 2590b94515203e09292f244977b45b8bbf486011.nq.gz
│   ├── 31dd672a9516775eeea3e8992686f5c27ad352fd.nq.gz
│   ├── 33d31608ed66a56ce6f41218392345c660e00d90.nq.gz
│   ├── 385166988fbb8e86ac7b1388b749b6c47bddfca6.nq.gz
│   ├── 4246d7559803791d782756617140253a4183f8a4.nq.gz
│   ├── 50d3dbdfe56b5ef0ba7b60128119e85ecc1003e0.nq.gz
│   ├── 5a731136ed2cc49bb1b9f3001e349f8e2a84d049.nq.gz
│   ├── 604f69f7a6765ea0903c6a388d9192a8953ff88b.nq.gz
│   ├── 72a33558153fb57def85612b021ec596ef2a51b9.nq.gz
│   ├── 7585ad4b4d8efa180a9e8f3b32f9c5d9a7bcfd08.nq.gz
│   ├── 7a4ada64ab2125415019ab4f530e92772b27a9fa.nq.gz
│   ├── 89aa5cbd828a8bedca47b638260e14d00e944849.nq.gz
│   ├── 8ad2919065868c29e04d08276c383bf2aa5827d9.nq.gz
│   ├── 9697a042421f74b24fb461ae126ef1e10f50361b.nq.gz
│   ├── 98b8eab6bc8987a04101e2c44ca85aec8500c478.nq.gz
│   ├── bf50d49c21e10ca4898a533e085c8555bafabfea.nq.gz
│   ├── c112460f4046eb2788b2f93e70fd62775463352b.nq.gz
│   ├── c3d6a3b02607f5849a26fca46ce0dd40a7ff1777.nq.gz
│   ├── d4a2c4405ec2e962c521a13af91bf5f7098a62a8.nq.gz
│   ├── d6069322906e3340dd894917453c3ce5037fff52.nq.gz
│   ├── e122f914a87b277e565fc9567af1a7545ec9872b.nq.gz
│   ├── e582053ea018c369be05aae96cf730744f1dc616.nq.gz
│   ├── ee5047f7c786851f35cf6c04095a016833ee275b.nq.gz
│   ├── ef9fa89f42380a65e8f4d7616d4e99ef488107fe.nq.gz
│   ├── f1c095836630033a5efb8d3d7a825966835935b1.nq.gz
│   └── fea4bda8a5dccedc79087cc4b78cce16443e8826.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 01ecced2be9e6a0ee6f15348d10f901b6b65c3ed.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 36 files
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

[klen/aiorest-client](https://github.com/klen/aiorest-client)

---
*Parsed on 2026-10-20 by [repolex](https://repolex.ai)*
