# Repolex Knowledge Graph of asimov-platform/prefect-asimov

RDF knowledge graph data for [asimov-platform/prefect-asimov](https://github.com/asimov-platform/prefect-asimov), parsed by [repolex](https://repolex.ai).

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
lexq download asimov-platform/prefect-asimov
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── blob
│   ├── 0109f34f01d439968a5632a111cd1f1780a9ea6b.nq.gz
│   ├── 056fce806d0b314ebd074d1a664a6fa90e135f89.nq.gz
│   ├── 1d013ff92fa855fb03f148d15f9488c339392020.nq.gz
│   ├── 2391f73aa051d3804285ce744f2e9a1c7e08993d.nq.gz
│   ├── 24ee5b1be9961e38a503c8e764b7385dbb6ba124.nq.gz
│   ├── 32d46ee883b58d6a383eed06eb98f33aa6530ded.nq.gz
│   ├── 5247f6f2ed57d73bee8eeccbcefe181e1a0278e5.nq.gz
│   ├── 77d6f4ca23711533e724789a0a0045eab28c5ea6.nq.gz
│   ├── c29be08c8d0cb1597ac9c00a94811545824089df.nq.gz
│   ├── cd8caa246424c5cee3d81c5c9b2537385483e940.nq.gz
│   ├── e3e57a8ce4ccbf74759a6df8fa4a3980ff1c9209.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e84586e320ee8c29eddccbc73bd443f730bebc08.nq.gz
│   ├── e8aa4e17969f232da002dce9f8c0daebd7162a7f.nq.gz
│   ├── eced1c4471c6ee324049cdf09e0c20bac1685059.nq.gz
│   ├── ed800cec0c6afc609a0945228943762963cf603e.nq.gz
│   └── efb98088164f5786b17e83ed384971fc3c74f93c.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 6e86390a33dccc85034a406227cf5bf538c0b840.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

7 directories, 22 files
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

[asimov-platform/prefect-asimov](https://github.com/asimov-platform/prefect-asimov)

---
*Parsed on 2026-04-03 by [repolex](https://repolex.ai)*
