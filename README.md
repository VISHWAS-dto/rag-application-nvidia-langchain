# RAG Chatbot with NVIDIA & LangChain

A RAG-based chatbot that answers questions from your own documents using LangChain and NVIDIA AI Endpoints.
Supports PDF & text ingestion, semantic search via ChromaDB, and response generation with Mistral-Nemotron.

---

## Features

- 📄 Load and parse **PDF and text documents**
- ✂️ Smart document chunking with `RecursiveCharacterTextSplitter`
- 🧠 Semantic embeddings via **NVIDIA AI Endpoints**
- 🗃️ Vector storage and retrieval using **ChromaDB**
- 💬 Conversational Q&A powered by **Mistral-Nemotron** (via NVIDIA)
- 🔐 Secure API key management with `.env`

---

## Tech Stack

| Tool | Purpose |
|---|---|
| LangChain | Document loading, chaining, prompts |
| NVIDIA AI Endpoints | LLM (Mistral-Nemotron) + Embeddings |
| ChromaDB | Vector store for semantic search |
| Python-dotenv | Environment variable management |

---

## Setup & Installation

### 1. Clone the repository
```bash
git clone https://github.com/YOUR_USERNAME/rag-chatbot-nvidia-langchain.git
cd rag-chatbot-nvidia-langchain
```

### 2. Create a virtual environment
```bash
python -m venv .venv
source .venv/bin/activate        # On Windows: .venv\Scripts\activate
```

### 3. Install dependencies
```bash
pip install langchain langchain-community langchain-nvidia-ai-endpoints langchain-text-splitters chromadb pypdf python-dotenv
```

### 4. Set up your `.env` file
Create a `.env` file in the root directory:
```
NVIDIA_API_KEY=your_nvidia_api_key_here
```

> 🔑 Get your free NVIDIA API key at [build.nvidia.com](https://build.nvidia.com)

---

## Usage

Open and run the notebook:
```bash
jupyter notebook main.ipynb
```

Once running, the chatbot will prompt you to enter questions. Type `0` to exit.

```
You: What is the document about?
Ai: The document covers ...

You: 0   ← exit
```

---

## Project Structure

```
rag-chatbot-nvidia-langchain/
│
├── main.ipynb        # Main RAG chatbot notebook
├── .env              # API keys (DO NOT commit this)
├── .gitignore        # Ignores .env, venv, cache, etc.
└── README.md         # Project documentation
```

---

## ecurity Note

Never commit your `.env` file. Make sure your `.gitignore` includes:
```
.env
.venv/
__pycache__/
chroma_db/
```

---

## Author 
Vishwas


