# Hugging Face Interface

Accessing Hugging Face Models.

Setup.

1. To use models, one may have to register and get access to. For instance to access Llamma model, one need to get access to from meta. It takes about an hour to get access to models.
2. Generate API Key aka HF tokens. Go to : https://huggingface.co/settings/tokens
3. Next login using this token. In bash type:  huggingface-cli login
   It will ask for HF token. Enter the token. and low login should be successful.
4. You can download the models and other components locally from HF hub. For instance:


```python
from transformers import AutoTokenizer, AutoModelForCausalLM

# Load the tokenizer and model from Hugging Face
model_name = "meta-llama/Llama-2-7b-chat-hf"  # You can specify other versions here

tokenizer = AutoTokenizer.from_pretrained(model_name)
model = AutoModelForCausalLM.from_pretrained(model_name, torch_dtype="auto", device_map="auto")
```
