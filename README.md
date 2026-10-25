<div align="center">

# 🤖 Conversational RAG AI Chatbot Assistant

### ⚡ Document Intelligence • Context-Aware Conversational Retrieval • LLaMA 3.3 70B & LangChain

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python" />
  <img src="https://img.shields.io/badge/LangChain-Framework-1C3C3C?style=for-the-badge&logo=chainlink&logoColor=white" alt="LangChain" />
  <img src="https://img.shields.io/badge/Groq%20Cloud-LLaMA%203.3%2070B-F05A28?style=for-the-badge" alt="Groq" />
  <img src="https://img.shields.io/badge/ChromaDB-Vector_Store-FF6F61?style=for-the-badge" alt="ChromaDB" />
  <img src="https://img.shields.io/badge/Streamlit-UI-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white" alt="Streamlit" />
</p>

---

</div>

## 📌 Overview

**Conversational RAG AI Chatbot Assistant** is an advanced Retrieval-Augmented Generation (RAG) platform that enables users to upload custom PDF documents and conduct dynamic, contextual question-answering sessions. Powered by **Groq Cloud's ultra-fast LLaMA 3.3 70B Versatile model**, **ChromaDB vector embeddings**, and **LangChain's history-aware retriever**, the assistant maintains full multi-turn conversational context while delivering grounded, hallucination-free answers directly cited from your files.

---

## 🚀 Key Features

* **📄 Multi-Document PDF Ingestion:** Seamless document loading and parsing powered by `PyMuPDFLoader`.
* **✂️ Recursive Chunking & Semantic Embeddings:** Splitting documents with `RecursiveCharacterTextSplitter` into structured chunks with overlap to maintain semantic continuity.
* **🧠 ChromaDB Vector Store:** Fast, localized vector retrieval with dense embedding indexes.
* **⚡ Ultra-Low Latency Inference:** Powered by Groq's Tensor Streaming Processing Units running `llama-3.3-70b-versatile`.
* **🔄 Contextualized Multi-Turn Chat History:** 
  * History-aware prompt reformulation transforms follow-up questions (e.g. *"What did you mean by that?"*) into self-contained search vectors.
  * Preserves session history across user exchanges using `RunnableWithMessageHistory`.
* **🖥️ Interactive Streamlit Interface:** Modern, user-friendly interface with instant API key entry, file upload progress, and transparent conversational state inspection.

---

## 🛠️ Architecture & Dataflow

```
[Uploaded PDF Files]
       │
       ▼
 [PyMuPDFLoader] ──► [Recursive Character Splitter]
                              │
                              ▼
                       [ChromaDB Vector Store]
                              │
[User Query] ──► [History-Aware Retriever] ◄── [Chat History Memory]
                              │
                              ▼
                 [LLaMA 3.3 70B (via Groq)]
                              │
                              ▼
                     [Grounded Response]
```

---

## ⚙️ Installation & Setup

### 1. Clone the Repository
```bash
git clone https://github.com/bharat-kumaar/AI-Chatbot-Assistant.git
cd AI-Chatbot-Assistant
```

### 2. Create Virtual Environment
```bash
python -m venv venv
# Windows:
venv\Scripts\activate
# Linux/Mac:
source venv/bin/activate
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

### 4. Configure API Keys
Copy `.env.example` to `.env`:
```bash
cp .env.example .env
```
Add your Groq Cloud API key (obtain a free key from [Groq Console](https://console.groq.com)):
```env
GROQ_API_KEY=your_actual_groq_api_key
```

### 5. Launch the Application
```bash
streamlit run app.py
```
Open your web browser at `http://localhost:8501`.

---

## 💡 How to Use

1. Enter your **Groq API Key** in the sidebar or input field.
2. Upload one or multiple **PDF documents**.
3. Type any question regarding the documents.
4. Enjoy real-time, context-aware answers generated directly from your uploaded materials!

---

## 📄 License
This project is open-source under the [MIT License](LICENSE).

---

<p align="center">
  Developed with 🧠 by <a href="https://github.com/bharat-kumaar"><strong>Bharat Kumar</strong></a>
</p>
