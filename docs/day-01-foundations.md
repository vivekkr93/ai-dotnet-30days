# Day 01 — Foundations

Purpose
-------
Capture simple definitions, learning notes, and the chosen mini-prototype for Day 1.

Simple definitions (very simple language)
- AI: Systems that perform tasks that normally need human intelligence (writing, planning, reasoning).
- ML: Method to let programs learn patterns from data (classification, regression).
- LLM: Large Language Model trained on lots of text; good at generating and summarizing language.

Topic map
---------
- LLM: text generation engine
- Prompting: how to ask LLMs clearly
- Embeddings: convert text to vectors for similarity
- RAG: retrieval-augmented generation (search + LLM)
- Agents: LLM + tools + memory

Mini-prototype: /api/ai/summarize
--------------------------------
API design (simple)

- POST /api/ai/summarize
- Request JSON: { "text": "...", "maxSummaryChars": 800, "style": "bullet|paragraph" }
- Response JSON: { "summary": "...", "highlights": ["..."] }

Why this prototype
- Fast to implement and demonstrates LLM integration and prompt design.

Day 1 checklist
- [ ] Read definitions and confirm understanding
- [ ] Create repo docs and pick prototype
- [ ] Create minimal .NET 10 API scaffold (day01) — optional
- [ ] Add .env.example (do not commit secrets)
- [ ] Run a local test once Azure OpenAI keys are available

Troubleshooting notes
- 401/403: check AZURE_OPENAI_ENDPOINT and AZURE_OPENAI_KEY
- Deployment not found: ensure AZURE_OPENAI_DEPLOYMENT matches Azure deployment name
- Env vars not read: restart terminal or set them in PowerShell before running
