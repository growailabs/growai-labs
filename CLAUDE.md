# Project Conventions for growai-labs

## Folder Structure (do NOT deviate without explicit approval)
- notebooks/          → All Jupyter notebooks & Colab files, subfolders by topic (e.g. notebooks/llm-basics/)
- experiments/        → Raw / exploratory code for specific techniques
  - rag/              → Retrieval-Augmented Generation experiments
  - agents/           → Agent frameworks & tool-use experiments
  - prompt-engineering/ → Prompt templates, chaining, few-shot examples
  - llm-evaluation/   → Benchmarks, evals, comparison scripts
  - (new topic)       → Create new sibling folder only when topic is clearly distinct
- projects/           → Polished, more complete mini-apps / demos (should have own README.md inside)
- scripts/            → Reusable helper scripts & utilities (e.g. data loaders, eval helpers)
- data/               → Small sample datasets only (gitignore large files / use git lfs if needed)
- docs/               → Markdown writeups, explanations, blog-style posts, architecture notes

## Rules Claude MUST follow
- Always place new files in the correct top-level folder — never create files directly in root unless it's CLAUDE.md, .gitignore, requirements.txt, pyproject.toml etc.
- When suggesting or creating a new experiment: propose a new subfolder under experiments/ with kebab-case or snake_case name matching the concept.
- Keep root clean: only essential files (README.md, CLAUDE.md, pyproject.toml / requirements.txt, .gitignore)
- Use descriptive subfolder names that match YouTube video topics for easy cross-referencing.
- When I say "add to rag" or "experiment with agents", automatically put code in the right place.
- Never suggest flattening structure or merging folders without strong justification.

## Style & Practices
- Python 3.10+, use modern type hints
- Notebooks: one concept per notebook when possible
- Commit messages: "feat: add [topic] experiment in experiments/[folder]"