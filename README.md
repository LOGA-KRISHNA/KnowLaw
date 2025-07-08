# fine-tuned-knowlaw-bot

A fine-tuned language model developed for Indian legal domain tasks, such as answering legal questions, parsing court judgments, and navigating various legal acts and rules.

## 📌 Model Details

- **Base Model:** [your base model, e.g., DeepSeek R1]
- **Fine-tuned On:** Indian legal datasets (IPC, CRPC, Bare Acts, case summaries)
- **Use Case:** Chatbot, Legal Q&A, Document summarization, Legal search

## 🚀 How to Use

```python
from transformers import AutoModelForCausalLM, AutoTokenizer

tokenizer = AutoTokenizer.from_pretrained("logakrishna/fine-tuned-knowlaw-bot")
model = AutoModelForCausalLM.from_pretrained("logakrishna/fine-tuned-knowlaw-bot")

input_text = "What is the punishment for theft under IPC?"
inputs = tokenizer(input_text, return_tensors="pt")
outputs = model.generate(**inputs)
print(tokenizer.decode(outputs[0]))
