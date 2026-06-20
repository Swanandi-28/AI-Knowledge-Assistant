# 🤖 AI Knowledge Assistant

**An AI-powered Knowledge Assistant built using *n8n, AI Agents, Pinecone Vector Database, Cohere Embeddings, and Large Language Models (LLMs)**. The system allows users to upload PDF documents and ask questions in natural language. Relevant information is retrieved from the uploaded documents using **Retrieval-Augmented Generation (RAG)**, enabling accurate and context-aware responses based on the document content.

---

## Features

* Automatic document ingestion and processing — Upload documents and automatically process them into a searchable knowledge base.
* Intelligent Text Chunking – Splits large documents into optimized chunks for efficient retrieval and improved response quality.
* Semantic Embedding Generation – Converts document content into vector embeddings using AI-powered embedding models.
* Embedding generation for semantic understanding
* Vector Database Integration – Stores embeddings in Pinecone for fast and scalable semantic search.
* Retrieval-Augmented Generation (RAG) - Retrieves relevant document context before generating responses, ensuring accurate and grounded answers.
* AI-powered question answering – Uses an AI Agent to reason, retrieve knowledge, and generate context-aware responses.
* Source-aware responses based on uploaded documents – Generates answers based on retrieved document content rather than relying solely on the language model.
* Workflow automation using n8n – End-to-end automation for document ingestion, retrieval, memory management, and response generation.

---

## Tech Stack

### Backend & AI

```text

| Layer           | Technology        | Purpose                             |
| --------------- | ----------------- | ----------------------------------- |
| Automation      | n8n Cloud         | Workflow orchestration              |
| AI Agent        | n8n AI Agent      | Query processing and tool execution |
| LLM             | OpenRouter        | Response generation                 |
| Embeddings      | Cohere Embeddings | Semantic vector generation          |
| Vector Database | Pinecone          | Knowledge storage and retrieval     |
| Memory          | n8n Simple Memory | Conversational context              |

```

## How It Works

1. The user uploads a document to the knowledge base.
2. The document is processed through an n8n ingestion workflow.
3. The document content is extracted and converted into text.
4. The extracted text is divided into smaller chunks for efficient retrieval.
5. Semantic embeddings are generated for each text chunk using an embedding model.
6. The embeddings are stored in the Pinecone Vector Database.
7. The user submits a question through the AI Knowledge Assistant.
8. The Chat Trigger sends the query to the AI Agent.
9. The AI Agent retrieves relevant document chunks from Pinecone using semantic search.
10. Previous conversation context is retrieved from Simple Memory for follow-up questions.
11. The retrieved knowledge and conversation context are provided to the Large Language Model (LLM).
12. The AI Agent generates a context-aware response grounded in the uploaded documents.
13. The final answer is returned to the user in natural language.


---

### System Architecture

```text
┌───────────────────────────────────────────────────────────────┐
│                           USER                                │
└───────────────────────┬───────────────────────┬───────────────┘
                        │                       │
                        │ Upload Document       │ Ask Question
                        ▼                       ▼

┌───────────────────────────────────────────────────────────────┐
│                     n8n Cloud Workflows                       │
│                                                               │
│  ┌─────────────────────────────┐  ┌────────────────────────┐ │
│  │ Workflow 1: Document        │  │ Workflow 2: Knowledge  │ │
│  │ Ingestion                   │  │ Retrieval & QA         │ │
│  │                             │  │                        │ │
│  │ Webhook Trigger             │  │ Chat Trigger           │ │
│  │          ↓                  │  │        ↓               │ │
│  │ Default Data Loader         │  │     AI Agent           │ │
│  │          ↓                  │  │        ↓               │ │
│  │ Recursive Character         │  │  Pinecone Retrieval    │ │
│  │ Text Splitter               │  │       Tool             │ │
│  │          ↓                  │  │        ↓               │ │
│  │ Cohere Embeddings           │  │  Simple Memory         │ │
│  │          ↓                  │  │  (Conversation Context)│ │
│  │ Pinecone Vector Store       │  │        ↓               │ │
│  │ (Insert Documents)          │  │ OpenRouter Chat Model  │ │
│  └─────────────────────────────┘  └────────────────────────┘ │
└──────────────────────────────┬────────────────────────────────┘
                               │
                               ▼

                    ┌──────────────────────┐
                    │ Pinecone Vector DB   │
                    │                      │
                    │ Knowledge Storage    │
                    │ & Semantic Retrieval │
                    └──────────┬───────────┘
                               │
                               ▼

                    ┌──────────────────────┐
                    │ OpenRouter LLM       │
                    │                      │
                    │ Response Generation  │
                    └──────────┬───────────┘
                               │
                               ▼

                    ┌──────────────────────┐
                    │ Generated Answer     │
                    └──────────────────────┘
```

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

