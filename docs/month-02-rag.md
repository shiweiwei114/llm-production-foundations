# Month 2 – Retrieval-Augmented Generation (RAG)

## Objective

The objective of Month 2 is to extend the foundational LLM API service built in Month 1 into a **retrieval-augmented AI system** capable of incorporating external knowledge sources.

Instead of relying solely on a model’s pretrained knowledge, this phase introduces a **Retrieval-Augmented Generation (RAG) pipeline** that retrieves relevant documents from a vector database and injects them into the prompt context before generation.

This improves:

- factual accuracy
- domain knowledge coverage
- controllability of model responses

The goal is to understand and implement the **core architecture used in many real-world AI applications**, including AI assistants, knowledge-base search, and enterprise copilots.

---

## Core Concepts Covered

This phase explores the essential building blocks of modern LLM-powered systems.

### Embeddings
Text embeddings convert text into high-dimensional vector representations that capture semantic meaning. These vectors allow similarity comparisons between queries and documents.

Key concepts explored:

- semantic similarity
- cosine similarity
- embedding models
- vector representations of text

### Vector Search

Vector databases store embeddings and enable efficient similarity search.

Topics covered:

- nearest neighbor search
- top-k retrieval
- approximate nearest neighbor (ANN) indexing
- metadata filtering

### Document Ingestion

Raw documents must be processed before retrieval.

This includes:

- loading documents
- chunking text into manageable segments
- generating embeddings
- storing embeddings in a vector index

### Retrieval-Augmented Generation (RAG)

RAG integrates retrieval and generation to produce grounded responses.

Pipeline:
User Query
↓
Embedding
↓
Vector Search
↓
Relevant Documents Retrieved
↓
Prompt Augmentation
↓
LLM Response


This architecture allows LLMs to access **external knowledge bases without retraining**.

---

## Engineering Focus

This phase emphasizes **AI system engineering rather than model training**.

The implementation focuses on:

### Modular Architecture

The RAG system is structured into reusable modules:
rag/
embeddings.py
vector_store.py
ingest.py
retriever.py
rag_pipeline.py


Each module handles a specific stage of the retrieval pipeline.

### Data Ingestion Pipeline

A simple ingestion workflow processes raw documents and indexes them in the vector database.

Key components:

- document loaders
- embedding generation
- vector storage

### Retrieval Layer

The retriever identifies the most relevant document chunks for a given query using vector similarity search.

### Prompt Augmentation

Retrieved context is injected into the prompt before sending the request to the language model.

This grounds the model’s responses in **external knowledge sources**.

### Production-Oriented Design

The system is designed with production considerations such as:

- logging
- modular services
- extensibility for future improvements
- clear separation between retrieval and generation logic

---

## Resources Used

The following learning materials were used to guide the design and implementation of the RAG system.

### Engineering Guides

- Pinecone Learning Center – Retrieval-Augmented Generation
- Microsoft RAG Architecture Guidance
- OpenAI Cookbook (embeddings and retrieval examples)

### Technical Documentation

- Chroma Vector Database documentation
- OpenAI Embeddings API documentation

### System Design Learning

- Full Stack Deep Learning – LLM application architecture
- Industry blog posts on RAG system design and retrieval pipelines

These resources provided practical guidance on building **production-style LLM systems rather than simple demos**.


## Next Steps

Future improvements for this system include:

- advanced document chunking strategies
- hybrid search (keyword + vector)
- reranking models
- evaluation pipelines for retrieval quality


