# Reflection

This notebook demonstrates a complete end-to-end AI agent designed for my master's thesis, where the system converts natural-language software requirements into structured test artifacts. The agent processes each requirement through a four-stage pipeline consisting of data understanding, reasoning, inference, and structured output generation. Gemini 2.5 Flash-Lite was used as the core model due to its low latency and reliable output consistency, making it suitable for iterative requirement analysis.

Prompt engineering played a central role: zero-shot prompts allowed the model to process previously unseen requirements, while few-shot prompts improved stability and coverage by providing the model with high-quality examples. The pipeline successfully produced augmented requirements, test cases, and evaluation metrics in structured JSON format, demonstrating its ability to support automated test design workflows.

What worked well was the model’s ability to identify key test dimensions and generate coherent, testable requirement reformulations. The system also proved flexible and reproducible through GitHub-stored prompts and Colab execution. Future improvements could include integrating token-based cost calculations, validating generated test cases automatically, and experimenting with larger Gemini models to improve overall precision and robustness.
