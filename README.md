# AskDocs-AI---PDF-Based-Retrieval-Augmented-Generation-System

AskDocs-AI is a practical Retrieval-Augmented Generation (RAG) project focused on answering questions from PDFs and related document sources using modern LLM and vector-search workflows. The repository brings together experiments in document ingestion, chunking, embeddings, vector database storage, evaluation, deployment, and multimodal PDF understanding.

## Overview

The project demonstrates how to build an AI-powered document Q&A system that can:

- ingest PDF files and extract textual content
- split large documents into retrievable chunks
- convert chunks into embeddings
- store and query them with vector databases
- use LLMs to generate grounded answers from retrieved context
- support experimentation with evaluation, web content, SQL-based retrieval, and deployment interfaces

This repository is designed as a learning and experimentation space for PDF-based, retrieval-augmented AI systems.

## Core Features

- PDF document processing and text extraction
- Chunk-based document segmentation
- Embedding generation with OpenAI and related frameworks
- FAISS-based similarity search
- Retrieval-augmented answer generation using LangChain
- multimodal PDF handling for images and tables
- web-based and app-based demos with Streamlit and Gradio
- evaluation workflows using RAGAS and SQL-backed document exploration

## Repository Structure

- `2_vector_db/` – vector database experiments and embedding storage patterns
- `3_building_simple_rag_pipeline/` – foundational RAG pipeline implementations
- `4_advanced_RAG/` – advanced retrieval and query enhancement experiments
- `5_RAG_Evaluation/` – evaluation pipelines and quality testing
- `6_sql_rag/` – SQL-aware RAG and database integration work
- `7_multimedia_pdf/` – PDF extraction with tables, images, and multimodal Q&A
- `8_deploying_st_app/` – Streamlit deployment app for website/document querying
- `9_prompt_caching/` – prompt optimization and caching examples
- `10_other_experimentation/` – additional exploratory notebooks and scripts
- `Requirements.txt` – Python dependencies for the project
- `tesla_motors_data.db` – sample database used in SQL/RAG workflows

## Tech Stack

- Python
- LangChain
- OpenAI API / LLM integration
- FAISS
- PDF parsing libraries (`PyPDF2`, `pymupdf`, `pdfplumber`)
- Streamlit and Gradio for interfaces
- SQLAlchemy and SQLite for data-backed workflows
- Sentence-transformers and vector-search tooling

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/tamaxhh/AskDocs-AI---PDF-Based-Retrieval-Augmented-Generation-System.git
cd AskDocs-AI---PDF-Based-Retrieval-Augmented-Generation-System
```

### 2. Create a virtual environment

```bash
python -m venv .venv
source .venv/bin/activate   # On macOS/Linux
.venv\Scripts\activate      # On Windows
```

### 3. Install dependencies

```bash
pip install -r Requirements.txt
```

### 4. Configure environment variables

Create a `.env` file in the project root and add your API key, for example:

```env
OPENAI_API_KEY=your_openai_api_key_here
```

If you are using other providers or services, you may also need to configure additional environment values depending on the script you run.

## Example Usage

### PDF-based Q&A app

Run the multimodal PDF Q&A demo:

```bash
python 7_multimedia_pdf/project.py
```

This script processes uploaded PDFs, extracts text, images, and tables, builds embeddings, and answers questions using a retrieval pipeline.

### Streamlit app

Run the website/document chatbot demo:

```bash
streamlit run 8_deploying_st_app/streamlit_app_chatbot.py
```

This app lets you input a URL or document and ask questions based on the scraped or extracted content.

## Project Goals

This repository is intended to help users learn and prototype the following:

- document-aware LLM applications
- retrieval and ranking for unstructured data
- embedding generation and vector storage
- grounding AI answers in source documents
- end-to-end pipeline design for RAG systems

## Notes

This project is an experimental codebase with multiple modules that illustrate different stages of building RAG systems. Some folders contain prototype scripts, notebooks, and deployment examples rather than a single production-ready app.

## Future Directions

Potential extensions include:

- production-grade PDF ingestion pipeline
- better chunking and reranking strategies
- support for more document formats
- deployment with Docker and cloud hosting
- user authentication and file management
- enterprise search and indexing improvements

## Contributing

Contributions, improvements, and experiments are welcome. If you are extending the repository, keep the existing structure consistent and document any new scripts or workflows clearly.
