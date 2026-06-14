# 🤖 AI Knowledge Assistant

An AI-powered Knowledge Assistant built using **n8n**, **Large Language Models (LLMs)**, **Embeddings**, and **Vector Search**. The system allows users to upload PDF documents and ask questions in natural language. Relevant information is retrieved from the uploaded documents using **Retrieval-Augmented Generation (RAG)**, enabling accurate and context-aware responses based on the document content.

---

## Features

* Upload PDF documents
* Automatic document ingestion and processing
* Text extraction from uploaded documents
* Text chunking for efficient retrieval
* Embedding generation for semantic understanding
* Vector database storage for semantic search
* Retrieval-Augmented Generation (RAG)
* AI-powered question answering
* Source-aware responses based on uploaded documents
* Light/Dark theme toggle
* Workflow automation using n8n

---

## Tech Stack

### Backend & AI

* n8n
* Large Language Model (LLM)
* Embedding Model
* Vector Database
* Retrieval-Augmented Generation (RAG)

---

## How It Works

1. The user uploads a PDF document.
2. The document text is extracted automatically.
3. The extracted text is divided into smaller chunks.
4. Embeddings are generated for each text chunk.
5. The embeddings are stored in a vector database.
6. The user asks a question related to the uploaded document.
7. Relevant document chunks are retrieved through semantic search.
8. The retrieved context is provided to the LLM.
9. The LLM generates an accurate answer based on the retrieved information.

---

## Workflow Architecture

### Document Ingestion Workflow

PDF Document
     │
     ▼
Extract Text
     │
     ▼
Text Splitter
     │
     ▼
Generate Embeddings
     │
     ▼
Store in Vector Database


### Question Answering Workflow

User Query
    │
    ▼
AI Agent
    │
    ▼
Vector Search
    │
    ▼
Retrieve Relevant Chunks
    │
    ▼
Provide Context to LLM
    │
    ▼
Generate Answer
    │
    ▼
Response to User


### System Architecture

┌─────────────────┐
│  PDF Documents  │
└────────┬────────┘
         │
         ▼
┌─────────────────┐
│ Text Extraction │
└────────┬────────┘
         │
         ▼
┌─────────────────┐
│  Text Splitter  │
└────────┬────────┘
         │
         ▼
┌─────────────────┐
│   Embeddings    │
└────────┬────────┘
         │
         ▼
┌─────────────────┐
│ Vector Database │
└────────┬────────┘
         │
         ▼
┌─────────────────┐
│    AI Agent     │
│      (LLM)      │
└────────┬────────┘
         │
         ▼
┌─────────────────┐
│ Generated Answer│
└─────────────────┘


---

## Use Cases

* Academic document analysis
* Research paper querying
* Knowledge base assistants
* Internal company documentation search
* Intelligent document retrieval
* AI-powered learning assistants

---

## Future Improvements

* Multi-document support
* Conversation history
* Enhanced source citations
* Support for DOCX and TXT files
* Cloud deployment
* Improved document management
* Multi-user support

---

## Author

**Swanandi Kawade**
Computer Engineering Student
Passionate about Artificial Intelligence, Automation, and Software Development.
