# Injection

This project tests how well a local LLM can protect information stored in its system prompt against prompt injection attacks.

For the experiment I used Ollama with Qwen3:8B. A fake banking assistant was given a system prompt containing a dummy secret, and 120 different prompts were used to try to make the model reveal it.

## Setup

The project uses:

- Python 3
- Ollama
- Qwen3:8B
- OpenAI Python SDK



```powershell
pip install openai
```
