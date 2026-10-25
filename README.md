# PowerOllama
[![Static Badge](https://img.shields.io/badge/hugging%20face-powerollama-yellow?logo=hugging%20face)](https://huggingface.co/powerollama)
[![Static Badge](https://img.shields.io/badge/ollama-PowerOllama-white?logo=ollama)](https://ollama.com/PowerOllama)

Soft fork of ollama-python that add tweaks to the repository.

## What you need
- [Ollama](https://ollama.com) should installed and running
- Pull a model to use a library: `ollama pull <model>` (for example: `ollama pull gemma4:31b-cloud`)
  - See [the available models in Ollama](https://ollama.com/search).

## Install
```sh
pip install powerollama
```

## Usage
```py
import os
from ollama import Client

client = Client(
    host='https://ollama.com',
    headers={'Authorization': 'Bearer ' + os.environ['OLLAMA_API_KEY']},
)

response = client.chat(
    model='OLLAMA_MODEL',
    messages=[{'role': 'user', 'content': 'Hello!'}],
)
print(response.message.content)
```
