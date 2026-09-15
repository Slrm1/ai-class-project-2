# FitFindr — AI Senior Project 2

FitFindr is a multi-tool AI agent for secondhand fashion. It helps a user search mock thrift listings, decide how a found item works with their wardrobe, and generate a shareable fit-card caption. The agent must make decisions based on tool results, preserve state across calls, and recover gracefully when a tool fails or returns nothing useful.

## Full Assignment

The complete project brief is saved in [`ASSIGNMENT.md`](./ASSIGNMENT.md).

## Required Tools

```python
search_listings(description, size, max_price)
suggest_outfit(new_item, wardrobe)
create_fit_card(outfit, new_item)
```

## Core Requirements

- At least 3 distinct tools with clearly defined interfaces.
- A planning loop that changes behavior based on previous tool results.
- State management across tool calls in the same session.
- Error handling for every tool.
- A complete multi-step workflow using all 3 required tools.
- `planning.md` in the repository root.
- README documentation whose tool signatures match the actual code.
- Pytest tests for normal and failure paths.
- A 3–5 minute demo video linked from this README before submission.

## Recommended Stack

- Python
- Groq API
- `meta-llama/llama-4-scout-17b-16e-instruct`
- Gradio
- Pytest
- Mock listing and wardrobe data from the FitFindr starter repo

## Setup

Create a virtual environment:

```bash
python -m venv .venv
```

Activate it on Mac/Linux:

```bash
source .venv/bin/activate
```

Windows Git Bash:

```bash
source .venv/Scripts/activate
```

Windows Command Prompt:

```bash
.venv\Scripts\activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Create a `.env` file in the repo root:

```env
GROQ_API_KEY=your_key_here
```

Never commit `.env`.

## Submission Checklist

- [ ] Add/fork the official FitFindr starter files into this repository.
- [ ] Complete `planning.md` before implementation.
- [ ] Implement and test all three required tools.
- [ ] Implement the planning loop and session state.
- [ ] Deliberately test each required failure mode.
- [ ] Run `python -m pytest tests/` successfully.
- [ ] Complete the final README documentation.
- [ ] Add at least 2 specific AI-usage examples.
- [ ] Record and link the 3–5 minute demo video.
- [ ] Confirm the documented tool signatures exactly match the actual code.
