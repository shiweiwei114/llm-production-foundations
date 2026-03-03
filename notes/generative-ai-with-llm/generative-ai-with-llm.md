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