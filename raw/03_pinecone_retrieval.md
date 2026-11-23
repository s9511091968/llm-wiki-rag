# Source 03: Pinecone Learning Center — RAG & Hybrid Search
- **Source**: Pinecone Vector Database Guide
- **URL**: https://www.pinecone.io/learn/retrieval-augmented-generation/
- **Raw Notes**:
  - Embeddings convert text into high-dimensional numerical vectors capturing semantic meaning.
  - Vector search uses Cosine Similarity or Dot Product to find the Top-K closest document chunks to the user's query vector.
  - Hybrid Search combines sparse keyword search (BM25, great for exact terms/IDs) with dense vector search (semantic similarity).
  - Reranking models (Cross-Encoders) take the initial Top-20 retrieved results and re-score them precisely to pass only the top 3-5 chunks to the LLM.