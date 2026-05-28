# DocuMind-AI-RAG
# 📖 DocuMind AI — PDF Question Answering System (RAG-Based)

> An AI-powered PDF Question Answering System built using Retrieval-Augmented Generation (RAG), LangChain, Ollama, and Streamlit.

DocuMind AI allows users to upload PDF documents and ask intelligent context-aware questions using local Large Language Models (LLMs).

---

# 🚀 Features

* 📂 Upload PDF documents
* 🔍 Semantic search over document content
* 🤖 AI-generated answers using Llama 3.1
* ⚡ Fast vector similarity retrieval
* 🧠 RAG-based architecture
* 💾 ChromaDB / FAISS vector storage
* 🖥️ Interactive Streamlit UI
* 🔒 Fully local execution with Ollama

---

# 🛠️ Tech Stack

| Technology       | Purpose           |
| ---------------- | ----------------- |
| Python           | Backend           |
| Streamlit        | Frontend UI       |
| LangChain        | RAG Pipeline      |
| Ollama           | Local LLM Runtime |
| Llama 3.1        | LLM Model         |
| ChromaDB / FAISS | Vector Database   |
| PyPDFLoader      | PDF Parsing       |

---

# 🏗️ System Architecture

```text
                ┌───────────────────┐
                │   Upload PDF      │
                └─────────┬─────────┘
                          │
                          ▼
                ┌───────────────────┐
                │ Extract PDF Text  │
                └─────────┬─────────┘
                          │
                          ▼
                ┌───────────────────┐
                │ Text Chunking     │
                └─────────┬─────────┘
                          │
                          ▼
                ┌───────────────────┐
                │ Create Embeddings │
                └─────────┬─────────┘
                          │
                          ▼
                ┌───────────────────┐
                │ Vector Database   │
                │ Chroma / FAISS    │
                └─────────┬─────────┘
                          │
                          ▼
                ┌───────────────────┐
                │ Similarity Search │
                └─────────┬─────────┘
                          │
                          ▼
                ┌───────────────────┐
                │ Ollama + Llama3.1 │
                └─────────┬─────────┘
                          │
                          ▼
                ┌───────────────────┐
                │ Generated Answer  │
                └───────────────────┘
```

---

# 🔄 Workflow

```text
Upload PDF
    │
    ▼
Extract Text
    │
    ▼
Split into Chunks
    │
    ▼
Generate Embeddings
    │
    ▼
Store in Vector Database
    │
    ▼
Ask Question
    │
    ▼
Retrieve Relevant Chunks
    │
    ▼
Generate AI Response
```

---

# 📂 Project Structure

```bash
documind-ai/
│
├── app.py
├── requirements.txt
├── README.md
│
├── data/
├── vectorstore/
├── utils/
│   ├── loader.py
│   ├── embeddings.py
│   ├── retriever.py
│   └── llm.py
│
└── assets/
```

---

# ⚙️ Installation

## Clone Repository

```bash
git clone https://github.com/mukund7296/documind-ai-rag.git

cd documind-ai
```

## Create Virtual Environment

### Windows

```bash
python -m venv venv

venv\Scripts\activate
```

### Linux / Mac

```bash
python3 -m venv venv

source venv/bin/activate
```

---

# 📦 Install Dependencies

```bash
pip install -r requirements.txt
```

---

# 🤖 Install Ollama

Download:
https://ollama.ai/download

Pull Models:

```bash
ollama pull llama3.1

ollama pull nomic-embed-text
```

---

# ▶️ Run Application

```bash
streamlit run app.py
```

---

# 🌐 Open Browser

```text
http://localhost:8501
```

---

# 💡 Example Questions

* What is the conclusion of the document?
* Summarize this PDF
* What are the key findings?
* Explain chapter 2
* What technologies are mentioned?

---

# 🚀 Future Enhancements

* Multi-PDF support
* Chat history memory
* Source citation highlighting
* Docker deployment
* Authentication
* Hybrid search
* GPU acceleration

---

# 👨‍💻 Author

Mukund Biradar

Python Developer | Gen AI Engineer | RAG Enthusiast

---

# 📜 License

MIT License
