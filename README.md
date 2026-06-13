# llm-rag

A small repository exploring Retrieval-Augmented Generation (RAG) techniques with large language models. This project contains example code and a notebook that demonstrate how to index, retrieve, and use external documents to augment LLM responses.

## Project summary

- **Purpose:** Learn and prototype RAG workflows (vector indexing, retrieval, prompt construction, and generation) using lightweight examples.
- **Contents:** `main.py` (example runner), `notebook.ipynb` (interactive walkthrough), and minimal packaging metadata (`pyproject.toml`).

## Features

- Simple end-to-end example showing how to:
	- Ingest documents / chunks
	- Build a vector index
	- Retrieve relevant passages
	- Compose prompts for an LLM using retrieved context
- Interactive notebook for experimentation and explanation

## Requirements

- Python 3.10 or newer
- Git (optional, for cloning)

Dependencies are managed in `pyproject.toml`. If you prefer a requirements file, you can generate one from your environment.

## Quick setup

1. Create and activate a virtual environment

```bash
python -m venv .venv
source .venv/bin/activate
```

2. Install dependencies (using pip + pyproject)

```bash
python -m pip install --upgrade pip
python -m pip install -e .
```

If you don't have an editable installable package defined, alternatively install common tooling manually, for example:

```bash
# example, adapt as needed
python -m pip install jupyterlab numpy faiss-cpu sentence-transformers openai
```

## Running the examples

- Interactive notebook: open `notebook.ipynb` in Jupyter or JupyterLab and run the cells to follow the walkthrough.

```bash
jupyter lab notebook.ipynb
```

- Scripted run: `main.py` contains a simple entry point and example flows. Run it with:

```bash
python main.py
```

Adjust configuration (API keys, model names, dataset paths) via environment variables or by editing the top of the notebook/script.

## Configuration

- Keep secrets out of the repo. Use environment variables for API keys, e.g. `OPENAI_API_KEY` or other provider keys.
- Example (bash):

```bash
export OPENAI_API_KEY="sk-..."
```

## Development

- Formatting: use `black` and `isort` for consistent formatting.
- Linting: use `flake8` or `ruff`.
- Tests: add pytest-based tests under a `tests/` folder and run `pytest`.

Example dev install:

```bash
python -m pip install -e .[dev]
```

## Contributing

- Contributions, bug reports, and suggestions are welcome. Please open an issue first to discuss larger changes.
- When submitting a PR, include clear description, tests (when applicable), and follow the existing code style.

## Notes and next steps

- Add a `LICENSE` file to clearly state the project's license.
- Add a `requirements.txt` or extend `pyproject.toml` with optional extras for dev/test.
- If you want, I can:
	- Add example data and a minimal vector store implementation
	- Wire up a specific LLM provider example (OpenAI, local Llama, etc.)

## Contact

If you want help extending this README with provider-specific instructions or runnable examples, tell me which provider and I'll update the docs.

---