# Generative AI with LLMs

## Overview

This document covers fundamental concepts of Large Language Models (LLMs) and transformer architecture.

## Transformers Architecture

### Key Paper
- **[Attention is All You Need](https://arxiv.org/abs/1706.03762)** - The foundational paper introducing the Transformer architecture

### Components

#### Encoder
- Encodes input prompts with contextual understanding
- Produces one vector per input token
- Captures semantic meaning and relationships between tokens

#### Decoder
- Accepts input tokens to start generation
- Generates new tokens sequentially
- Produces the output text one token at a time

## Key Concepts

- **Attention Mechanism**: Allows the model to focus on relevant parts of the input when processing each token
- **Tokenization**: Breaking down text into tokens (subword units)
- **Contextual Understanding**: Ability to understand meaning based on surrounding context

## Fine-Tuning

### What is Fine-Tuning?
Fine-tuning involves providing many examples of input prompts paired with desired completions—significantly more than few-shot strategies. This approach adapts a pre-trained model to specific use cases.

### Challenges

#### Catastrophic Forgetting
Fine-tuning on a single task can cause the model to lose performance on other tasks it previously understood well.

**Impact**: While fine-tuning can significantly increase performance on a specific task, it may reduce the model's ability to perform well on other tasks.

### Solutions to Avoid Catastrophic Forgetting

> **Note**: You might not need to implement these if single-task performance is your goal.

1. **Multi-task Fine-tuning**: Train on multiple tasks simultaneously to maintain broader capabilities
2. **Parameter Efficient Fine-tuning (PEFT)**: Update only a small subset of parameters instead of the entire model

### Parameter Efficient Fine-tuning (PEFT)

Parameter Efficient Fine-tuning maintains the original model weights while training only a small set of new parameters.

#### LoRA (Low Rank Adaptation)
- Freezes most of the original LLM weights
- Injects 2 rank decomposition matrices alongside the original weights
- Trains only the weights of the smaller matrices
- Highly efficient in terms of parameters and memory

#### Prompt Tuning
- Adds trainable "soft prompts" to the input
- Keeps all model weights frozen
- Optimizes the prompt embeddings during training