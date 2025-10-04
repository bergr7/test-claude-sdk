# Claude Agent SDK Python Project

This project is built using the Claude Agent SDK Python framework.

## Project Structure

```
.
├── src/
│   ├── __init__.py
│   ├── agent.py           # Main agent implementation
│   ├── tools/             # Agent tools
│   │   └── __init__.py
│   └── utils/             # Utility functions
│       └── __init__.py
├── tests/
│   ├── __init__.py
│   ├── test_agent.py      # Agent tests
│   └── test_tools.py      # Tool tests
├── docs/
│   └── README.md
├── .env.example           # Environment variables template
├── .gitignore
├── main.py                # Entry point
├── pyproject.toml         # Project configuration
└── README.md
```

## Setup

1. Install dependencies:
```bash
uv sync
```

2. Configure environment variables:
- Copy `.env.example` to `.env`
- Add your Anthropic API key and other required credentials

## Running the Agent

```bash
uv run python main.py
```

## Testing

Run all tests:
```bash
uv run pytest
```

Run with coverage:
```bash
uv run pytest --cov
```

Run specific test markers:
```bash
uv run pytest -m unit        # Unit tests only
uv run pytest -m integration # Integration tests
uv run pytest -m e2e        # End-to-end tests
```

## Development

Format code:
```bash
uv run black .
uv run isort .
```

Lint code:
```bash
uv run ruff check .
```

Type checking:
```bash
uv run mypy src/
```

## Agent Architecture

This agent is built using Claude Agent SDK Python and follows these patterns:

- **Agent Class**: Main agent logic in `src/agent.py`
- **Tools**: Modular tools in `src/tools/`
- **State Management**: If required, state handling in agent class
- **Error Handling**: Comprehensive error handling with fallbacks
- **Testing**: Complete test coverage with unit and integration tests