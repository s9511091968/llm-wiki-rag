# Source 05: RAGAs Documentation — Core Evaluation Metrics
- **Source**: RAGAs Evaluation Framework
- **URL**: https://docs.ragas.io/en/stable/concepts/metrics/available_metrics/
- **Raw Notes**:
  - Evaluating a RAG pipeline requires measuring both the Retriever and the Generator (known as the RAG Triad):
    1. Context Relevance / Precision: Are the retrieved chunks actually relevant to the user's query without too much noise?
    2. Faithfulness (Groundedness): Is the generated answer factually consistent with the retrieved context (zero hallucination)?
    3. Answer Relevance: Does the final answer directly and completely address the user's question?