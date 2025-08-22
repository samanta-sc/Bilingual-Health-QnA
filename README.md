# 🏥 Bilingual Health QnA (Bengali + English)

An AI-powered **health question-answering system** that supports both **Bengali** and **English** queries.  
Built on top of **Llama-3.2-3B-Instruct (Unsloth)** with **LoRA fine-tuning**, this project enables multilingual healthcare assistance with optimized performance and API deployment.

---

## 🚀 Project Highlights
- **Model**: `unsloth/Llama-3.2-3B-Instruct`  
- **LoRA Fine-tuning**: Efficient training with low-rank adaptation  
- **Bilingual Support**: Automatically detects question language (Groq API + Deepseek model)  
- **Dataset Sources**:
  - [Medical Customer Care (English)](https://huggingface.co/datasets/DR-DRR/Medical_Customer_care)  
  - [Doctor QA Bangla](https://huggingface.co/datasets/shetumohanto/doctor_qa_bangla)  
- **Performance**: Achieved **validation loss: 0.74**  
- **Deployment**: FastAPI + ngrok, tested with Postman  
- **Environment**: Trained on Kaggle GPU  

---

## ⚙️ Config

**Model Config(Default):** 
```python
max_seq_length = 2048
load_in_4bit = True
lora_alpha = 16
lora_dropout = 0
target_modules = ["q_proj","k_proj","v_proj","o_proj","gate_proj","up_proj","down_proj"]
use_gradient_checkpointing = "unsloth"
```

**SFTConfig:**  
  - `learning_rate = 2e-5`  
  - `num_train_epochs = 6`  
  - `per_device_train_batch_size = 8`  
  - `evaluation_strategy = "epoch"` 
