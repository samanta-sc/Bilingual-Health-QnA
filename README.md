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

## 💡 Inference & Generation

- <b>Language Detection:</b> Groq API + Deepseek

- <b>English Generation:</b>
```python
max_new_tokens=128, temperature=0.1, min_p=0.1
```

- <b>Bengali Generation:</b>
```python
max_new_tokens=256, temperature=0.1, min_p=0.1
```
  - Repetition handled via unique sentence filtering.

---

## 🌐 API Exposure

- Built with <b>FastAPI</b>
- Exposed via <b>ngrok</b>
- Tested with <b>Postman</b>

---

## 📊 Results

✅ Bilingual support (Bengali + English) <br>
✅ Validation loss: 0.74 <br>
✅ Stable inference with low temperature <br>
✅ Deployed as REST API <br>
