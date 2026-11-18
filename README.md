# Enterprise RAG Assistant with Hybrid Search and Reranking

An AI-powered document question-answering system that uses Retrieval-Augmented Generation (RAG) to retrieve relevant information from PDF and text documents and generate context-aware answers.

## Overview

This project implements an end-to-end RAG pipeline combining dense vector search, BM25 keyword search, and cross-encoder reranking to improve document retrieval accuracy and answer relevance.

## Key Features

- PDF and text document ingestion
- Text preprocessing and configurable chunking
- Dense vector embeddings
- Semantic search using FAISS
- BM25 keyword-based retrieval
- Hybrid search combining semantic and keyword retrieval
- Cross-encoder reranking
- Context-aware LLM response generation
- Source attribution and document references
- Retrieval and response evaluation
- REST API using FastAPI

## Tech Stack

| Category | Technologies |
|---|---|
| Language | Python |
| LLM Framework | LangChain |
| Embeddings | Hugging Face |
| Vector Database | FAISS |
| Retrieval | BM25, Semantic Search |
| Reranking | Cross-Encoder |
| API | FastAPI |
| Deployment | Docker |

## Architecture

1. Document Ingestion – Load PDF and text documents.
2. Preprocessing – Clean, split, and chunk documents.
3. Embedding Generation – Convert document chunks into vector embeddings.
4. Hybrid Retrieval – Retrieve relevant chunks using semantic and keyword search.
5. Reranking – Reorder retrieved results using a cross-encoder.
6. Answer Generation – Generate responses using retrieved context and an LLM.
7. Evaluation – Measure retrieval recall, MRR, answer faithfulness, and latency.

## Project Structure

```text
enterprise-rag-assistant/
├── app/
│   ├── ingestion.py
│   ├── preprocessing.py
│   ├── embeddings.py
│   ├── retrieval.py
│   ├── reranking.py
│   └── generation.py
├── evaluation/
│   └── evaluate.py
├── data/
├── tests/
├── screenshots/
├── main.py
├── requirements.txt
├── Dockerfile
├── .gitignore
└── README.md
```

## Evaluation Metrics

- Recall@K
- Mean Reciprocal Rank (MRR)
- Answer Faithfulness
- Response Latency

The project benchmark described in my portfolio work improved Recall@5 from 71% to 81% compared with a vector-only retrieval baseline on a 150-question evaluation dataset.

## Installation

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
cd enterprise-rag-assistant

python -m venv venv
pip install -r requirements.txt
```

## Future Improvements

- Add conversational memory
- Integrate multiple LLM providers
- Add advanced retrieval evaluation
- Deploy using Docker
- Build an interactive Streamlit interface

## Author

**Lakshmi Tripura**

AI/ML Engineer | Generative AI | LLMs | RAG | AI Agents | MLOps
