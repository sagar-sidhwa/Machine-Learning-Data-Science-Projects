# 🩺 LLM + RAG Powered Medical Transcription Summarizer

This project uses **Large Language Models (LLMs)** and **Retrieval-Augmented Generation (RAG)** to build a smart medical assistant that **summarizes patient transcription records**.

### 💡 Objective
Enable doctors and nurses to **automatically receive summaries** of patient histories before check-ups using previously recorded descriptions and transcriptions.

---

## 📚 Dataset
**Source:** [Kaggle – Medical Transcription Samples]  
**Rows:** ~4,999  
**Key Columns:**
- `description`: Patient complaint or initial report
- `transcription`: Full check-up notes
- `medical_specialty`: Field of medicine
- `keywords`: Tags (may be incomplete)

---

## 🧠 Techniques Used

### ✅ 1. Baseline LLM Summarization
- Summarized using GPT-based model over each row independently.

### ✅ 2. RAG (Retrieval-Augmented Generation)
- **Step 1:** Text embedding using `sentence-transformers`
- **Step 2:** Vector store with FAISS
- **Step 3:** Query + Retrieve + LLM Summarization
- **Outcome:** Intelligent summaries using historical patient context

---

## 🔧 Libraries
- `sentence-transformers`
- `faiss`
- `openai` (or HuggingFace `transformers`)
- `pandas`, `matplotlib`, `seaborn`

---

## 🧪 Future Enhancements
- Fine-tune small LLMs (Phi, GPT4All) on domain-specific context.
- Build a web app for real-time hospital assistant.
- Add doctor’s notes into the vector DB for more accurate predictions.

---

## 📌 Conclusion
This project demonstrates the **power of combining LLMs + Vector Search** for the medical domain. It offers a foundational system for **automated patient health summarization** and opens doors for real-time clinical AI tools.

---
