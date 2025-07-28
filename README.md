# Finetuned_MediBot
This project demonstrates how to fine-tune the DeepSeek-R1-Distill-Llama-8B model using the Unsloth library for efficient LoRA-based supervised fine-tuning. The model is trained on a medical question-answering dataset with complex reasoning chains.

## 🚀 Workflow Overview
### Environment Setup:
- Authenticate with Hugging Face and Weights & Biases using kaggle_secrets.

### Model Loading:
- Load the DeepSeek-R1-Distill-Llama-8B model using Unsloth in 4-bit precision.

### Prompt Templates:
- Define system prompts for both inference and training using step-by-step medical reasoning.

### Inference Example:
- Run a test medical question through the model using the defined inference prompt.

### Dataset Preparation:
- Load and preprocess the FreedomIntelligence/medical-o1-reasoning-SFT dataset with chain-of-thought formatting.

### LoRA Fine-Tuning:
- Apply parameter-efficient fine-tuning with LoRA adapters using SFTTrainer.

### Training & Logging:
- Log training metrics to W&B and save outputs.

## 📌 Notes
- Training is limited to 500 examples and 60 steps for quick prototyping. 

- Make sure your GPU supports BF16 for better numerical stability (like T4).

- Use wandb to track training stats in real-time.

- Training took around 35 minutes.

- Used Kaggle T4 GPUs for this task.


## 🛠️ Dependencies

Install required packages using:

```bash
pip install -r requirements.txt
```


