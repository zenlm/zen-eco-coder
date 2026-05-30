# Zen Eco 4B Coder

Code generation and analysis model. Part of the Zen Eco family.

[![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

## Overview

Zen Eco 4B Coder is the code-specialized variant of Zen Eco 4B. Optimized for code generation, completion, debugging, and explanation across multiple programming languages while retaining the compact Eco architecture.

| Property | Value |
|----------|-------|
| Parameters | 4B |
| Context | 32K |
| License | Apache 2.0 |

## Usage

```python
from transformers import AutoModelForCausalLM, AutoTokenizer

model = AutoModelForCausalLM.from_pretrained("zenlm/zen-eco-coder")
tokenizer = AutoTokenizer.from_pretrained("zenlm/zen-eco-coder")

messages = [{"role": "user", "content": "Write a Python function that implements binary search on a sorted list."}]
inputs = tokenizer.apply_chat_template(messages, return_tensors="pt")
output = model.generate(inputs, max_new_tokens=512)
print(tokenizer.decode(output[0], skip_special_tokens=True))
```

## Related

- [zen-eco](https://huggingface.co/zenlm/zen-eco) — Base 4B model
- [zen-code](https://huggingface.co/zenlm/zen-code) — Standalone 4B code model
- [zen-coder](https://huggingface.co/zenlm/zen-5-coder-gguf) — 24B code model
- [Zen LM](https://github.com/zenlm) — Full model family

Apache 2.0 · [Zen LM](https://zenlm.org) · [Hanzo AI](https://hanzo.ai)
