# Injection

This project tests how well a local LLM can protect information stored in its system prompt against prompt injection attacks.

For the experiment I used Ollama with Qwen3:8B. A fake banking assistant was given a system prompt containing a dummy secret, and 120 different prompts were used to try to make the model reveal it.

## Setup

The project uses:

- Python 3
- Ollama
- Qwen3:8B
- OpenAI Python SDK

The Python code connects to Ollama using its OpenAI compatible API.

## Project Files

```text
prompt-injection-test/
    main.py
    test.py
    prompts.txt
    results.json
    README.md
```

`main.py` runs all the attacks and checks if the secret was leaked.

`test.py` is used to check if Python can connect to Ollama.

`prompts.txt` contains the 120 attack prompts.

`results.json` stores the responses and test results.

## Installation

Install Ollama and download the model:

```powershell
ollama pull qwen3:8b
```

Check that it is installed:

```powershell
ollama list
```

Install the Python library:

```powershell
pip install openai
```
