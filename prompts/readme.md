# Thesis AI Agent Prompts

This directory contains prompt examples for the **single AI agent** that implements my thesis system as an end-to-end solution.

## System idea (X → y)

The agent receives an input requirement **X** (functional or non-functional), written in natural language, and produces an output **y** with:

- Augmented / clarified requirement text (more testable, measurable).
- A set of model-specific results for multiple LLMs (e.g. GPT-4o-mini, Gemini-1.5-pro, Claude-3.5-sonnet):
  - Generated test cases count.
  - Quality metrics (coverage, testability, clarity, consistency, etc.).
  - Example test cases (step summary + expected result).
- A comparison summary that highlights which model is best by metric and overall.

The end-to-end pipeline of the single AI agent is:

1. **Data understanding** – read and analyse requirement X (id, title, description, type).
2. **Inference** – generate or refine testable acceptance criteria and test cases for each LLM model.
3. **Reasoning** – evaluate and score each model’s output using internal rubrics (coverage, testability, clarity, quality, etc.).
4. **Output generation** – return a structured JSON object **y** with all model results and a comparison summary.

All prompts in this folder:

- Explicitly describe the pipeline above.
- Enforce a strict JSON schema for the output.
- Avoid any extra natural language around the JSON (so the output is machine-readable).

Files:

- `prompt_01_zero_shot.txt` – single new observation X (zero-shot).
- `prompt_02_few_shot.txt` – few-shot prompt with several (X, y) examples from Lab 1.2 and a new X to predict y for.
