# Source 01: Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks
- **Authors**: Patrick Lewis et al. (Facebook AI Research, 2020)
- **URL**: https://arxiv.org/abs/2005.11401
- **Raw Notes**:
  - Large pre-trained language models store factual knowledge in their parameters (Parametric Memory), but cannot easily expand or revise their memory, cannot provide provenance for their predictions, and may produce "hallucinations".
  - RAG combines pre-trained parametric memory (seq2seq model) with non-parametric memory (dense vector index of Wikipedia, accessed with a pre-trained neural retriever).
  - Results show RAG models generate more specific, diverse, and factual language than a state-of-the-art parametric-only seq2seq baseline.