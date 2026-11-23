# LLM Wiki 總目錄：RAG (檢索增強生成) 知識庫

本知識庫專為「完全沒接觸過 RAG 的初學者」設計，將技術概念拆解為五個循序漸進的模組：

1. **[01_core_concepts.md](./01_core_concepts.md)** — **RAG 的核心概念與痛點解決**：用「開卷考試」比喻說明 RAG 如何解決 AI 幻覺與知識過時問題。
2. **[02_indexing_chunking.md](./02_indexing_chunking.md)** — **離線索引階段（Indexing）**：解析文件切塊（Chunking）、重疊區間（Overlap）與向量嵌入（Embedding）。
3. **[03_retrieval_rerank.md](./03_retrieval_rerank.md)** — **線上檢索階段（Retrieval）**：介紹向量語意搜尋、混合檢索（Hybrid Search）與重排序（Reranking）。
4. **[04_generation_guardrails.md](./04_generation_guardrails.md)** — **增強生成階段（Generation）**：如何透過 System Prompt 設定防幻覺護欄與來源引用。
5. **[05_evaluation_triad.md](./05_evaluation_triad.md)** — **RAG 系統評估三要素（RAG Triad）**：透過檢索相關性、忠實度與回答相關性驗證系統品質。