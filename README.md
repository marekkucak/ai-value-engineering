# AI Value Engineering Masterclass

Private Equity Value Masterclass for AI & Graph Engineers.

## Setup

This project uses `uv` for dependency management.

```bash
# Install all dependencies
uv sync

# Activate the virtual environment
source .venv/bin/activate
```

## Running Lessons

All lessons are in Jupyter notebooks under the `notebooks/` directory:

- `00_foundations_environment_and_value_thinking.ipynb` - Foundation (mandatory prerequisite)
- `01_finance_for_ai_engineers.ipynb` - Finance fundamentals
- And more...

```bash
# Run a notebook
jupyter notebook notebooks/00_foundations_environment_and_value_thinking.ipynb
```

## Project Structure

```
ai-value-engineering/
├── notebooks/              # Lesson notebooks
├── reports/
│   └── templates/         # Exercise templates
├── src/
│   └── value_models/      # Python modules for value calculations
├── tests/                 # Test suite
├── pyproject.toml         # Project configuration
├── uv.lock               # Locked dependencies
└── AI_VALUE_ENGINEERING_MASTERCLASS.md  # Curriculum guide
```

## Development

```bash
# Install with dev dependencies
uv sync --all-extras

# Run tests
pytest

# Format code
black src tests

# Lint
ruff check src tests
```
