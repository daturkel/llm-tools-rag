# llm-tools-rag

A tool plugin for [LLM](https://llm.datasette.io/) that allows you to search over your embedding collections.

[![PyPI](https://img.shields.io/pypi/v/llm-tools-rag.svg)](https://pypi.org/project/llm-tools-rag/)
[![Changelog](https://img.shields.io/github/v/release/daturkel/llm-tools-rag?include_prereleases&label=changelog)](https://github.com/daturkel/llm-tools-rag/releases)
[![Tests](https://github.com/daturkel/llm-tools-rag/actions/workflows/test.yml/badge.svg)](https://github.com/daturkel/llm-tools-rag/actions/workflows/test.yml)
[![License](https://img.shields.io/badge/license-Apache%202.0-blue.svg)](https://github.com/daturkel/llm-tools-rag/blob/main/LICENSE)

## Installation

Install this plugin in the same environment as [LLM](https://llm.datasette.io/):

```bash
llm install llm-tools-rag
```

## Usage

Use `-T RAG` to enable the RAG tools. You can specify a non-default database with `-T RAG("other_db.db")`.


```bash
llm -m claude-4-sonnet -T RAG "what are the available plugin hooks in llm?"
```

## Development

To set up this plugin locally, first checkout the code. Then create a new virtual environment:

```bash
cd llm-tools-rag
python -m venv venv
source venv/bin/activate
```

Install the dependencies and test dependencies:

```bash
pip install -e '.[test]'
```

To run the tests:

```bash
pytest
```

## Dependencies

- [llm](https://llm.datasette.io/): The LLM CLI tool this plugin extends
- [sqlite-utils](https://sqlite-utils.datasette.io/en/stable/): For querying LLM's sqlite databases