# Task 9: LangGraph Reasoning System

This project demonstrates how to integrate a symbolic knowledge base with LangGraph to perform logical inference using retrieval-augmented generation (RAG) and chain-of-thought reasoning.

## Overview

- A small Prolog-style knowledge base was created, including facts (e.g., `animal(sparrow)`) and rules (e.g., `bird(X) :- animal(X), flies(X)`).
- The knowledge base was converted to LangChain `Document` objects and embedded using HuggingFace sentence transformers.
- FAISS was used to index and retrieve relevant chunks.
- A LangGraph state graph was built to:
  - Retrieve context
  - Judge its relevance
  - Apply a basic chain-of-thought reasoning step

## Sample Output

```
Query: Can a sparrow fly?

Chain of Thought Reasoning:
Step 1: Examine retrieved context...
animal(sparrow).
flies(sparrow).
→ Reasoning: The fact 'flies(sparrow)' exists, so yes, it can fly.
```

## How to Run

1. Open the notebook or script in Google Colab
2. Install dependencies:
   ```bash
   pip install langchain langgraph faiss-cpu sentence-transformers
   ```
3. Run all cells in sequence

## Repository Contents

- `task9_langgraph.py`: Script implementation
- `Task_9_LangGraph.ipynb`: Notebook with runnable steps and outputs
- `Task_9_LangGraph_Writeup.pdf`: Final one-page deliverable
- `README.md`: Project overview and instructions

## Repository

https://github.com/suvalavala/task9_LangGraph
