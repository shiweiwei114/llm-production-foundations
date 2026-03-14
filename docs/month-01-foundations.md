# 📅 Month 1 – Foundations of Applied AI Engineering

## 🎯 Objective

Build a strong conceptual and practical foundation for working with large language models (LLMs) in production environments.

This month focuses on understanding how modern LLMs work at a conceptual level and implementing a production-style API service that integrates with a hosted model provider.

---

## 🧠 Core Concepts Covered

### 1. Large Language Models (LLMs)
- Pretraining vs fine-tuning
- Context windows
- Sampling strategies (temperature, top-p)
- Prompt structure and response behavior

### 2. Transformers (Intuition-Level Understanding)
- Self-attention mechanism
- Why transformers replaced RNNs
- How models process tokens in parallel

### 3. Tokenization
- What is a token?
- How token count impacts cost
- Context length limits and truncation strategies

### 4. Embeddings (Introductory Level)
- What embeddings represent
- Why vector representations matter
- Preview of retrieval-based systems (RAG in Month 2)

---


## 📊 Engineering Focus

Unlike demo-level AI projects, this implementation emphasizes:

- Separation of concerns (LLM client abstraction)
- Cost-awareness in model usage
- Observability and structured logging
- Configuration via environment variables
- Clean API design using FastAPI

The goal is to treat LLM integration as a backend system component, not a novelty feature.

---

## 📚 Resources Used

- DeepLearning.AI – Generative AI with LLMs
- OpenAI API documentation
- "The Illustrated Transformer" – Jay Alammar
- Transformer explanation videos (attention intuition)

---

## ✅ Month 1 Completion Criteria

- Able to clearly explain transformer architecture at a conceptual level
- Understand tokenization and cost implications
- Successfully built and tested LLM API service
- Docker container builds and runs locally
- Token usage and cost are logged per request

---

## 🔭 Next Steps (Month 2 Preview)

- Text embeddings
- Vector similarity search
- Retrieval-Augmented Generation (RAG)
- Integration with vector databases
