# PDF RAG Chatbot

# PDF RAG Chatbot

A simple Retrieval-Augmented Generation (RAG) chatbot built with LangChain, Google Gemini, ChromaDB, and HuggingFace Embeddings. The chatbot allows users to upload a PDF document and ask questions based on its contents.

---

## Features

* Load PDF documents
* Split documents into chunks
* Generate embeddings using Sentence Transformers
* Store embeddings in ChromaDB
* Retrieve relevant context from the PDF
* Generate answers using Gemini 2.5 Flash
* Simple command-line interface

---

## Tech Stack

* Python
* LangChain
* Google Gemini
* ChromaDB
* HuggingFace Embeddings
* PyPDF

---

## Installation

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/pdf-rag-chatbot.git
cd pdf-rag-chatbot
```

### 2. Create a Virtual Environment

```bash
python -m venv venv
```

Activate the environment:

**Windows**

```bash
venv\Scripts\activate
```

**Linux/macOS**

```bash
source venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install langchain langchain-google-genai langchain-community langchain-text-splitters chromadb sentence-transformers pypdf torch
```

### 4. Configure Gemini API Key

**PowerShell**

```powershell
$env:GOOGLE_API_KEY="YOUR_GEMINI_API_KEY"
```

Verify:

```powershell
python -c "import os; print(bool(os.getenv('GOOGLE_API_KEY')))"
```

Expected output:

```text
True
```

---

## Project Structure

```text
pdf-rag-chatbot/
│
├── app.py
├── README.md
└── sample.pdf
```

---

## Running the Application

Start the chatbot:

```bash
python app.py
```

Example:

```text
Enter PDF path: sample.pdf

Ask a question (or type 'exit'): What is this document about?

Answer:
This document discusses...
--------------------------------------------------

Ask a question (or type 'exit'): exit
```

---

## How It Works

1. Loads the PDF document.
2. Splits the document into smaller chunks.
3. Converts text chunks into vector embeddings.
4. Stores embeddings in a vector database.
5. Retrieves the most relevant content for a user query.
6. Sends the retrieved context to Gemini.
7. Generates an answer based on the document content.

---

## Future Enhancements

* Streamlit Web Interface
* Multiple PDF Support
* Persistent Vector Database
* Chat History
* Source Citations
* Hybrid Search
* Agentic RAG Workflows

---

## License

MIT License

Feel free to fork, modify, and use this project for learning, experimentation, and personal projects.
