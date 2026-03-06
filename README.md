# 🏥 Medical Research Q&A Agent
### Retrieval-Augmented Generation (RAG) for Public Health Q&A

**Built by Vasundhara Baligar | UMass Amherst MS CS**

[![Python](https://img.shields.io/badge/Python-3.10+-blue)](https://python.org)
[![LangChain](https://img.shields.io/badge/LangChain-0.3+-green)](https://langchain.com)
[![FAISS](https://img.shields.io/badge/FAISS-Vector%20Search-orange)](https://faiss.ai)
[![Gradio](https://img.shields.io/badge/Gradio-UI-red)](https://gradio.app)

---

## 📌 Overview

An intelligent Medical Q&A system that answers clinical and public health questions using **Retrieval-Augmented Generation (RAG)**. The system retrieves relevant context from a real medical dataset and generates accurate, grounded answers — without hallucinating information.

This project demonstrates:
- End-to-end RAG pipeline design
- Semantic search using FAISS vector store
- LLM integration with LangChain
- Interactive web deployment with Gradio

---

## 🏗️ Architecture

```
User Question
     ↓
[Embedding Model] → Convert question to vector
     ↓
[FAISS Vector Store] → Retrieve top-3 most relevant medical Q&A pairs
     ↓
[TinyLlama LLM] → Generate answer grounded in retrieved context
     ↓
[Gradio UI] → Display answer to user
```

---

## 🛠️ Tech Stack

| Component | Technology |
|---|---|
| Language | Python 3.10+ |
| RAG Framework | LangChain |
| Embedding Model | sentence-transformers/all-MiniLM-L6-v2 |
| Vector Store | FAISS |
| LLM | TinyLlama-1.1B-Chat |
| Dataset | medalpaca/medical_meadow_medqa (500 pairs) |
| UI | Gradio |
| Platform | Google Colab (A100 GPU) |

---

## 📊 Dataset

- **Source:** [medalpaca/medical_meadow_medqa](https://huggingface.co/datasets/medalpaca/medical_meadow_medqa)
- **Size:** 500 real medical Q&A pairs
- **Domain:** Clinical medicine, pharmacology, public health
- **Chunks:** 1,508 text chunks indexed in FAISS

---

## 🚀 How to Run

### Option 1: Google Colab (Recommended)
1. Open `Medical-RAG-QA-Agent.ipynb` in Google Colab
2. Set runtime to **GPU (A100 preferred)**
3. Run all cells in order
4. Click the Gradio public URL to use the app

### Option 2: Local Setup
```bash
# Clone the repo
git clone https://github.com/yourusername/medical-rag-qa-agent.git
cd medical-rag-qa-agent

# Install dependencies
pip install -r requirements.txt

# Run the notebook
jupyter notebook Medical-RAG-QA-Agent.ipynb
```

---

## 💡 Example Questions

- *"What antibiotic treats UTI in pregnant women?"*
- *"What are the symptoms of diabetes?"*
- *"What is the first-line treatment for hypertension?"*
- *"What causes anemia?"*

---

## 📁 Project Structure

```
medical-rag-qa-agent/
│
├── Medical-RAG-QA-Agent.ipynb   # Main notebook
├── requirements.txt              # Dependencies
└── README.md                     # This file
```

---

## 🔑 Key Concepts Demonstrated

- **Retrieval-Augmented Generation (RAG):** Grounds LLM answers in real data
- **Semantic Search:** FAISS indexes 1,508 medical text chunks for fast similarity search
- **Embedding Model:** sentence-transformers converts text to dense vectors
- **LangChain LCEL:** Modern pipeline chaining for RAG
- **Gradio Deployment:** One-click shareable web UI

---

## 🔮 Future Work

- Fine-tune the embedding model on medical terminology
- Add PDF upload feature for custom medical documents
- Integrate larger LLM (Mistral-7B) for better answer quality
- Add JavaScript frontend for DS4CG-style dashboard
- Deploy permanently on Hugging Face Spaces

---

## 📬 Contact

**Vasundhara Vishwanath Baligar**
- Email: vbaligar@umass.edu
- [LinkedIn](https://linkedin.com) | [GitHub](https://github.com) | [Portfolio](https://portfolio.com)
