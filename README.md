# 💬 Langflow-Powered Customer Support Agent

This project demonstrates how to build a **context-aware customer support agent** using **Langflow** and **RAG (Retrieval-Augmented Generation)**. The agent answers user queries by retrieving relevant context from a custom documentation corpus, combining it with the power of LLMs (e.g., Gemini or OpenAI) for accurate and personalized responses.

---

## 🧠 Features

- ✅ **Retrieval-Augmented Generation (RAG)**: Answers are grounded in real company documentation.
- 🧩 **Langflow Integration**: Modular, visual agent workflow built using Langflow's drag-and-drop interface.
- ⚡ **FastAPI Backend**: Lightweight API to interact with the chatbot pipeline.
- 📄 **Document Indexing**: PDF ingestion, chunking, and embedding into a vector store.
- 💡 **Prompt Engineering**: Designed prompts to guide the LLM for tone, relevance, and format.

---

## 🛠️ Tech Stack

- **Langflow** – For LLM workflow orchestration  
- **ChromaDB** – Lightweight vector store for document retrieval  
- **OpenAI/Gemini APIs** – LLM for text generation  
- **FastAPI** – Backend service to serve the agent  
- **PyMuPDF / Unstructured** – PDF parsing and document preprocessing  
- **Langchain** – RAG and embedding pipeline

---

## 🚀 How It Works

1. **Document Upload**: PDFs or text files containing support docs are parsed and chunked.
2. **Embedding + Storage**: Text chunks are embedded and stored in ChromaDB.
3. **Query Input**: User submits a question via the frontend or API.
4. **Context Retrieval**: Top-k relevant chunks are retrieved from the vector DB.
5. **LLM Generation**: Retrieved context is passed to the LLM with a formatted prompt.
6. **Response Delivery**: Final answer is returned to the user via FastAPI.

---

## 📦 Setup Instructions

```bash
# Clone the repo
git clone https://github.com/ShresthJn19/Langflow-Customer-Support-Agent.git
cd Langflow-Customer-Support-Agent

# (Optional) Set up a virtual environment
python -m venv venv
source venv/bin/activate  # or venv\Scripts\activate on Windows

# Install dependencies
pip install -r requirements.txt
```

---

## 🧪 Run the App
```bash
# Start the FastAPI server
uvicorn main:app --reload
```

---

## 📚 Example Use Case

**User:** “How can I reset my password if I forgot my security questions?”
**Agent:** “You can reset your password by clicking on ‘Forgot Password’ and choosing ‘Verify via email’. If you do not have access to your email, contact support with your account ID.”

---

## 🧩 Langflow UI

A visual workflow is set up using Langflow for better debugging, prompt tweaking, and component-level control.
